# Task 4: Setup and Use a Firewall on Windows

## Objective
Configure and test basic firewall rules to allow or block traffic on a Windows system.

---

## Tools Used
- Windows Defender Firewall
- ncat (Netcat) for testing port connectivity

---

## Contents

### Firewall Status

- ![Firewall Status](imgs/firewall_stauts.png)

### Inbound Rules

- ![Inbound Rules](imgs/inbound_rules.png)
- Rules file: [`rules/inbound.txt`](rules/inbound.txt)

### Outbound Rules

- ![Outbound Rules](imgs/outbound_rules.png)
- Rules file: [`rules/outbound.txt`](rules/outbound.txt)

### Blocking Port 23 (Telnet)

- ![Blocking Telnet Step 1](imgs/blocking_telnet_1.png)
- ![Blocking Telnet Step 2](imgs/blocking_telnet_2.png)
- ![Blocking Telnet Step 3](imgs/blocking_telnet_3.png)
- ![Blocking Telnet Step 4](imgs/blocking_telnet_4.png)
- ![Blocking Telnet Step 5](imgs/blocking_telnet_5.png)

### Updated Inbound Rules

- ![Updated Inbound Rules](imgs/updated_inbound_rules.png)

### After Blocking Telnet

- ![Telnet Blocked](imgs/telnet_block.png)

### Restoring Original State

- ![Restore Firewall](imgs/restore_previous_firewall.png)

### After Restoring Original State

- ![Telnet Unblocked](imgs/telnet_unblock.png)

---

## Video Demonstration

- [`Telnet checking.mkv`](Telnet%20checking.mkv)  
  A video walkthrough demonstrating the firewall behavior when Telnet port is Unblocked.

---

## Summary: How Firewall Filters Traffic

1. **Inspects Each Packet:**  
   Every data packet trying to enter or leave your system is analyzed.

2. **Matches Against Rules:**  
   The firewall checks if the packet matches any allow or block rules you've configured (e.g., block port 23, allow port 22).

3. **Decision Made:**  
   - If a packet matches an **allow** rule, it is permitted through.  
   - If it matches a **block** rule, it is dropped (ignored).

4. **Default Behavior:**  
   If no rule matches, most firewalls follow a **default deny** policy—blocking everything not explicitly allowed.

