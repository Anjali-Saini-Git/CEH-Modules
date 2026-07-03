# Module 4 – Enumeration

## Topics Covered

### Enumeration Fundamentals
- What is Enumeration?
- Reconnaissance vs. Enumeration comparison
- Common enumeration types: DNS, SMTP, Service, SMB

### NetBIOS Enumeration
- NetBIOS services: Name Service (137/UDP), Datagram (138/UDP), Session (139/TCP)
- **Tools:** `nmap`, `nmblookup`, `enum4linux`, `smbclient`

### SMB Enumeration
- SMB protocol for file/print sharing
- Null session attacks and anonymous access
- **Tools:** `nmap -sC -p 139,445`, `smbclient -L //target -N`

### LDAP, SNMP & NTP
- **LDAP** (389/TCP): Directory access protocol
- **SNMP** (161/UDP): Network device monitoring
- **NTP** (123/UDP): Time synchronization

### SMTP Enumeration
- SMTP ports: 25 (default), 465 (SSL), 587 (STARTTLS)
- **Commands:** `nmap -p 25 --script smtp-*`, `nc`, `telnet`

### Key Findings from Lab
- Metasploitable2 target
- Anonymous SMB share access (`/tmp`)
- SMTP hostname disclosure
- Samba version fingerprinting

---

## 🛠️ Tools Practiced
- Nmap (service detection, scripts)
- nmblookup (NetBIOS name query)
- enum4linux (all-in-one SMB enumeration)
- smbclient (SMB client for share access)
- Netcat (`nc`) & Telnet
- Metasploitable2 (target VM)
