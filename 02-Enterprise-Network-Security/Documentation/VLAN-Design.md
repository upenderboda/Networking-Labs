# VLAN Design

## Overview

This enterprise network is divided into three departments using Virtual Local Area Networks (VLANs) to improve network organization, performance, and security.

## VLAN Information

| VLAN ID | Department | Network Address | Subnet Mask | Default Gateway |
|---------|------------|-----------------|-------------|-----------------|
| 10 | IT | 192.168.10.0/26 | 255.255.255.192 | 192.168.10.1 |
| 20 | Finance | 192.168.10.64/26 | 255.255.255.192 | 192.168.10.65 |
| 30 | Customer Service | 192.168.10.128/26 | 255.255.255.192 | 192.168.10.129 |

## Port Assignment

| Switch Ports | VLAN | Department |
|--------------|------|------------|
| Fa0/2 - Fa0/6 | VLAN 10 | IT |
| Fa0/7 - Fa0/11 | VLAN 20 | Finance |
| Fa0/12 - Fa0/16 | VLAN 30 | Customer Service |
| Fa0/1 | Trunk | Router |

## Trunk Configuration

- Trunk Port: FastEthernet0/1
- Encapsulation: IEEE 802.1Q
- Allowed VLANs: 10, 20, 30

## Inter-VLAN Routing

Router-on-a-Stick (ROAS) is implemented using subinterfaces:

- GigabitEthernet0/0/0.10
- GigabitEthernet0/0/0.20
- GigabitEthernet0/0/0.30

Each subinterface acts as the default gateway for its respective VLAN.