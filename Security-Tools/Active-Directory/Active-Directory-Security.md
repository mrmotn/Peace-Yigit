# 🏢 Active Directory Security

> Active Directory is the backbone of enterprise identity management.  
> Most corporate breaches involve AD misconfigurations or abuse.

This document outlines my understanding of AD from a security perspective.

---

## 🎯 Why AD Matters

Active Directory controls:
- User and group identity
- Authentication and authorization
- Trust relationships across domains
- Resource access and policies

Compromise of AD often leads to **full network compromise**.

---

## 🧱 Core AD Concepts

- Domains, trees, and forests
- Organizational Units (OUs)
- Users, groups, and permissions
- Authentication protocols: Kerberos, NTLM
- Group Policy Objects (GPOs)
- Trust relationships between domains

---

## 🧠 Security Perspective

I approach AD security by asking:
- Who has excessive privileges?
- Where are implicit trust boundaries?
- Which accounts are outdated or unmonitored?
- How are sensitive groups protected?

---

## 🛡️ Defensive Awareness

Key AD security measures I study:
- Privilege auditing (admin, service accounts)
- Proper delegation and separation of duties
- Monitoring account usage and failed logins
- Detecting lateral movement attempts
- Hardened GPOs and endpoint policies

---

## 📚 Advanced Topics I Study

- Kerberos ticketing (TGT, TGS)
- AD enumeration techniques (lab only)
- Common misconfigurations in trusts
- Logging and SIEM integration for AD events
- Service Principal Names (SPNs) and their implications

---

## 📌 Conclusion

Active Directory security is about **identity and trust control**.  
If identity fails, everything else in the enterprise network becomes vulnerable.  
Understanding AD deeply is critical for both red-team and blue-team perspectives.
