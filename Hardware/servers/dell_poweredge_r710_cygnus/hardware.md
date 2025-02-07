# Proxmox main host - Cygnus

## Purpose and Overview

*   **Purpose:** Virtualization server for VMs and LXCs
*   **Operating System:** Proxmox Virtual Enviroment 7.3.1
*   **Role in Homelab:** Currently this is the main virtualization server in the homelab


## Hardware Specifications

*   **Model:** Dell PowerEdge R710
*   **Processor (CPU):**
    *   Model: 2x Intel Xeon E5520
    *   Cores / Threads: 4c / 8t
    *   Clock Speed: around 2.2GHz
*   **Memory (RAM):**
    *   Capacity: 128 GB
    *   Type: DDR3 ECC
    *   Configuration: **bad configuration** 
*   **Storage (Disks):**
    *   **Format:** 2.5 Inch
    *   **RAID Controller:** Standard PERC 6/i
    *   **RAID Configuration:** everything currently is RAID 0
        *   **System Drives:** DELL 146 GB 15K HDD
        *   **Data Drives:** DELL 600GB 10K HDD
        *   **Additional Drives/Media:** HGST 900GB 10K HDD
*   **Network:**
    *   **Built-in Network Adapters:** 4x 1GbE
    *   **IP Addressing:** Static IP: 10.0.0.106/24, default gateway: 10.0.0.1
*   **Power:**
    *   **Power Supplies:** 2x 870W 
    *   **Redundancy:** No, one PSU is faulty
*   **Other:**
    *   **iDRAC:** 6 Enterprise
    *   **BIOS/UEFI Version:** Latest 6.6.0
    * **Cooling:** Stock DELL cooling

## Proxmox Configuration (Proxmox Specific)

*   **Proxmox VE Version:** 7.3.1
*   **Network Configuration (Bridge):** vmbr0 - main network bridge
*   **Storage:**
    *   **ZFS Pools:** None right now
*   **List of Virtual Machines/Containers:** 
    *   **VM 101:** Name: Win11, OS: Windows 11 LTSC, CPU: 8 vCPU, RAM: 16GB, Disk: 50GB
    *   **CT 202:** Name: Deb12, OS: Debian 12, CPU: 2 vCPU, RAM: 2GB, Disk: 8GB
* **Backup:** None right now

## Change Log

*   **2025-02-07** - [Initial update of this overview] 

## Notes and Issues

*   The VMs are named like this: 1xx
*   The CTs are named like this: 2xx
