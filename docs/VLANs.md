## VLANs

The goal is to segment my home network using VLANs based on the third octet of the LAN IP address: `10.0.x.0/24`, where `x` corresponds to the VLAN ID. The planned segmentation is as follows:

*   **VLAN Naming Convention:** The VLAN ID corresponds to the third octet of the IP address in the `10.0.x.0/24` network.
*   **Address Range:** Each VLAN will use a subnet mask of `/24`.

Here's a detailed description of each planned VLAN:

*   **VLAN 10 - PCs, Laptops, and Game Consoles**
    *   **IP Range:** `10.0.10.0/24`
    *   **Purpose:** User devices such as desktops, laptops, and gaming consoles.
*   **VLAN 20 - Servers**
    *   **IP Range:** `10.0.20.0/24`
    *   **Purpose:** Servers running within the homelab environment.
*   **VLAN 21 - Virtual Machines (VMs)**
    *   **IP Range:** `10.0.21.0/24`
    *   **Purpose:** Virtual Machines (VMs) running on the servers.
*   **VLAN 22 - Containers (CTs)**
    *   **IP Range:** `10.0.22.0/24`
    *   **Purpose:** Containers (CTs) running on the servers.
*   **VLAN 23 - Remote management interfaces (iDRAC)**
    *   **IP Range:** `10.0.23.0/24`
    *   **Purpose:** Remote access interfaces for backup communication with servers.
*   **VLAN 30 - Surveillance Cameras**
    *   **IP Range:** `10.0.30.0/24`
    *   **Purpose:** PoE powered surveillance cameras for home security.
*   **VLAN 40 - Guest Wi-Fi**
    *   **IP Range:** `10.0.40.0/24`
    *   **Purpose:** Wireless network for guests with restricted access to network resources.
    *   **DHCP IP Pool:** `10.0.40.100 - 10.0.40.200`
*   **VLAN 41 - Normal Wi-Fi**
    *   **IP Range:** `10.0.41.0/24`
    *   **Purpose:** Wireless network for my whole family at home.
    *   **DHCP IP Pool:** `10.0.41.100 - 10.0.41.200`
*   **VLAN 99 - Management Network**
    *   **IP Range:** `10.0.99.0/24`
    *   **Purpose:** Network devices (switches, routers, access points) and my laptop (ThinkPad) requiring separation from the rest of the network. Inter-VLAN routing between this VLAN and other VLANs will be blocked.
    *   **Rationale:** Isolation of network management devices to enhance security.

**Routing:**

Inter-VLAN routing will be handled by a combination of:

*   **MikroTik CCR2004-1G-12S+2XS**
*   **Brocade FastIron LS648** - Possible because of <a href="/projects@home/issues@homelab/Brocade-FLS648-firmware-issue/overwiew.md">L3 firmware</a>
*   **additional used routing devices will be added here**

The specific routing configuration (which VLANs are routed by which device) will be determined and documented separately.


**Security Considerations:**

*   **Firewall Policies:** Inter-VLAN firewall policies will be implemented to control traffic flow.  A connectivity matrix will be documented separately to define allowed communication paths.  Initial policy will be deny-by-default, with exceptions explicitly allowed.
*   **Future Considerations:**  Evaluation and potential implementation of Intrusion Detection/Prevention System (IDS/IPS) to monitor critical VLANs.

**Availability and Redundancy:**

*   **Link Aggregation:** Link aggregation (LAG/LACP) will be used where possible to increase bandwidth and provide link redundancy.  Specific LAG configurations will be documented separately.


**Currently to do:**

*   Configure the switch/router to support these VLANs.
*   Assign the appropriate ports to each VLAN.
*   Configure VLAN interfaces on the router(s) for inter-VLAN routing (if desired, excluding VLAN 99).
*   Configure DHCP on each VLAN to automatically assign IP addresses, using the specified IP Pools for Wi-Fi networks. 
*   Configure DHCP on each VLAN to automatically assign IP addresses.