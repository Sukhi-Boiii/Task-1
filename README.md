
Cybersecurity Internship – Task 1: Nmap Network Scan
=====================================================

Objective:
----------
Scan the local network using Nmap to identify active devices, open ports, and exposed services.

Steps Performed:
----------------
1. Identified my local IP range.
2. Ran the following command:
   nmap -sS -oN nmapcmd.txt 192.168.1.0/24
3. Found 11 live hosts with various open ports.
4. Noted interesting services like:
   - HTTP (80), HTTPS (443), DNS (53)
   - NFS (2049), RPCBind (111), UPNP (5000)
   - High unknown ports like 49152, 9876

Findings Summary:
-----------------
- Common services like web, DNS, and FTP were open.
- Some hosts exposed services like RPC, NFS, RTSP, and iPhone sync.
- One device was identified as a Hikvision camera (vendor redacted in GitHub copy).

What I Learned:
---------------
- How to perform a SYN scan with Nmap
- How to analyze and interpret open ports
- Importance of masking sensitive data before uploading scan results publicly

Sensitive Data Masking (IMPORTANT):
-----------------------------------
Before uploading scan results to GitHub:
- Replace internal IPs like 192.168.1.X with <REDACTED-IP-X> or Device-X
- Mask all MAC addresses: e.g., <REDACTED-MAC>
- Remove vendor info like "Hikvision", "Apple" if privacy is a concern

Files Included:
---------------
- nmapcmd.txt (scan output with redactions)
- README.md (this file)

Notes:
------
Scan performed ethically in a lab/test environment.
All sensitive identifiers masked for public sharing.
