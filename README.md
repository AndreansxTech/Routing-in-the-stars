# Hi ! 👋 Happy to see you visiting my Homelab project

<!— ![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=Cloudflare&logoColor=white)  
![Proxmox](https://img.shields.io/badge/proxmox-proxmox?style=for-the-badge&logo=proxmox&logoColor=%23E57000&labelColor=%232b2a33&color=%232b2a33)  —>

![Static Badge](https://img.shields.io/badge/LAN_speed-Nan-%237ef728?style=for-the-badge)  
![Static Badge](https://img.shields.io/badge/Networking-%233449eb?style=for-the-badge)
![GitHub commit activity](https://img.shields.io/github/commit-activity/t/AndreansxTech/Homelab-2025?style=for-the-badge&logo=github)


## Learning Tracks

Here’s a breakdown of the networking areas I’m actively exploring and experimenting with in my homelab. This lab isn’t about finishing anything – I will mostl likely reset configurations often, rebuild topologies from scratch, and try out different methods to reinforce concepts. It’s an ongoing cycle of experimentation and learning.

### **1. Lab Infrastructure & Virtualization**

> Getting the environment ready for hands-on learning

- Setup of physical servers (Dell PowerEdge R610 and R710)  
- Installation and use of **Proxmox VE** for virtualization  
- Using backup and snapshot tools to iterate fast

### **2. VLANs & Layer 2 Switching**

> Learning isolation, segmentation, and L2 communication

- VLAN creation and tagging (802.1Q)  
- Trunk vs access ports  
- Practice with VLAN interfaces (SVIs)  
- Using Brocade CLI for L2 configuration  


### **3. Layer 3 Concepts & Routing**

> Understanding how traffic moves between subnets

- Static routing and basic concepts of dynamic routing  
- RIP v1/v2 lab scenarios  
- Inter-VLAN routing using Layer 3 switch  
- Introduction to CIDR, subnetting, and route summarization  
- Practicing route inspection and troubleshooting

### **4. Addressing & Network Services**

> Playing with the building blocks of communication

- MAC addressing, ARP, and IP addressing  
- DHCP configuration and IP pool planning  
- DNS basics and practical server setup  
- Introduction to NAT and PAT  
- TFTP server setup for firmware and config uploads

### **5. Monitoring & Discovery**

> Making the network observable and self-documenting

- SNMP, CDP, LLDP experiments  
- Syslog and basic logging of events  
- Topology mapping and automatic discovery  


### **6. Protocol Labs & Real-World Simulation**

> Simulating realistic enterprise behaviors

- STP and redundancy basics (concept only for now)  
- Multi-switch VLAN labs  
- Router-on-a-stick setup  
- Testing convergence and failover behavior  
- Mixing real hardware with virtualized routers

### **7. Certification Labs & Theory**

> Following a progression toward industry credentials

- Currently focusing on **CompTIA Network+**  
- MikroTik MTCNA practice (using real CCR/CRS devices)  
- Introduction to CCNA-level labs  
- Building foundational knowledge in CLI usage  
- Using the homelab as an offline CCNA/MTCNA sandbox

—

## Plans for now

I’m not hosting services anymore – instead, I’m focused entirely on **learning networking**.  
Right now, I’m studying for the **CompTIA Network+ certification**, mostly with online courses. It's not like I will be able to take the exam anytime soon because I am still in middle school but that actually gives me a kind of a headstart

Expect a mix of command-line configs, hand-drawn diagrams, and technical notes. The lab will be rebuilt over and over as I progress through different networking topics and certifications.

—

## Practical Networking: My Homelab Documentation 🧐

This repository serves as my personal knowledge base for learning network engineering through real hardware and configurations. I document every step with code, text, and diagrams (maybe  drawn on my iPad), especially focusing on older hardware like Brocade switches that are still useful in labs but lack modern documentation.

I also archive firmware and rare config examples to contribute to the long-term preservation of networking know-how.

—

## The Goal 📈

My goal is to become a professional network engineer.  
This homelab gives me a hands-on way to:

*   Practice designing and troubleshooting real networks  
*   Learn routing/switching protocols and concepts deeply  
*   Get ready for certifications like Network+, MTCNA, and CCNA  
*   Explore the behavior of both virtual and physical network devices

—

## Explore the Homelab: Key Resources 🔍

*   **Latest issue:** [Brocade FastIron LS648 firmware problem](https://github.com/AndreansxTech/My-Homelab/blob/main/issues@homelab/Brocade-FLS648-firmware-issue/overwiew.md)  
*   **Homelab Journal 📝:** [My learning log](https://github.com/AndreansxTech/My-homelab/blob/main/docs/journal.md)  
*   **Hardware Inventory 🧰:** [Device list](https://github.com/AndreansxTech/Homelab-2025/blob/main/Inventory/devices.md)  
*   **Rack Diagram 🏢:** [Rack layout (placeholder)](https://github.com/AndreansxTech/Homelab-2025/blob/main/Inventory/rack-diagram-placeholder)  
*   **Network Topology 🌐:** [Current topology](https://github.com/AndreansxTech/My-homelab/blob/main/docs/general-network-topology.png)
