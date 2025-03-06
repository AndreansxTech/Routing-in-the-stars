# Hi ! 👋 Happy to see you visiting my Homelab project

![Static Badge](https://img.shields.io/badge/LAN_speed-1GbE-%237ef728?style=for-the-badge)
![Static Badge](https://img.shields.io/badge/Services_status-Down-%23f72847?style=for-the-badge)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=Cloudflare&logoColor=white)
![Proxmox](https://img.shields.io/badge/proxmox-proxmox?style=for-the-badge&logo=proxmox&logoColor=%23E57000&labelColor=%232b2a33&color=%232b2a33)
![GitHub commit activity](https://img.shields.io/github/commit-activity/t/AndreansxTech/Homelab-2025?style=for-the-badge&logo=github)


## Milestones

This is a list of the milestones in my Homelab project. The status is updated regularly.

- [x] **Basic Infrastructure (✅)**
    - [x] Purchase of first servers (Dell PowerEdge R610, R710)
    - [x] Installation and configuration of Proxmox Virtual Environment on R710
    - [ ] Basic network configuration (VLANs, routing) - *In progress*
- [ ] **Gigabit Ethernet Network (❌)**
    - [ ] Full configuration of the 1GbE network
    - [ ] Testing and optimization of network performance
- [ ] **Storage and Backup (❌)**
    - [ ] Configuration of a NAS server
    - [ ] Implementation of a backup strategy for Proxmox
- [ ] **Multimedia (❌)**
    - [ ] Launching a Plex/Jellyfin server
- [ ] **10 Gigabit Ethernet Network (❌)**
    - [ ] Purchase and configuration of 10GbE hardware
    - [ ] Migration of key services to the 10GbE network

[ .. more to come here .. ]

## Plans for now

For now I would like to create a NAS server, Backup server for proxmox, TFTP server for my network hardware, Plex / Jellyfin Media Server and Minecraft server.
Currently Im learning general theory about VLANs


## Practical Networking: My Homelab Documentation 🧐

This repository is a hands-on resource documenting my experiences with building and maintaining a homelab network. I’ll be sharing practical configurations, scripts, and insights gained from real-world troubleshooting, with a focus on preserving knowledge about older or less common hardware.

A addition goal is to contribute to the longevity of network knowledge. This includes documenting solutions for obscure devices where information is scarce, and even archiving firmware and relevant resources to prevent them from disappearing from the internet. For example look at the <a href=”https://github.com/AndreansxTech/My-homelab/blob/main/projects%40home/Brocade-FLS648-wrong-firmware/overwiew.md”>Brocade FLS648 issue</a>

Expect to find configuration files for network devices, server setups, files, and automation scripts ( with sensitive information redacted, naturally ). Whether you’re a seasoned network engineer or just starting out, I hope this repository provides valuable inspiration and guidance, and contributes to the collective knowledge of the networking community.

## Start of the project
   I was interested in tech for kind of a long time. But never really did anything serious at my home apart from custom ROMing a couple of old samsung smartphones, until.. </br>
   Around the summer vacations I saw how big oppurtunities I had for creating a lab in my home. I have a big room and I have access to fast internet. Around the middle of October of 2024 I did my first step to creating a homelab. I bought two Dell PowerEdge servers: a R610 and a R710. </br>
   I learned some simple things about Proxmox Virtual Enviroment and realized how much potential it had. So I installed it on my R710. I created some simple VMs such as a Win11 or Ubuntu Server for a Minecraft Server.

## The Goal 📈

My objective is to develop practical skills in network engineering to pursue a career in this field. This homelab provides a platform to gain hands-on experience in areas such as:

*   Network design and implementation
*   Routing and switching protocols
*   Network security
*   Server administration
*   Troubleshooting and problem-solving

By actively engaging in these activities, I aim to acquire the knowledge and experience needed to excel in a network engineering role.


### Where you might want to look
- [The journal](https://github.com/AndreansxTech/My-homelab/blob/main/docs/journal.md)
- [The list of all devices in my homelab](https://github.com/AndreansxTech/Homelab-2025/blob/main/Inventory/devices.md)
- [Rack diagram](https://github.com/AndreansxTech/Homelab-2025/blob/main/Inventory/rack-diagram-placeholder)
- [General network diagram](https://github.com/AndreansxTech/My-homelab/blob/main/docs/general-network-topology.png)
