# 🔐 Cryptography Fundamentals

> Cryptography is not about hiding data —  
> it is about **controlling trust, integrity, and confidentiality**.

This document summarizes my understanding of cryptography from a cybersecurity perspective.

---

## 🎯 Why Cryptography Matters

Modern security relies heavily on cryptography to:
- Protect sensitive data
- Ensure secure communication
- Verify identity
- Maintain data integrity

Most real-world security failures are not due to broken algorithms, but due to **incorrect usage or implementation**.

---

## 🧱 Core Goals of Cryptography

Cryptography aims to provide:

- **Confidentiality:** Only authorized parties can read the data  
- **Integrity:** Data cannot be altered without detection  
- **Authentication:** Verifying identity  
- **Non-repudiation:** Actions cannot be denied later  

Understanding which goal applies in which context is critical.

---

## 🔑 Symmetric Cryptography

### Concept
- Same key is used for encryption and decryption
- Fast and efficient
- Requires secure key distribution

### Common Use Cases
- Disk encryption
- Secure file storage
- Encrypted network sessions (as part of hybrid systems)

### Security Considerations
- Key management is the biggest risk
- Weak keys or reuse leads to compromise

---

## 🔐 Asymmetric Cryptography

### Concept
- Uses a public/private key pair
- Solves key distribution problems
- Slower than symmetric encryption

### Common Use Cases
- Secure key exchange
- Digital signatures
- Authentication systems

### Security Considerations
- Private key protection is critical
- Trust models (PKI) must be understood

---

## 🔄 Hash Functions

### Purpose
- One-way transformation
- Data integrity verification
- Password storage

### Properties
- Deterministic
- Collision resistant
- Pre-image resistant

### Security Perspective
- Hashing ≠ encryption
- Salting is essential for passwords
- Weak hashes lead to credential compromise

---

## 🧠 Cryptography in Practice

Real-world systems combine multiple cryptographic components:
- Symmetric encryption for performance
- Asymmetric encryption for key exchange
- Hashing for integrity and authentication

This layered approach is known as **hybrid cryptography**.

---

## 🛡️ Common Cryptographic Mistakes

- Rolling custom crypto
- Hardcoded keys
- Weak random number generation
- Reusing keys across contexts
- Incorrect certificate validation

Most vulnerabilities stem from **design or implementation errors**, not broken math.

---

## 🔍 Cryptography from a Security Testing Perspective

When assessing cryptographic usage, I focus on:
- Algorithm choice
- Key length and rotation
- Proper use of TLS
- Certificate handling
- Password storage mechanisms

The goal is to identify **misuse**, not to break encryption.

---

## 📚 Advanced Cryptography Topics I Study

- TLS handshake and certificate chains
- Public Key Infrastructure (PKI)
- Password-based key derivation functions
- Token-based authentication (JWT)
- Cryptographic randomness

---

## ⚖️ Ethics & Responsibility

Cryptography protects:
- Privacy
- Trust
- Digital safety

Understanding cryptography comes with responsibility.  
It must be used to **secure systems**, not undermine trust.

---

## 📌 Conclusion

Cryptography is a cornerstone of cybersecurity.

Strong algorithms do not guarantee security —  
**correct implementation and key management do**.

> Secure systems fail when cryptography is misunderstood, not when it is too weak.

