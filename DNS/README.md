# 🛰️ Identify DNS Zone Transfer Vulnerabilities

This lab demonstrates how DNS zone transfers can expose sensitive network data if improperly configured.

---

## 🔍 Objective

- Add a DNS CNAME record
- Test a DNS zone transfer
- Intentionally misconfigure the DNS server
- Perform a successful zone transfer
- Analyze the leaked DNS data

---

## 🧪 Environment

- **ACIDC01** – Windows Server 2022 (DNS Server)
- **ACIKALI** – Kali Purple Linux

---

## 🧱 Task 1 – Add a CNAME Record

We created an alias `testing.aciplab.com` pointing to `aciplabtestingserver.com`.

![DNS Manager](./1-DNSManager.png)  
![Creating CNAME](./2-CreateCNAME.png)  
![CNAME Record Added](./3-ViewCNAME.png)

---

## ❌ Task 2 – Attempt Zone Transfer (Should Fail)

We attempted to run a DNS zone transfer from ACIKALI using:

```bash
sudo dig axfr @192.168.0.1 aciplab.com

Result:Transfer failed (expected)