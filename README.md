

# Hi ! 👋 Happy to see you visiting my Networking Lab Project

![Static Badge](https://img.shields.io/badge/LAN_speed-Nan-%237ef728?style=for-the-badge)  
![Static Badge](https://img.shields.io/badge/Networking-%233449eb?style=for-the-badge)
![GitHub commit activity](https://img.shields.io/github/commit-activity/t/AndreansxTech/Homelab-2025?style=for-the-badge&logo=github)

—
##### Archiv 03.04.2025
## What is this repo?

This is **not a self-hosting lab** with NAS, media servers, etc.  
It’s a **network engineering learning lab** based on physical hardware and real-world configurations.  
Expect command-line configs, hand-drawn diagrams, technical breakdowns, and iterative scenarios.

This repo evolves as I grow – configs are wiped, topologies rebuilt, ideas retested. It’s a place for **experimentation**, not perfection.

—

## Learning Tracks

Here’s a breakdown of the networking areas I’m actively exploring and experimenting with:

### 1. Lab Infrastructure & Virtualization
> Getting the environment ready for hands-on learning

- Proxmox VE, Dell PowerEdge servers, backups, snapshots

### 2. VLANs & Layer 2 Switching
> Learning isolation, segmentation, and L2 communication

- 802.1Q tagging, trunks, access ports, SVIs

### 3. Layer 3 Concepts & Routing
> Understanding how traffic moves between subnets

- Static/dynamic routing, CIDR, route inspection

### 4. Addressing & Network Services
> Playing with the building blocks of communication

- MAC, ARP, DHCP, DNS, NAT, TFTP

### 5. Monitoring & Discovery
> Making the network observable and self-documenting

- SNMP, CDP, LLDP, syslog

### 6. Protocol Labs & Real-World Simulation
> Simulating realistic enterprise behaviors

- Multi-switch setups, failover tests, hybrid topologies

### 7. Certification Labs & Theory
> Working toward CompTIA Network+, MTCNA, and CCNA

- CLI practice, sandbox scenarios, concepts in action

—

## Repository Structure

This repo is split into multiple sections to help me organize my learning:
  
```
My-homelab/
│
├── README.md                 ← You are here!
├── lab-guide.md             ← How to use this repo (WIP)
├── assets/                  ← Diagrams, screenshots
│
├── scenarios/               ← Hands-on lab scenarios
│   ├── scenario-01_CCR2004_trunk_brocade_crs/
│   │   ├── topology.png
│   │   ├── description.md
│   │   ├── config/
│   │   │   ├── ccr2004.rsc
│   │   │   ├── brocade.txt
│   │   │   └── crs326.rsc
│   │   └── notes.md
│   └── …
│
├── knowledge/               ← Theoretical notes and concepts
│   ├── arp.md
│   ├── vlan.md
│   └── layer2-vs-layer3.md
│
├── issues/                  ← Troubleshooting logs
│   └── brocade_fw_issue.md
│
└── docs/                    ← Learning journal, topology
├── journal.md
├── general-network-topology.png

—
```

## Plans for now

I’m currently studying for **CompTIA Network+**, while building lab scenarios using MikroTik and Brocade gear.  
I’m still in high school – but that gives me a great head start.

—

## The Goal

My goal is to become a professional **network engineer**.  
This lab helps me:

* Practice designing and troubleshooting real networks  
* Learn routing/switching protocols deeply  
* Prepare for certifications like Network+, MTCNA, and CCNA  
* Explore how real devices behave and fail

—

## Key Resources

* [Latest issue: Brocade LS648 firmware](https://github.com/AndreansxTech/My-Homelab/blob/main/issues@homelab/Brocade-FLS648-firmware-issue/overwiew.md)  
* [Homelab Journal](https://github.com/AndreansxTech/My-homelab/blob/main/docs/journal.md)  
* [Network Topology](https://github.com/AndreansxTech/My-homelab/blob/main/docs/general-network-topology.png)

