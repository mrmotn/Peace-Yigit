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
#What is Nmap?

Nmap (Network Mapper) is an open-source tool used for network discovery and security auditing. It helps identify hosts, open ports, services, and basic system information on a network.

## What can you do with Nmap?

Discover live hosts on a network

Identify open ports

Detect running services

Perform basic operating system fingerprinting

Build network security awareness


## Installation
Linux
sudo apt install nmap

## macOS
brew install nmap

Windows

Download the official installer from: https://nmap.org

## 🔍 Basic Usage
Scan a single target
nmap 192.168.1.1

## Scan a domain
nmap example.com

## 🌐 Network Discovery
Find active hosts in a subnet
nmap -sn 192.168.1.0/24


-sn performs host discovery only (no port scan)

🚪 Port Scanning
Scan most common ports
nmap --top-ports 100 target_ip

Scan all TCP ports (slow)
nmap -p- target_ip

Scan specific ports
nmap -p 22,80,443 target_ip

## 🔎 Service & Version Detection
nmap -sV target_ip


This detects:

Running services

Approximate service versions

💻 Operating System Detection (Estimated)
nmap -O target_ip


OS detection provides an estimate, not guaranteed accuracy.

📜 Nmap Scripting Engine (NSE)

NSE allows automated and security-focused scripts.

Default safe scripts
nmap -sC target_ip

Vulnerability category scripts
nmap --script vuln target_ip


Use scripts only on authorized targets.

## 📁 Output & Reporting
Normal output
nmap -oN scan.txt target_ip

XML output (for reports)
nmap -oX scan.xml target_ip

## 🧪 Safe Learning Environments

Practice Nmap legally using:

Local Virtual Machines (VirtualBox + Kali Linux)

TryHackMe (Beginner rooms)

Hack The Box (Academy)

## 📚 Learning Tips

Learn networking fundamentals first

Understand what each command does

Focus on interpreting scan results

Share anonymized lab results on GitHub



