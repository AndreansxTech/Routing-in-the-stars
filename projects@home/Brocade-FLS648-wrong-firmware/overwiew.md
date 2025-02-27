## This directory is dedicated to a weird situation with my Brocade FastIron LS648-STK switch.
### Nicknamed *"Rigel"*
### How it started
Lately, I wanted to do some inter-vlan routing on this switch since I found that it *is* capable of that. </br>
I wanted to achieve that by first creating the vlans, assigning subnets for them and then enabling routing between vlans globally on this switch.
Here is what I did:
```bash
SSH@Rigel(config)#vlan 10 name VLAN10
SSH@Rigel(config-vlan-10)#untagged eth 1/1/3 to 1/1/12 
Added untagged port(s) ethe 1/1/3 to 1/1/12 to port-vlan 10.
SSH@Rigel(config-vlan-10)#tagged eth 1/1/48
Added tagged port(s) ethe 1/1/48 to port-vlan 10.
SSH@Rigel(config-vlan-10)#ip-subnet 10.0.10.0/24
SSH@Rigel(config-vlan-ip-subnet)#
```
With that, I added ports 3 to 12 to the VLAN ID 10 and added what is typically a trunk port on the 48 port, and I assigned a subnet to this VLAN.
Here is the VLAN 20 configuration:
```bash
SSH@Rigel(config)#vlan 20 name PCs
SSH@Rigel(config-vlan-20)#tagged eth 1/1/48
Added tagged port(s) ethe 1/1/48 to port-vlan 20.
SSH@Rigel(config-vlan-20)#untagged eth 1/1/13 to 1/1/24
Added untagged port(s) ethe 1/1/13 to 1/1/24 to port-vlan 20.
SSH@Rigel(config-vlan-20)#ip-subnet 10.0.20.0/24
SSH@Rigel(config-vlan-ip-subnet)#
```
This is the cut output of `write terminal` command: ( It was cut to only include the important parts )
```bash
SSH@Rigel(config-vlan-ip-subnet)#write terminal
Current configuration:
!
ver 07.2.02aT7e1
!
stack unit 1
  module 1 fls-48-port-copper-base-module
  module 2 fls-cx4-1-port-10g-module
  module 3 fls-cx4-1-port-10g-module
!
!
!
!
vlan 1 name DEFAULT-VLAN by port
!
vlan 10 name VLAN10 by port
 tagged ethe 1/1/48 
 untagged ethe 1/1/3 to 1/1/12 
 ip-subnet 10.0.10.0 255.255.255.0
!
vlan 20 name PCs by port
 tagged ethe 1/1/48 
 untagged ethe 1/1/13 to 1/1/24 
 ip-subnet 10.0.20.0 255.255.255.0
```
After that, I wanted to try inter-vlan routing. So I tried to use the `ip routing` or `ip route` command in the global config level:
```bash
SSH@Rigel(config)#ip routing
Invalid input -> routing
Type ? for a list
SSH@Rigel(config)#ip route
Invalid input -> route
Type ? for a list
SSH@Rigel(config)#
```
This command `routing` or `route` seems to not even exist:
```bash
SSH@Rigel(config)#ip ?
  access-list                   Configure named access list
  address                       Set IP address
  arp                           Set ARP option
  default-gateway               Set IP default gateway
  dhcp                          Set DHCP option
  dhcp-client                   DHCP client address negotiation
  dhcp-server                   DHCP Server
  dns                           Set IP DNS
  icmp                          Control ICMP attacks
  igmp-report-control           Rate limit forwarding IGMP reports to upstream
                                Router, same as "ip multicast report-control"
  mtu                           Set IP MTU
  multicast                     Set IGMP snooping globally
  pimsm-snooping                Set PIMSM snooping globally
  preserve-acl-user-input-format
  show-acl-service-number       Use TCP/UDP service number to display ACL clause
  show-portname                 Use port name instead of interface number on
                                log messages
  show-service-number-in-log    Use App service number in log display
  show-subnet-length            Use subnet mask length to display IP subnet mask
  source                        Set source guard option
  ssh                           Configure Secure Shell
  ssl                           Configure Secure Socket
  tcp                           Control TCP SYN attacks           
  ttl                           Set IP TTL value
SSH@Rigel(config)#ip  
```
After some searching, I found that I should be in fact, able to use this command. This switch is L3 after all.
I checked the system:
```bash
SSH@Rigel#show ver
  Copyright (c) 1996-2010 Brocade Communications Systems, Inc.
    UNIT 1: compiled on Feb 16 2011 at 05:14:51 labeled as FGS07202a
                (2862535 bytes) from Primary FGS07202a.bin
        SW: Version 07.2.02aT7e1 
  Boot-Monitor Image size = 416213, Version:05.0.00T7e5 (Fev2)
  HW: Stackable FLS648 (PROM-TYPE FLS648-STK-U)
==========================================================================
UNIT 1: SL 1: FLS-48G 48-port Management Module
         Serial  #: M8AN23F00Z
         P-ENGINE  0: type D804, rev 01
         P-ENGINE  1: type D804, rev 01
==========================================================================
UNIT 1: SL 2: FLS-1XGC 1-port 10G Module (1-CX4)
==========================================================================
UNIT 1: SL 3: FLS-1XGC 1-port 10G Module (1-CX4)
==========================================================================
  400 MHz Power PC processor 8248 (version 130/2014) 66 MHz bus
  512 KB boot flash memory
30720 KB code flash memory
  256 MB DRAM
STACKID 1  system uptime is 2 hours 36 minutes 23 seconds 
The system : started=cold start  

SSH@Rigel#
```
Thats when I saw that the firmware is labeled as FGS07202a and *not as* **FLS07202a**.</br>
This might mean that for some unknown reason, my switch has a firmware from the GS series and not from the correct LS series. It basically functions probably because those switches might be similar on hardware level. But this lack of correct firmware, makes me unable to use the L3 options.