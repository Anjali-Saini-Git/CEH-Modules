# Module 8 – Sniffing

## Overview

This module covers network sniffing techniques – capturing and analyzing data packets as they travel across a network. Includes practical labs on Wireshark analysis and ARP spoofing attacks.

---

## Key Concepts Covered

- **Sniffing Fundamentals** – What is packet sniffing, types of sniffing (passive vs active)
- **Promiscuous Mode** – How NICs capture all network traffic
- **TCP Handshake Analysis** – Capturing and analyzing SYN, SYN-ACK, ACK packets
- **HTTP Protocol Analysis** – Identifying plaintext credentials in transit
- **ARP Spoofing** – Man-in-the-Middle attack demonstration
- **MITM Attack Lifecycle** – Scan → Poison → Intercept → Capture → Maintain

---

## Practical Labs

### Lab 1: Wireshark Traffic Analysis
- Captured TCP three-way handshake
- Analyzed HTTP POST requests
- **Identified plaintext credentials** (username/password transmitted in clear text)

### Lab 2: ARP Spoofing MITM Attack
- **Environment:** Kali Linux (attacker), Windows (victim), Ettercap
- **Attack Execution:**
  - Scanned network to identify hosts
  - Poisoned ARP cache of victim and gateway
  - Intercepted HTTP POST request containing login credentials
  - Captured username (Anjali) and password (Admin) in plaintext
- **Post-Attack Evidence:** Duplicate MAC address detected – clear indicator of ARP spoofing

---

## Tools Practiced
- Wireshark
- Ettercap (GUI)
- ARP (Address Resolution Protocol)
- TCP/IP Protocol Suite

---

*All demonstrations are performed in isolated, authorized lab environments for educational purposes.*
