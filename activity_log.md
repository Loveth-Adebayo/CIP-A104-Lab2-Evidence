# LAB 2 ACTIVITY LOG
# File Upload and Command Execution Security Assessment

**Student:** Loveth Adebayo  
**Date:** 29 August 2026  
**Course:** CIP-A104 — Offensive Security Operations I  

---

## Activity Timeline

| Date/Time | Activity | Tool Used | Outcome | Notes/Corrections |
|-----------|----------|-----------|---------|-------------------|
| 26 Aug 2026 20:30 | Configured Host-Only network for VMs | VirtualBox | Both VMs on vboxnet0 | None |
| 26 Aug 2026 21:00 | Enabled enp0s8 on Ubuntu | dhclient | IP: 192.168.56.107 | Manual dhclient needed |
| 26 Aug 2026 21:15 | Made network config permanent | netplan | Survives reboot | Added to /etc/netplan/ |
| 27 Aug 2026 09:00 | Confirmed NOT publicly exposed | Firefox (Host) | Connection failed | Isolation confirmed |
| 27 Aug 2026 09:15 | Logged into DVWA | Firefox | Logged in as admin | None |
| 27 Aug 2026 09:30 | Set DVWA security level to Low | DVWA | Security Level: Low | None |
| 27 Aug 2026 10:00 | Uploaded marker file to DVWA | DVWA | Upload successful | None |
| 27 Aug 2026 10:15 | Retrieved uploaded file | Firefox/curl | File accessible | None |
| 27 Aug 2026 10:30 | Performed mismatch test on DVWA | DVWA | Upload successful | None |
| 27 Aug 2026 11:00 | Reset Mutillidae database | Mutillidae | Reset successful | None |
| 27 Aug 2026 11:15 | Created Mutillidae account | Mutillidae | Account: testuser | None |
| 27 Aug 2026 11:30 | Uploaded TXT file to Mutillidae | Mutillidae | Upload successful | None |
| 27 Aug 2026 11:45 | Uploaded PHP file to Mutillidae | Mutillidae | Upload successful | No validation |
| 27 Aug 2026 12:00 | DNS baseline test | Mutillidae | NXDOMAIN output | None |
| 27 Aug 2026 12:15 | Command injection test | Mutillidae | Output: www-data | Vulnerability confirmed |
| 27 Aug 2026 12:30 | Toggled to Secure Mode | Mutillidae | Level 5 (Secure) | None |
| 27 Aug 2026 12:45 | Repeated injection Secure Mode | Mutillidae | BLOCKED | "Malicious characters not allowed" |
| 29 Aug 2026 16:00 | Reset DVWA Database | DVWA | Reset successful | None |
| 29 Aug 2026 16:05 | Reset Mutillidae Database | Mutillidae | Reset successful | None |
| 29 Aug 2026 16:10 | Verified clean snapshot | VirtualBox | Clean snapshot exists | None |
| 29 Aug 2026 16:15 | Confirmed no public exposure | Firefox (Host) | Connection failed | Isolation verified |

---

## Summary of Evidence Collected

| Evidence | Description |
|----------|-------------|
| E-1 to E-15 | Screenshots documenting all test steps |
| Evidence Register | Complete list of all evidence |
| Analysis Answers | 4 questions answered |
| This Activity Log | Timeline of all actions | Cleanup record

---

## Tools Used

- VirtualBox
- Kali Linux
- Firefox
- Curl
- Ping
- Nmap
- Sha256sum
- Nano
- Zip
