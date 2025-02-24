```bash
SSH@Rigel#write terminal
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
vlan 10 name test10 by port
 tagged ethe 1/1/4 
 untagged ethe 1/1/3 
 ip-subnet 10.0.10.0 255.255.255.0
!
!
!
!
!
!                                                                 
!
!
!
!
!
!
qos mechanism strict
aaa authentication web-server default enable
aaa authentication login default enable
chassis name FLS648-STK
enable telnet authentication
enable telnet password .....
enable super-user-password .....
fast uplink-span ethe 1/1/1 
hostname Rigel
ip address 10.0.0.20 255.255.255.0
ip dns server-address 10.0.0.1 1.1.1.1
no ip dhcp-client enable
ip default-gateway 10.0.0.1
username root nopassword
username skib nopassword
password-change any
snmp-server contact koliberekart@icloud.com                       
web client 10.0.0.113 
web access-group group
web-management frame bottom
no web-management hp-top-tools
web-management page-menu
web-management enable ethe 1/1/2 
web-management enable vlan 1
ssh access-group 1
interface ethernet 1/1/1
 port-name 1Gb Uplink
 speed-duplex 1000-full-master
!
interface ethernet 1/1/2
 port-name Management1
!
```
