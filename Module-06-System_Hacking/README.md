# Module 6 – System Hacking

## Topics Covered

### System Hacking Lifecycle
- Footprinting → Scanning → Enumeration → Vulnerability Analysis → **Gaining Access** → **Maintaining Access** → **Clearing Tracks/Logs**

### Windows Password Cracking Lab
- **SAM File**: Windows password database
- **Critical Files**: SAM (hashes), SYSTEM (boot key), SECURITY (cached credentials)
- **NTLM**: Authentication protocol that stores hashes in SAM database
- **Full Attack Chain**:
  1. Dump registry hives 
  2. Transfer files to Kali Linux
  3. Extract hashes 
  4. Crack with John the Ripper 
  5. Found password: **User@123**

### Linux Password Cracking
- **Shadow File**– stores password hashes
- Crack with John the Ripper

### Metasploit Framework – Complete Attack Chain

| Step | Purpose |
|------|-------------|
| Create Payload | Generate malicious executable |
| Set up Listener | Wait for incoming connection |
| Deliver Payload | Transfer to target |
| Connection Established | Meterpreter shell active |
| Privilege Escalation | USER → SYSTEM |
| Process Migration | Move to legitimate process (svchost.exe) |
| Credential Dumping | Mimikatz extracts NTLM hash |
| Pass-the-Hash | Authenticate using hash only |
| Keylogging | Captured: User@123 |
| Persistence | Survives reboots |
| Covering Tracks | Clears Windows event logs |

### Key Achievements
- Initial Access – Reverse Meterpreter shell
- Privilege Escalation – USER → SYSTEM
- Credential Access – NTLM hash extracted
- Password Recovery – User@123 (keylogging)
- Persistence – WindowsDefender service installed
- Stealth & Evasion – Process migrated, logs cleared

## Tools Practiced
- John the Ripper
- Metasploit Framework (msfconsole, msfvenom, Meterpreter)
- Mimikatz
- Impacket (secretsdump)
- Windows Registry (reg save)
- Keylogging, Persistence, Pass-the-Hash
