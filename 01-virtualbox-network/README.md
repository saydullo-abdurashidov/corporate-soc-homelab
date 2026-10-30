# VirtualBox Network Infrastructure

## Project Overview

This section documents the deployment of Kerio Control as a virtual firewall in an isolated corporate network environment using Oracle VirtualBox.

## Objectives

- Create a virtual machine for Kerio Control.
- Configure WAN and LAN network interfaces.
- Establish an isolated internal network.
- Access the Kerio Control web administration interface.
- Verify basic network connectivity.

## Environment

| Component | Configuration |
|---|---|
| Hypervisor | Oracle VirtualBox |
| Firewall | Kerio Control |
| Firewall VM | KERIO-FW01 |
| RAM | 1 GB |
| CPU | 1 Core |
| Virtual Disk | 20 GB |
| WAN Adapter | NAT |
| LAN Adapter | Internal Network |
| Internal Network Name | CORP-LAN |

## Network Configuration

| Interface | Configuration | Purpose |
|---|---|---|
| WAN | NAT | External network connectivity |
| LAN | 172.20.0.1/24 | Internal corporate network |

**LAN Network:** `172.20.0.0/24`

**LAN Gateway:** `172.20.0.1`

## Implementation

### 1. Virtual Machine Network Configuration

The Kerio Control virtual machine was configured with two network adapters:

- Adapter 1: NAT (WAN)
- Adapter 2: Internal Network (CORP-LAN)

### 2. Kerio Control Installation

Kerio Control was installed successfully on the virtual machine.

### 3. Network Interface Configuration

The LAN interface was configured with the static IP address `172.20.0.1/24`. The WAN interface was connected through VirtualBox NAT.

### 4. Web Administration Access

The Kerio Control web administration interface was accessed from the Administrator PC through a web browser.

## Connectivity Validation

The following connectivity checks were performed:

| Test | Result |
|---|---|
| Kerio LAN connectivity | Successful |
| External IP connectivity | Successful |
| DNS resolution | Successful |

The tests confirmed connectivity to the Kerio LAN interface, external IP connectivity, and DNS resolution.

## Screenshots

### 1. VirtualBox Network Adapter 1 — WAN (NAT)

![VirtualBox Adapter 1 NAT](https://github.com/user-attachments/assets/a585c4e7-ed83-42dc-91d7-1167afc38305)

### 2. VirtualBox Network Adapter 2 — LAN (Internal Network)

![VirtualBox Adapter 2 Internal Network](https://github.com/user-attachments/assets/58a4f3bc-9d0c-4af7-901f-8463758b3beb)

### 3. Kerio Control Installation

![Kerio Control installation](https://github.com/user-attachments/assets/bf0cfa72-9f80-46a0-ad12-9568ecfe868e)

### 4. Kerio Control After Installation

![Kerio Control after installation](https://github.com/user-attachments/assets/3c4d09c9-7777-4501-acb5-b8b620cdc4be)

### 5. Kerio Control Network Configuration

![Kerio Control network configuration](https://github.com/user-attachments/assets/4ad5ef98-43b0-40c9-99c7-771eb1ac595c)

### 6. Kerio Control Web Administration Dashboard

![Kerio Control dashboard](https://github.com/user-attachments/assets/c0453e4b-3b08-449a-b91c-f5f760ca4a6e)

## Skills Practiced

- Virtualization with Oracle VirtualBox
- Firewall deployment and configuration
- NAT and Internal Network configuration
- WAN and LAN networking
- Basic network connectivity troubleshooting
- Web-based firewall administration

## Next Steps

- Deploy Windows Server.
- Configure Active Directory Domain Services.
- Integrate Windows clients into the corporate network.
- Begin centralized security logging and monitoring.
