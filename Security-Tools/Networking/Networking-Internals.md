# 🌐 Networking Internals

> Understanding networking is foundational to cybersecurity.  
> Tools are meaningless without knowing how data actually moves.

This document summarizes my understanding of core networking concepts from a security perspective.

---

## 🎯 Why Networking Matters

Every security issue exists because:
- Data is transmitted
- Protocols make assumptions
- Trust boundaries are crossed

Understanding networking allows me to:
- Interpret scan results correctly
- Identify misconfigurations
- Think like both attacker and defender

---

## 🧱 OSI & TCP/IP Models

### OSI Model (Conceptual)
1. Physical
2. Data Link
3. Network
4. Transport
5. Session
6. Presentation
7. Application

### TCP/IP Model (Practical)
- Network Interface
- Internet
- Transport
- Application

Security issues often occur at **layer boundaries**.

---

## 🔄 Core Protocols

### TCP vs UDP
- TCP: Reliable, stateful, slower
- UDP: Fast, stateless, less predictable

### IP
- Routing and addressing
- Trust assumptions in internal networks

### DNS
- Name resolution
- Frequent source of misconfiguration and information leakage

### HTTP / HTTPS
- Stateless communication
- Headers and methods define behavior

---

## 🧠 Security Perspective

Key questions I always ask:
- Is this traffic encrypted?
- Is authentication implicit or explicit?
- Where does trust begin and end?
- What happens if input is unexpected?

---

## 📌 Conclusion

Networking knowledge:
- Improves tool accuracy
- Reduces false assumptions
- Strengthens root-cause analysis

Security starts with understanding the wire.
