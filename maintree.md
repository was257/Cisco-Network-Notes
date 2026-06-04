🌐 CCNA 200-301 Keyword Mind Map
1. Network Fundamentals
OSI vs TCP/IP

Layer 1-7 / Encapsulation / Decapsulation / PDU / Data / Segment / Packet / Frame / Bits

Cabling

UTP / Fiber / Straight-through / Crossover / T568A / T568B

Topologies

Star / Mesh / 3-Tier / Core / Distribution / Access / Collapsed Core / 2-Tier / Spine-Leaf

IPv4 Addressing

Subnetting / VLSM / CIDR / Public IP / Private IP / RFC 1918 / Broadcast / Multicast / Unicast

IPv6

128-bit / Hexadecimal / Omit Zeros / Double Colon (::) / Global Unicast / Link-Local (fe80::) / EUI-64

2. Network Access (L2 Switching)
VLANs

Broadcast Domains / Access Port / Trunk Port / 802.1Q / Tagging / Native VLAN / Native VLAN Mismatch

STP (802.1D)

Broadcast Storms / MAC Table Instability / BPDU / Bridge ID / Priority (4096 Multiples) / MAC Address / Root Bridge / Root Port (RP) / Designated Port (DP) / Non-Designated Port (NDP) / Blocking / Listening / Learning / Forwarding

PVST+

Cisco Proprietary / Per-VLAN STP / System ID Extension (Priority + VLAN ID)

RSTP (802.1w)

Fast Convergence / Proposal/Agreement / Discarding / Learning / Forwarding / Alternate Port / Backup Port / Edge Port / PortFast / UplinkFast / BackboneFast

EtherChannel

Link Aggregation / Port-Channel / Load Balancing / LACP (Active/Passive) / PAgP (Desirable/Auto) / On Mode / Speed/Duplex Match

Wireless

WLC / LAP / Split-MAC Architecture / CAPWAP / SSID / WPA2 / WPA3 / Pre-Shared Key (PSK) / 802.1X

3. IP Connectivity (L3 Routing)
Routing Concepts

Routing Table / Longest Match Rule / Administrative Distance (AD) / Metric / Next-Hop / CEF / FIB / Adjacency Table

Static Routing

Standard Static / Default Route (0.0.0.0/0) / Floating Static Route (Backup, High AD)

OSPFv2

Link-State / IGP / Dijkstra Algorithm / Cost (Bandwidth) / Area 0 (Backbone) / Wildcard Mask / Router ID

OSPF Adjacency

Hello/Dead Intervals / Area ID / Authentication Match / Init / Two-Way / ExStart / Exchange / Loading / Full

OSPF Network Types

Point-to-Point / Broadcast / DR (Designated Router) / BDR (Backup DR) / Priority / Multicast (224.0.0.5, 224.0.0.6)

Inter-VLAN Routing

Router-on-a-Stick (ROAS) / Subinterfaces / SVI (interface vlan) / Layer 3 Switch / ip routing

4. IP Services
DHCP

DORA Process (Discover, Offer, Request, Acknowledge) / DHCP Relay Agent / ip helper-address

NAT

Inside Local / Inside Global / Outside Local / Outside Global / Static NAT (1:1) / Dynamic NAT (Pool) / PAT (Overload, Ports)

NTP

Time Synchronization / Stratum Levels / Master / Client

FHRP

Default Gateway Redundancy / HSRP (Active/Standby, Virtual IP/MAC, Cisco) / VRRP (Master/Backup)

Remote Access

Telnet (Port 23, Clear Text, Insecure) / SSH (Port 22, Crypto Key, Secure) / VTY Lines (line vty 0 4)

5. Security Fundamentals
Device Security

line console 0 / password / login / enable secret (MD5/SHA) / service password-encryption (Type 7)

ACLs (Access Control Lists)

Packet Filtering / Top-Down Processing / Implicit Deny Any

Standard ACL

1-99 / 1300-1999 / Source IP Only / Place Closest to Destination

Extended ACL

100-199 / 2000-2699 / Source/Destination IP / Protocol (TCP/UDP) / Port Number / Place Closest to Source

Port Security

switchport port-security / Max MACs / Static / Sticky MAC / Violations (Protect, Restrict, Shutdown)

Threats & Defense

AAA (Authentication, Authorization, Accounting) / Dynamic ARP Inspection (DAI) / DHCP Snooping

6. Automation and Programmability
SDN

Controller / Centralized Control Plane / Distributed Data Plane / Management Plane

APIs

Northbound API (REST, Intent-based) / Southbound API (NETCONF, RESTCONF, OpenFlow) / Cisco DNA Center

Data Formats

JSON (Braces {}, Brackets [], Key-Value) / XML (Tags <>) / YAML (Indentation, Dashes -)

Configuration Management

Ansible (Agentless, Playbooks, YAML) / Puppet (Agent-based, Manifests) / Chef (Agent-based, Recipes, Ruby)
