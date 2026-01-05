# Nmap Practical Guide
This guide covers my most used Nmap commands during penetration testing engagements.

## 1. Simple Scans
* **Scan a single target:** `nmap 10.10.10.1`
* **Scan multiple targets:** `nmap 10.10.10.1 10.10.10.2`

## 2. Advanced Discovery
* **Service Version Detection:** `nmap -sV <target>` (Helps identify what software is running on a port)
* **Default Script Scan:** `nmap -sC <target>` (Uses Nmap scripts to find common vulnerabilities)
* **Aggressive Scan:** `nmap -A <target>` (OS detection, version detection, script scanning, and traceroute)

---
