Network Topology – Detailed Explanation

This topology represents a multi-layer hierarchical network design built using VLAN segmentation, Layer 2 switching, Layer 3 routing, and inter-VLAN communication. The network is divided into multiple VLANs distributed across access switches, which connect to distribution-layer switches, and finally to a core layer responsible for routing and network-wide connectivity.

Access Layer

At the bottom, several access switches connect end-user devices such as PCs and workstations. Each block of PCs belongs to a different VLAN (e.g., VLAN10, VLAN20, VLAN30, VLAN40, VLAN50, VLAN60, VLAN70, VLAN80).
The access layer provides:

VLAN membership for hosts

Basic switching

Uplink connections to the distribution layer

Segmentation of broadcast domains

Distribution Layer

The distribution switches aggregate traffic from all access switches. Their main functions include:

Inter-VLAN routing (when multilayer switches are used)

Redundancy and load balancing between uplinks

Policy enforcement (ACLs, security, QoS)

Path selection using dynamic routing or spanning tree optimizations

The topology shows multiple redundant links between distribution switches and the core layer, ensuring higher availability and avoiding single points of failure.

Core Layer

The core devices at the center act as the backbone of the network. Their responsibilities include:

High-speed packet forwarding

Routing between large network segments

Providing fast, reliable connectivity for the entire LAN

The core also connects to external services and servers through Gigabit interfaces.

Server Segment

On the right side, a server is attached through a Layer 3 switch. The server IP subnet is routed via the core, allowing internal users to access centralized services such as DHCP, DNS, or file hosting.

Upper VLAN Segments (130, 140, 150, 160)

At the top, additional VLANs host network appliances, administrative PCs, or separate department segments. These are uplinked through access switches into the distribution layer.

IP Addressing

The main subnet shown is 192.168.1.0/24, used for interconnection between distribution and core switches.
Each access VLAN would contain its own subnet (e.g., 192.168.10.0/24 for VLAN10, 192.168.20.0/24 for VLAN20, etc.).

Redundancy & Spanning Tree

The black dashed lines represent redundant Layer 2 paths.
These links may be managed using:

RSTP / MSTP

EtherChannel (LACP/PAgP)

Layer 3 routed links for loop-free topologies

This ensures that even if a link fails, traffic can still be forwarded through an alternate path.

Summary

This topology demonstrates a fully structured enterprise network consisting of:

A 3-tier design (Core – Distribution – Access)

Multiple VLANs for segmentation

Layer 2 redundancy

Layer 3 routing between VLANs

Server integration

Structured cabling and hierarchical design principles
