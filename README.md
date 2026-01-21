# Cybersecurity Homelab - Project Eevee
This repository documents the design, deployment, and operation of a personal enterprise-style home lab built to simulate real-world corporate IT and Cybersecurity environmnents 

The lab is designed to support hands-on pratice with:
- Network Segmentation and Firewalling
- Active Directory and Identity Management
- SIEM Logging and Detection Engineering
- Red Team / Blue Team Security Testing
- Infrastructure Monitoring and Automation

## Objectives 
- Simulate a small enterprise network with realistic architecture
- Practice Security Operations, Detection, and Incident Response
- Gain hands-on experience with enterprise tooling
- Document infrastructure and security decisions

## High-Level Architecture
- One dedicated Proxmox node running on bare-metal hardware
- Virtualized Firewall providing routing, NAT, and network segmentation
- Windows and Linux VMs deployed behind firewall
- Multiple isolated VLANs for:
  - Managemnent
  - Server Infrastructure
  - Security Testing / Attack Simulation
- Physical switch providing VLAN trunking to the Proxmox host
- Out of band management via Proxmox web GUI

## Technology Stack

### Virtualization and Networking
- Proxmox VE
- OPNSense Firewall VM
- Virtual bridges and Linux networking
- VLAN based network segmentation

### Operating Systems
- Windows Server 2022 (AD, DNS, DHCP)
- Windows 10/11
- Linux (Ubuntu, Kali)

### Security Tooling (In progress, not yet deployed)
- Wireshark
- Nmap
- Splunk (SIEM)
  
### Hardware
- Intel i7 14th Gen 32 GB RAM 4060 ti Custom Desktop
- HP Intel i5 12th Gen 8 GB RAM 17'3 Laptop
- Raspberri Pi (planned for monitoring / utility services)
- 1 iOS / 1 Android mobile device (planned for MDM integration)
- Legacy 2011 iMac (planned for vulnerability exploitation testing)
  
## Repository Structure 
- /diagrams — Network topology + architecture diagrams
- /build-logs — Step-by-step build notes, issues, fixes
- /configs — Sanitized configs (no secrets)
- /labs — Security exercises, tests, and write-ups
- /assets — Screenshots used in documentation
