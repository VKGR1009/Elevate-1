# Elevate-1
# Task 1 – Network Reconnaissance and Packet Analysis

## Overview

This task demonstrates basic network reconnaissance using Nmap and Wireshark. The objective was to identify active hosts, scan for open ports, and observe the scan behavior at the packet level using live traffic analysis.

---

## Objectives

- Identify devices and open ports on the local subnet.
- Understand how TCP SYN scanning works.
- Analyze packet traffic captured during the scan using Wireshark.
- Document security risks associated with discovered services.

---

## Tools and Environment

- **Operating System**: Kali Linux (VMware environment)
- **Tools Used**:
  - [Nmap](https://nmap.org/)
  - [Wireshark](https://www.wireshark.org/)
- **Scanner IP**: 192.168.31.151
- **Scanned Subnet**: 192.168.31.0/24

---

## Nmap Scan

### Command Used

```bash
sudo nmap -sS 192.168.31.0/24 -oN scan_result.txt

Wireshark Capture
During the Nmap scan, a live packet capture was performed using Wireshark on the scanner system (Kali).

Steps to Capture
Start Wireshark

Select interface eth0

Begin packet capture

In a separate terminal, run the Nmap scan

Stop capture after scan completes

Save the file as nmap-scan.pcapng

Packet Filter Used for Analysis
wireshark
Copy
Edit
tcp.flags.syn == 1 && tcp.flags.ack == 0


