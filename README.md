# Organization-Networking-Infrastructure

About This Project

This project simulates a complete networking infrastructure for a multi-branch organization based in Karachi using Cisco Packet Tracer.
It demonstrates a realistic enterprise network setup with multiple departments, branches, inter-branch communication, VLANs, DHCP, NAT, routing, port security, and firewall rules.

The project covers:

Branch networks with department PCs and servers
Inter-branch communication using Edge Routers
Internet access with NAT
VLAN segmentation with Router-on-a-Stick (ROAS)
DHCP for dynamic IP assignment
Access Control Lists (ACLs) for firewalling
Port security and remote management

Network Overview
Branches

Branch 1

Finance Department – 3 PCs → Finance Switch
HR Department – 3 PCs → HR Switch
HTTP Server → Server Switch
Edge Router → Connects to other branches

Branch 2

Revenue Department – 3 PCs → Revenue Switch
Admin Department – 3 PCs → Admin Switch
Aggregation Switch → Connects both department switches
Edge Router → Connects to other branches

Branch 3

Sales Department – 3 PCs → Sales Switch
Project Department – 3 PCs → Project Switch
Aggregation Switch → Connects both department switches
Edge Router → Connects to other branches

Head Office (Branch 4)

Networks Department – 3 PCs → Networks Switch
Systems Department – 3 PCs → Systems Switch
HTTPS Server → Systems Switch
Edge Router → Connects to other branches
Internet Router → Connects to Internet (Google DNS 8.8.8.8)
Aggregation Node → Connects all Edge Routers

Key Features and Configurations

Subnetting and IP Management

Used VLSM to allocate IP pools efficiently for LAN, WAN, and inter-router links
DHCP configured on branch routers to provide IP addresses to devices dynamically

VLAN and Inter-VLAN Routing

Created VLANs for each department
Configured Router-on-a-Stick (ROAS) to allow inter-department communication within each branch

Routing

Static routing between branches ensures communication across branches
Backup routes are in place so communication continues if a primary link fails

NAT and Internet Access
NAT configured on Head Office router
All branches can reach the Internet (8.8.8.8) using NAT

Free WAN IP assigned for each branch

Firewall and ACL

Extended ACL configured for Web Servers

Branch 1 HTTP Server: accessible by Branch 3 and Branch 4 only

Branch 4 HTTPS Server: accessible by Branch 1 and Branch 2 only

Port Security

Port security enabled on server ports to restrict unauthorized devices

Remote Management

Routers and switches can be accessed remotely via Telnet/SSH

Console and privileged passwords configured

IP Addressing

All servers have static IPs

Devices inside VLANs receive dynamic IPs via DHCP

Tools Used

Cisco Packet Tracer – for simulation

VLSM – for efficient IP allocation

Router-on-a-Stick (ROAS) – for inter-VLAN routing

NAT – to provide Internet access

Extended ACL – firewall rules for web servers

How to Use / Open the Project

Open the .pkt file in Cisco Packet Tracer.

All routers, switches, VLANs, and devices are pre-configured.

Verify device connectivity using ping between PCs across VLANs and branches.

Access Web Servers via HTTP (Branch 1) or HTTPS (Branch 4) to test ACL rules.

Test Internet connectivity from any branch PC (ping 8.8.8.8).

Remote management can be tested via Telnet/SSH to routers and switches.

Project Highlights

Fully functional multi-branch network

Efficient IP allocation using VLSM

VLAN segregation for better network management

Router-on-a-Stick (ROAS) inter-VLAN routing

NAT and Internet access across branches

Access control using extended ACLs for servers

Port security and secure remote management

Redundant routing for branch communication

Author

Gotam Ladkani
Software Engineering Student
