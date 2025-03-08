
## *Brocade FastIron LS 648 STK* - Rigel

![Static Badge](https://img.shields.io/badge/broadcom-%23212121?style=for-the-badge&logo=broadcom&logoColor=cc092f&logoSize=auto)
![Static Badge](https://img.shields.io/badge/Outdated-%23e8271a?style=for-the-badge)
<!-- ![Static Badge](https://img.shields.io/badge/latest-%231a62e8?style=for-the-badge) -->
![GitHub last commit](https://img.shields.io/github/last-commit/andreansxtech/my-homelab?path=hardware%40home%2Fswitches%40homelab%2Frigel-switch%2Foverview.md&display_timestamp=author&style=for-the-badge)

Current situation with this switch is very weird. It seems to have a firmware from another switch. FGS instead of FLS in the firmware name.

256 MB DRAM
4 cores

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
STACKID 1  system uptime is 11 hours 29 minutes 24 seconds 
The system : started=cold start  

SSH@Rigel#
```
```ip routing``` command completly does not work. But it should work

```bash
SSH@Rigel(config)#vlan 10
SSH@Rigel(config-vlan-10)#ip routing
Invalid input -> routing
Type ? for a list
SSH@Rigel(config-vlan-10)#
```

In this folder, for archive purposes, is a binary file of the flash image from this switch, labeled as *FGS07202a.bin*. Read the <a href="/projects@home/Brocade-FLS648-firmware-issue/overwiew.md">Brocade-FLS648-wrong-firmware</a> article.

```bash
SSH@Rigel#copy flash tftp 10.0.0.113 FGS07202a.bin secondary 
SSH@Rigel#..............Flash to TFTP Done.
SSH@Rigel#
```