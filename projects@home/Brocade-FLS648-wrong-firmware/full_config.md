```bash
SSH@Rigel(config)#show tech-support
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
interface ethernet 1/1/3
 disable
!
interface ethernet 1/1/4
 disable
!
interface ethernet 1/1/5
 disable
!
interface ethernet 1/1/6
 disable
!
interface ethernet 1/1/7
 disable
!
interface ethernet 1/1/8
 disable
!
interface ethernet 1/1/9
 disable
!
interface ethernet 1/1/10
 disable
!
interface ethernet 1/1/11
 disable
!
interface ethernet 1/1/12
 disable
!
interface ethernet 1/1/13
 disable
!
interface ethernet 1/1/14
 disable
!
interface ethernet 1/1/15
 disable
!
interface ethernet 1/1/16
 disable
!
interface ethernet 1/1/17
 disable
!
interface ethernet 1/1/18
 disable
!
interface ethernet 1/1/19
 disable
!
interface ethernet 1/1/20
 disable
!
interface ethernet 1/1/21
 disable
!
interface ethernet 1/1/22
 disable
!
interface ethernet 1/1/23
 disable
!
interface ethernet 1/1/24
 disable
!
interface ethernet 1/1/25
 disable
!
interface ethernet 1/1/26
 disable
!
interface ethernet 1/1/27
 disable
!
interface ethernet 1/1/28
 disable
!
interface ethernet 1/1/29
 disable
!
interface ethernet 1/1/30
 disable
!
interface ethernet 1/1/31
 disable
!
interface ethernet 1/1/32
 disable
!
interface ethernet 1/1/33
 disable
!
interface ethernet 1/1/34
 disable
!
interface ethernet 1/1/35
 disable
!
interface ethernet 1/1/36
 disable
!
interface ethernet 1/1/37
 disable
!
interface ethernet 1/1/38
 disable
!
interface ethernet 1/1/39
 disable
!
interface ethernet 1/1/40
 disable
!
interface ethernet 1/1/41
 disable
!
interface ethernet 1/1/42
 disable
!
interface ethernet 1/1/43
 disable
!
interface ethernet 1/1/44
 disable
!
interface ethernet 1/1/45
 port-name fiber45
 disable
!
interface ethernet 1/1/46
 port-name fiber46
 disable
!
interface ethernet 1/1/47
 port-name fiber47
 disable
!
interface ethernet 1/1/48
 port-name fiber48
 disable
!
interface ethernet 1/2/1
 disable
!
interface ethernet 1/3/1
 disable
!
!
!
!
!
!
!
end

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
STACKID 1  system uptime is 2 hours 33 minutes 10 seconds 
The system : started=cold start  

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/1   Up      Forward Full 1G    None  No  1    0   001b.edec.ad80  1Gb Upli
1/1/2   Up      Forward Full 1G    None  No  1    0   001b.edec.ad81  Manageme
1/1/3   Disable None    None None  None  No  10   0   001b.edec.ad82          
1/1/4   Disable None    None None  None  No  10   0   001b.edec.ad83          
1/1/5   Disable None    None None  None  No  10   0   001b.edec.ad84          
1/1/6   Disable None    None None  None  No  10   0   001b.edec.ad85          
1/1/7   Disable None    None None  None  No  10   0   001b.edec.ad86          
1/1/8   Disable None    None None  None  No  10   0   001b.edec.ad87          
1/1/9   Disable None    None None  None  No  10   0   001b.edec.ad88          
1/1/10  Disable None    None None  None  No  10   0   001b.edec.ad89          
1/1/11  Disable None    None None  None  No  10   0   001b.edec.ad8a          
1/1/12  Disable None    None None  None  No  10   0   001b.edec.ad8b          
1/1/13  Disable None    None None  None  No  20   0   001b.edec.ad8c          
1/1/14  Disable None    None None  None  No  20   0   001b.edec.ad8d          
1/1/15  Disable None    None None  None  No  20   0   001b.edec.ad8e          
1/1/16  Disable None    None None  None  No  20   0   001b.edec.ad8f          
1/1/17  Disable None    None None  None  No  20   0   001b.edec.ad90          
1/1/18  Disable None    None None  None  No  20   0   001b.edec.ad91          
1/1/19  Disable None    None None  None  No  20   0   001b.edec.ad92          
1/1/20  Disable None    None None  None  No  20   0   001b.edec.ad93          
1/1/21  Disable None    None None  None  No  20   0   001b.edec.ad94          
1/1/22  Disable None    None None  None  No  20   0   001b.edec.ad95          
1/1/23  Disable None    None None  None  No  20   0   001b.edec.ad96          
1/1/24  Disable None    None None  None  No  20   0   001b.edec.ad97          
1/1/25  Disable None    None None  None  No  1    0   001b.edec.ad98          
1/1/26  Disable None    None None  None  No  1    0   001b.edec.ad99          
1/1/27  Disable None    None None  None  No  1    0   001b.edec.ad9a          
1/1/28  Disable None    None None  None  No  1    0   001b.edec.ad9b          
1/1/29  Disable None    None None  None  No  1    0   001b.edec.ad9c          
1/1/30  Disable None    None None  None  No  1    0   001b.edec.ad9d          
1/1/31  Disable None    None None  None  No  1    0   001b.edec.ad9e          
1/1/32  Disable None    None None  None  No  1    0   001b.edec.ad9f          
1/1/33  Disable None    None None  None  No  1    0   001b.edec.ada0          
1/1/34  Disable None    None None  None  No  1    0   001b.edec.ada1          
1/1/35  Disable None    None None  None  No  1    0   001b.edec.ada2          
1/1/36  Disable None    None None  None  No  1    0   001b.edec.ada3          
1/1/37  Disable None    None None  None  No  1    0   001b.edec.ada4          
1/1/38  Disable None    None None  None  No  1    0   001b.edec.ada5          
1/1/39  Disable None    None None  None  No  1    0   001b.edec.ada6          
1/1/40  Disable None    None None  None  No  1    0   001b.edec.ada7          
1/1/41  Disable None    None None  None  No  1    0   001b.edec.ada8          
1/1/42  Disable None    None None  None  No  1    0   001b.edec.ada9          
1/1/43  Disable None    None None  None  No  1    0   001b.edec.adaa          
1/1/44  Disable None    None None  None  No  1    0   001b.edec.adab          
1/1/45  Disable None    None None  None  No  1    0   001b.edec.adac  fiber45 
1/1/46  Disable None    None None  None  No  1    0   001b.edec.adad  fiber46 
1/1/47  Disable None    None None  None  No  1    0   001b.edec.adae  fiber47 
1/1/48  Disable None    None None  None  Yes N/A  0   001b.edec.adaf  fiber48 
1/2/1   Disable None    None None  None  No  1    0   001b.edec.adb0          
1/3/1   Disable None    None None  None  No  1    0   001b.edec.adb1          
Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/1   Up      Forward Full 1G    None  No  1    0   001b.edec.ad80  1Gb Upli

 Port 1/1/1 Counters:
         InOctets            296443385           OutOctets             18121487
           InPkts               228386             OutPkts                80798
  InBroadcastPkts                 3312    OutBroadcastPkts                   85
  InMulticastPkts                  811    OutMulticastPkts                 5992
    InUnicastPkts               224263      OutUnicastPkts                74721
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                22896       OutBitsPerSec                28328
     InPktsPerSec                    4       OutPktsPerSec                    5
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/2   Up      Forward Full 1G    None  No  1    0   001b.edec.ad81  Manageme

 Port 1/1/2 Counters:
         InOctets             17934673           OutOctets            294711964
           InPkts                77500             OutPkts               232891
  InBroadcastPkts                   90    OutBroadcastPkts                 3310
  InMulticastPkts                 1405    OutMulticastPkts                 5408
    InUnicastPkts                76005      OutUnicastPkts               224173
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                  190     OutFlowCtrlPkts                    0
     InBitsPerSec                28512       OutBitsPerSec                23888
     InPktsPerSec                    6       OutPktsPerSec                    5
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/3   Disable None    None None  None  No  10   0   001b.edec.ad82          

 Port 1/1/3 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/4   Disable None    None None  None  No  10   0   001b.edec.ad83          

 Port 1/1/4 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/5   Disable None    None None  None  No  10   0   001b.edec.ad84          

 Port 1/1/5 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/6   Disable None    None None  None  No  10   0   001b.edec.ad85          

 Port 1/1/6 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/7   Disable None    None None  None  No  10   0   001b.edec.ad86          

 Port 1/1/7 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/8   Disable None    None None  None  No  10   0   001b.edec.ad87          

 Port 1/1/8 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/9   Disable None    None None  None  No  10   0   001b.edec.ad88          

 Port 1/1/9 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/10  Disable None    None None  None  No  10   0   001b.edec.ad89          

 Port 1/1/10 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/11  Disable None    None None  None  No  10   0   001b.edec.ad8a          

 Port 1/1/11 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/12  Disable None    None None  None  No  10   0   001b.edec.ad8b          

 Port 1/1/12 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/13  Disable None    None None  None  No  20   0   001b.edec.ad8c          

 Port 1/1/13 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/14  Disable None    None None  None  No  20   0   001b.edec.ad8d          

 Port 1/1/14 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/15  Disable None    None None  None  No  20   0   001b.edec.ad8e          

 Port 1/1/15 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/16  Disable None    None None  None  No  20   0   001b.edec.ad8f          

 Port 1/1/16 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/17  Disable None    None None  None  No  20   0   001b.edec.ad90          

 Port 1/1/17 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/18  Disable None    None None  None  No  20   0   001b.edec.ad91          

 Port 1/1/18 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/19  Disable None    None None  None  No  20   0   001b.edec.ad92          

 Port 1/1/19 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/20  Disable None    None None  None  No  20   0   001b.edec.ad93          

 Port 1/1/20 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/21  Disable None    None None  None  No  20   0   001b.edec.ad94          

 Port 1/1/21 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/22  Disable None    None None  None  No  20   0   001b.edec.ad95          

 Port 1/1/22 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/23  Disable None    None None  None  No  20   0   001b.edec.ad96          

 Port 1/1/23 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/24  Disable None    None None  None  No  20   0   001b.edec.ad97          

 Port 1/1/24 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/25  Disable None    None None  None  No  1    0   001b.edec.ad98          

 Port 1/1/25 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/26  Disable None    None None  None  No  1    0   001b.edec.ad99          

 Port 1/1/26 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/27  Disable None    None None  None  No  1    0   001b.edec.ad9a          

 Port 1/1/27 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/28  Disable None    None None  None  No  1    0   001b.edec.ad9b          

 Port 1/1/28 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/29  Disable None    None None  None  No  1    0   001b.edec.ad9c          

 Port 1/1/29 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/30  Disable None    None None  None  No  1    0   001b.edec.ad9d          

 Port 1/1/30 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/31  Disable None    None None  None  No  1    0   001b.edec.ad9e          

 Port 1/1/31 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/32  Disable None    None None  None  No  1    0   001b.edec.ad9f          

 Port 1/1/32 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/33  Disable None    None None  None  No  1    0   001b.edec.ada0          

 Port 1/1/33 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/34  Disable None    None None  None  No  1    0   001b.edec.ada1          

 Port 1/1/34 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/35  Disable None    None None  None  No  1    0   001b.edec.ada2          

 Port 1/1/35 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/36  Disable None    None None  None  No  1    0   001b.edec.ada3          

 Port 1/1/36 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/37  Disable None    None None  None  No  1    0   001b.edec.ada4          

 Port 1/1/37 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/38  Disable None    None None  None  No  1    0   001b.edec.ada5          

 Port 1/1/38 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/39  Disable None    None None  None  No  1    0   001b.edec.ada6          

 Port 1/1/39 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/40  Disable None    None None  None  No  1    0   001b.edec.ada7          

 Port 1/1/40 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/41  Disable None    None None  None  No  1    0   001b.edec.ada8          

 Port 1/1/41 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/42  Disable None    None None  None  No  1    0   001b.edec.ada9          

 Port 1/1/42 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/43  Disable None    None None  None  No  1    0   001b.edec.adaa          

 Port 1/1/43 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/44  Disable None    None None  None  No  1    0   001b.edec.adab          

 Port 1/1/44 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/45  Disable None    None None  None  No  1    0   001b.edec.adac  fiber45 

 Port 1/1/45 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/46  Disable None    None None  None  No  1    0   001b.edec.adad  fiber46 

 Port 1/1/46 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/47  Disable None    None None  None  No  1    0   001b.edec.adae  fiber47 

 Port 1/1/47 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/1/48  Disable None    None None  None  Yes N/A  0   001b.edec.adaf  fiber48 

 Port 1/1/48 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/2/1   Disable None    None None  None  No  1    0   001b.edec.adb0          

 Port 1/2/1 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Port    Link    State   Dupl Speed Trunk Tag Pvid Pri MAC            Name      
1/3/1   Disable None    None None  None  No  1    0   001b.edec.adb1          

 Port 1/3/1 Counters:
         InOctets                    0           OutOctets                    0
           InPkts                    0             OutPkts                    0
  InBroadcastPkts                    0    OutBroadcastPkts                    0
  InMulticastPkts                    0    OutMulticastPkts                    0
    InUnicastPkts                    0      OutUnicastPkts                    0
        InBadPkts                    0
      InFragments                    0
       InDiscards                    0           OutErrors                    0
              CRC                    0          Collisions                    0
         InErrors                    0      LateCollisions                    0
      InGiantPkts                    0
      InShortPkts                    0
         InJabber                    0
   InFlowCtrlPkts                    0     OutFlowCtrlPkts                    0
     InBitsPerSec                    0       OutBitsPerSec                    0
     InPktsPerSec                    0       OutPktsPerSec                    0
    InUtilization                0.00%      OutUtilization                0.00%

Syslog logging: enabled (0 messages dropped, 0 flushes, 0 overruns)
    Buffer logging: level ACDMEINW, 23 messages logged
    level code: A=alert C=critical D=debugging M=emergency E=error
                I=informational N=notification W=warning

Static Log Buffer:
0d00h00m10s:I:System: Stack unit 1   Power supply 1  is up


Dynamic Log Buffer (50 lines):
0d02h29m35s:I:running-config was changed by  from ssh client 10.0.0.113
0d02h25m04s:I:VLAN: Id 20 added by  from ssh session
0d02h24m36s:I:running-config was changed by  from ssh client 10.0.0.113
0d02h21m19s:I:VLAN: Id 10 added by  from ssh session
0d02h19m21s:I:Security: SSH login by public key from src IP 10.0.0.113, src MAC 68f7.288d.ec40 to USER EXEC mode
0d00h00m24s:I:STP: VLAN 1 Port 1/1/2 STP State -> FORWARDING (FwdDlyExpiry)
0d00h00m22s:I:STP: VLAN 1 Port 1/1/2 STP State -> LEARNING (FwdDlyExpiry)
0d00h00m20s:I:System: Interface ethernet 1/1/2, state up
0d00h00m20s:I:STP: VLAN 1 Port 1/1/2 STP State -> LISTENING (MakeFwding)
0d00h00m17s:I:System: Interface ethernet 1/1/2, state down
0d00h00m17s:I:STP: VLAN 1 Port 1/1/2 STP State -> DISABLED (PortDown)
0d00h00m17s:I:STP: VLAN 1 Port 1/1/2 STP State -> FORWARDING (PortDown)
0d00h00m14s:I:STP: VLAN 1 Port 1/1/2 STP State -> FORWARDING (FwdDlyExpiry)
0d00h00m12s:I:STP: VLAN 1 Port 1/1/2 STP State -> LEARNING (FwdDlyExpiry)
0d00h00m12s:I:STP: VLAN 1 Port 1/1/1 STP State -> FORWARDING (FwdDlyExpiry)
0d00h00m10s:I:System: Interface ethernet 1/1/2, state up
0d00h00m10s:I:STP: VLAN 1 Port 1/1/2 STP State -> LISTENING (MakeFwding)
0d00h00m10s:I:STP: VLAN 1 Port 1/1/1 STP State -> LEARNING (FwdDlyExpiry)
0d00h00m09s:I:System: Interface ethernet 1/1/1, state up
0d00h00m09s:I:STP: VLAN 1 Port 1/1/1 STP State -> LISTENING (MakeFwding)
0d00h00m05s:I:DHCPC: protocol disabled
0d00h00m05s:I:System: Cold start
0d00h00m01s:W:System:Stack unit 1 Fan speed changed automatically to 1
real_transition-transit-sw_reset-discards:
1-0-0-0(1/1/1) 3-0-0-0(1/1/2) 0-0-0-0(1/1/3) 0-0-0-0(1/1/4) 
0-0-0-0(1/1/5) 0-0-0-0(1/1/6) 0-0-0-0(1/1/7) 0-0-0-0(1/1/8) 
0-0-0-0(1/1/9) 0-0-0-0(1/1/10) 0-0-0-0(1/1/11) 0-0-0-0(1/1/12) 
0-0-0-0(1/1/13) 0-0-0-0(1/1/14) 0-0-0-0(1/1/15) 0-0-0-0(1/1/16) 
0-0-0-0(1/1/17) 0-0-0-0(1/1/18) 0-0-0-0(1/1/19) 0-0-0-0(1/1/20) 
0-0-0-0(1/1/21) 0-0-0-0(1/1/22) 0-0-0-0(1/1/23) 0-0-0-0(1/1/24) 
0-0-0-0(1/1/25) 0-0-0-0(1/1/26) 0-0-0-0(1/1/27) 0-0-0-0(1/1/28) 
0-0-0-0(1/1/29) 0-0-0-0(1/1/30) 0-0-0-0(1/1/31) 0-0-0-0(1/1/32) 
0-0-0-0(1/1/33) 0-0-0-0(1/1/34) 0-0-0-0(1/1/35) 0-0-0-0(1/1/36) 
0-0-0-0(1/1/37) 0-0-0-0(1/1/38) 0-0-0-0(1/1/39) 0-0-0-0(1/1/40) 
0-0-0-0(1/1/41) 0-0-0-0(1/1/42) 0-0-0-0(1/1/43) 0-0-0-0(1/1/44) 
0-0-0-0(1/1/45) 0-0-0-0(1/1/46) 0-0-0-0(1/1/47) 0-0-0-0(1/1/48) 
0-0-0-0(1/2/1) 0-0-0-0(1/3/1) 
1/1/1: C 1/1/2: C 1/1/3: C 1/1/4: C 1/1/5: C 1/1/6: C 1/1/7: C 1/1/8: C 1/1/9: C 1/1/10: C 1/1/11: C 1/1/12: C 1/1/13: C 1/1/14: C 1/1/15: C 1/1/16: C 1/1/17: C 1/1/18: C 1/1/19: C 1/1/20: C 1/1/21: C 1/1/22: C 1/1/23: C 1/1/24: C 1/1/25: C 1/1/26: C 1/1/27: C 1/1/28: C 1/1/29: C 1/1/30: C 1/1/31: C 1/1/32: C 1/1/33: C 1/1/34: C 1/1/35: C 1/1/36: C 1/1/37: C 1/1/38: C 1/1/39: C 1/1/40: C 1/1/41: C 1/1/42: C 1/1/43: C 1/1/44: C 1/1/45: C 1/1/46: C 1/1/47: C 1/1/48: C 
1/2/1:XG-CX4 
1/3/1:XG-CX4 
[Empty]
GADDR        =   0126ed60       Dram Buf     =       1820
AVAIL_B      =        220       USED_B       =       1600
CPU_R        =       4623       Buf Msgs     =          0
SNOOP_TX     =      13835       SNOOP_DP     =         41
GET_B        =      16827       FREE_B       =      15227
Sw_Mode      =          2       New_Addr     =         53
NA_Learn     =         31       NA_Age       =         22
NA_Update    =          0       NA_Hash_Full =          0
NA_Hash_Del  =          0       SFLOW_sample =          0
Buf_G_Msgs   =          0       Buf_F_Msgs   =          0
Buf_Count    =          0
CPU_XR[TC0-3 [1360][0][3263][0]
CPU_XR[TC4-7 [0][0][0][0]
SSH@Rigel(config)#
```