## Home Lab Architecture

This document explains how I designed and isolated my personal cybersecurity home lab.
The goal is not only to use security tools, but to build a realistic, safe, and reproducible environment similar to real-world infrastructures.

## 🖥️ Hypervisor Choice

Hypervisor Used: VirtualBox
(VMware / Proxmox can be used with the same principles)

## Why VirtualBox?

Free and open-source

Stable for personal labs

Strong networking options (NAT, Host-only, Internal Network)

Easy snapshot and rollback support

Snapshots allow me to safely test configurations and revert systems after experiments.

## 🌐 Networking Architecture
Network Types Used
Network Type	Purpose	Reason
NAT	Internet access	Controlled outbound connectivity
Host-only	Isolated lab network	No exposure to real network
Internal Network	VM-to-VM communication	Simulates internal corporate LAN
NAT vs Host-only (Key Difference)

## NAT Network

VM can access the internet

Host and LAN devices are protected

Used for updates and package installs

Host-only Network

Completely isolated from the internet

Only host ↔ VM communication

Ideal for attack/defense simulations

## 📌 Isolation Reasoning:
Security testing tools should never interact with real external systems.
Host-only networking ensures all traffic stays inside the lab.

## 🧱 Defensive Layer

To better simulate real-world environments, I added a basic defensive layer.

## 🔥 Firewall (pfSense)

Role: Network perimeter security

Placement:

pfSense VM sits between attacker and target machines

Acts as a gateway and traffic controller

## Why pfSense?

Open-source and widely used in enterprise environments

Supports:

Firewall rules

NAT

Logging

IDS/IPS integration (Snort / Suricata)

## What I configured:

Basic inbound/outbound rules

Network segmentation

Logging of blocked connections

This setup helps me understand how attacks look from the defender’s perspective, not just the attacker’s.

## 📊 Log Monitoring

Purpose: Visibility and detection

Tools (example):

pfSense built-in logs

System logs from Linux VMs

## What I observe:

Blocked connection attempts

Port scan patterns

Traffic flow between internal networks

Learning how logs look during scans is critical for blue-team awareness.

## 🧠 Security Mindset

This lab is intentionally:

Isolated

Reproducible

Defensive-aware

Rather than only running tools, I focus on:

How traffic flows

Where detection happens

How misconfigurations expose systems

This approach reflects real-world security operations.

## 📐 High-Level Architecture
[ Attacker VM ]
       |
       | (Internal Network)
       |
[ pfSense Firewall ]
       |
       | (Host-only Network)
       |
[ Target VMs ]

## 📌 Conclusion

This home lab demonstrates:

Understanding of virtualization

Network isolation principles

Basic defensive security concepts

Safe and ethical testing practices

Building and maintaining my own lab strengthens both my technical skills and security mindset.
