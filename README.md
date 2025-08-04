# Elevate-1
Using Nmap to scan all devices on your local Wi-Fi network to find open ports and services. Then, with Wireshark, you're capturing the network traffic during that scan to understand how the devices respond, helping you learn how network scanning works and spot potential security risks.
# Task 1 – Network Port Scanning with Nmap

#🔧 Tools Used
- Nmap 7.95
- Operating System: Kali Linux

#🌐 Target
Scanned local network: `192.168.31.0/24`

# 📋 Summary of Findings
- Total hosts up: 6
- Devices include router, Android phone, Windows PC, and Kali Linux.
- Ports found open:
  - Router: 53, 80, 443, 7443, 8080, 8443
  - Windows PC: 135, 139, 445, 3306
  - Others: 2869 (UPnP)

# 🔐 Risk Analysis
- Router's web interfaces must be protected.
- SMB and MySQL ports on the PC should be secured.

# ✅ Command Used
```bash
nmap -sS 192.168.31.0/24 -oN scan_result.txt

