# 02 — Kerio Control Firewall

## Overview

This stage documents the deployment and initial configuration of Kerio Control as a virtual firewall in the corporate SOC home lab.

Kerio Control is used to separate the WAN and LAN networks and provide basic network connectivity for the lab environment.

## Lab Environment

| Component | Configuration |
|---|---|
| Hypervisor | Oracle VirtualBox |
| Firewall | Kerio Control |
| VM Name | KERIO-FW01 |
| RAM | 1 GB |
| CPU | 1 Core |
| Storage | 20 GB |
| WAN Interface | NAT |
| LAN Interface | Internal Network |

## Network Configuration

| Network Parameter | Value |
|---|---|
| Internal Network Name | SWITCH |
| LAN IP Address | 172.20.0.1 |
| Subnet Mask | 255.255.255.0 |
| Network Address | 172.20.0.0/24 |
| WAN Connection | VirtualBox NAT |

## Implementation Steps

1. Created the `KERIO-FW01` virtual machine in VirtualBox.
2. Configured the first network adapter as NAT (WAN).
3. Configured the second network adapter as Internal Network (`SWITCH`).
4. Installed Kerio Control.
5. Configured the LAN interface with a static IP address.
6. Accessed the Kerio Control web administration dashboard.
7. Checked basic network connectivity.

## Connectivity Verification

The following connectivity checks were performed:

- LAN gateway connectivity: `172.20.0.1`
- External IP connectivity: `8.8.8.8`
- DNS resolution: `google.com`

The reported tests were successful.

## Screenshots

### Kerio Control Dashboard

<img width="974" height="692" alt="image" src="https://github.com/user-attachments/assets/b4c7bdc5-93c1-4419-acd5-62ba27cb1685" />


### Network Interfaces

<img width="1021" height="728" alt="image" src="https://github.com/user-attachments/assets/680c684f-8013-469c-bf44-cc288a35dfc3" />

### Connectivity Tests

<img width="1022" height="730" alt="image" src="https://github.com/user-attachments/assets/bc7de3fa-c62f-4985-8b03-63b665faf48b" />

## Skills Practiced

- VirtualBox network configuration
- Firewall deployment
- WAN and LAN interface configuration
- NAT and Internal Network
- Basic network troubleshooting
- Connectivity verification

## Next Steps

- Deploy Windows Server 2022.
- Configure Active Directory Domain Services.
- Configure DNS for the domain environment.
- Connect Windows client machines to the corporate network.
- Prepare the infrastructure for centralized security monitoring.
