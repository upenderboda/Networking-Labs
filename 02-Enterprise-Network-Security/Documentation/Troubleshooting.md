# Troubleshooting

## Problems Encountered

### 1. VLAN Creation Error

Problem:
- Attempted to create VLAN using incorrect command syntax.

Solution:
- Used the correct commands:
  - vlan 10
  - name IT

---

### 2. Trunk Port Configuration

Problem:
- Router and switch could not communicate between VLANs.

Solution:
- Configured FastEthernet0/1 as an IEEE 802.1Q trunk.
- Verified using:
  - show interfaces trunk

---

### 3. DHCP Not Assigning IP Addresses

Problem:
- Devices were not receiving IP addresses automatically.

Solution:
- Created DHCP pools on the router.
- Configured excluded addresses.
- Verified using:
  - show ip dhcp binding
  - show ip dhcp pool

---

### 4. SSH Configuration

Problem:
- Remote management was not available initially.

Solution:
- Configured:
  - hostname
  - ip domain-name
  - username admin
  - crypto key generate rsa
  - ip ssh version 2
  - line vty 0 4
  - login local
  - transport input ssh

---

### 5. Port Security

Problem:
- Unauthorized devices could connect to switch ports.

Solution:
- Enabled Port Security.
- Configured Sticky MAC addresses.
- Set violation mode to Shutdown.

---

### 6. ACL Configuration

Problem:
- Customer Service devices were able to communicate with Finance.

Solution:
- Created an Extended ACL to deny traffic from VLAN 30 to VLAN 20.
- Applied the ACL to the appropriate router interface.

---

## Verification Commands

The following commands were used to verify the configuration:

- show vlan brief
- show interfaces trunk
- show ip interface brief
- show ip dhcp binding
- show ip dhcp pool
- show running-config
- show port-security
- show access-lists

## Lessons Learned

This project provided hands-on experience with:

- VLAN implementation
- Router-on-a-Stick
- DHCP configuration
- SSH configuration
- Port Security
- Extended ACLs
- Enterprise network troubleshooting