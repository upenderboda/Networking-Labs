# Security Policy

## Objective

The objective of this project is to secure the enterprise network by implementing multiple Cisco security features.

## Security Features Implemented

### SSH Remote Management

- SSH Version 2 enabled
- Local user authentication
- Secure remote administration
- Telnet disabled

### Port Security

Port Security is enabled on end-device interfaces.

Configuration:

- Maximum MAC Address: 1
- Sticky MAC Address Learning
- Violation Mode: Shutdown

Purpose:

- Prevent unauthorized devices from connecting
- Protect against MAC flooding attacks

### VLAN Segmentation

Departments are separated into different VLANs:

- VLAN 10 - IT
- VLAN 20 - Finance
- VLAN 30 - Customer Service

Benefits:

- Reduces broadcast traffic
- Improves security
- Limits unauthorized access

### Access Control List (ACL)

An Extended ACL is configured to block Customer Service devices from accessing the Finance department.

Allowed:

- IT → Finance
- Finance → IT
- Customer Service → IT

Blocked:

- Customer Service → Finance

### DHCP

Dynamic IP address assignment is configured for all VLANs using DHCP pools.

Benefits:

- Automatic IP assignment
- Reduced configuration errors
- Simplified network management