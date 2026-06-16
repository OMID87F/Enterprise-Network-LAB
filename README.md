# Enterprise Network LAB
## Overview
This project simulates a small enterprise network with multiple branches, focusing on network segmentation, routing, security, and centralized management.

The primary objective was to integrate the networking concepts learned throughout previous labs into a single, scalable environment that resembles a real-world enterprise deployment.

During development, the original design based on tunnel interfaces (EoIP and WireGuard) was replaced with a wired OSPF implementation due to stability limitations within the lab environment. This redesign provided valuable troubleshooting experience while maintaining the project's objectives.

## Objectives
* Build a segmented enterprise network using VLANs.

* Provide dynamic routing between multiple sites using OSPF.

* Deploy centralized DHCP services for all VLANs.

* Implement basic network security best practices.

* Apply access policies for management and client networks.

* Create a reusable enterprise lab for future expansion.

## Technologies Used
* MikroTik RouterOS
* Cisco IOS
* GNS3
* VLANs
* OSPF
* DHCP
* NAT
* SSH
* DHCP Snooping
* Port Security
* Simple Queues


## Key Features
Multi-site enterprise topology.

* Dynamic routing using OSPF.

* VLAN segmentation for different departments.

* DHCP services for all client networks.

* Internet access with selective NAT policies.

* CCTV network isolated from Internet access.

* SSH management restrictions using firewall policies.

* DHCP Snooping and Port Security on Cisco switches.

* Basic traffic management using Simple Queues.


## Repository Structure
```
README.md
Documentation.md
Topology.png
Sources/
```


## Validation
* The implementation was verified by:

* Successful inter-VLAN communication.

* End-to-end OSPF routing between branch networks.

* Internet connectivity for authorized VLANs.

* Restricted Internet access for CCTV devices.

* Successful DHCP address assignment.

* Validation of security and management policies.


## Challenges
Several challenges were encountered during development.

Initially, the network was designed to run OSPF over EoIP and WireGuard tunnels. While the tunnel configurations were completed successfully, unstable behavior inside the GNS3 environment caused routing sessions to reset frequently.

After investigating the issue, the design was revised to use a wired OSPF topology. This decision improved stability while preserving the overall learning objectives of the project.

Another issue involved Cisco switch configurations not persisting correctly during testing, which prevented DHCP clients from receiving IP addresses. Reconfiguring the switches resolved the problem.


## Documentation
Detailed configuration steps, screenshots, verification results, implementation notes, and troubleshooting are available in Documentation.md.

>**Note**: The detailed documentation is currently written in Persian (Farsi).


## Learning Outcomes
Through this project I gained hands-on experience with:

* Enterprise network design

* Multi-site routing with OSPF

* VLAN segmentation

* Cisco and MikroTik interoperability

* Basic network hardening

* DHCP deployment and troubleshooting

* Network policy implementation

* Troubleshooting complex multi-device environments
