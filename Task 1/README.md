# Elevate-Labs
# Task 1: Scan Your Local Network for Open Ports

## Objective
    Discover open ports on devices in your **local network** to understand **network exposure** and identify potential vulnerabilities.


## Tools Used
- [Nmap](https://nmap.org/) v7.97
- [Wireshark](https://www.wireshark.org/) for packet analysis



 **Identified local IP and subnet:**
- IP Address: 192.168.xx.113
- Subnet Mask: 255.255.255.0 ➝ CIDR: /24


**Executed TCP SYN scan on local network:**
```bash
nmap -sS  192.168.xx.0/24 -oN task1_nmap.txt
```
- Saved scan results in task1_nmap.txt.

- Captured and analyzed network traffic using Wireshark.


**Learnings:**
- Performed SYN scan using Nmap and interpreted output.

- Captured and analyzed TCP packets using Wireshark.

- Identified open ports and matched them to known services.

- Evaluated potential vulnerabilities related to exposed services.