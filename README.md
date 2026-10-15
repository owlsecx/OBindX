# 🦉 OBindX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-ONetwork-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OBindX** — Offline DNS Server Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Offline BIND / PowerDNS / Unbound / Knot Resolver configuration auditor

---

## ✨ Features

- Recursive brace/statement parser for the BIND 9 named.conf dialect (comments, quoted strings, nested blocks, address-match lists, include resolution)
- BIND checks — open resolver (amplification), AXFR to any, rndc controls exposure, version / hostname disclosure, DNSSEC validation, RRL absent, query-source fixed port, dynamic update to any, weak TSIG algorithms, world-readable key files
- Zone file analyzer — SOA timers, NS redundancy, unsigned zones where policy requires DNSSEC, weak DNSKEY algorithms, RFC1918 leaks, wildcards
- PowerDNS Authoritative (pdns.conf) and Recursor (recursor.conf) auditors — API keys, webserver ACLs, AXFR, dynamic updates, backend passwords (masked)
- Unbound auditor — access-control, harden-*, QNAME minimisation, aggressive NSEC, permissive validation, remote-control without certificates
- Knot Resolver (kresd.conf) auditor — listeners, views/ACLs, trust anchors, management endpoints
- Auto-discovery under a root directory (--root/--scan)
- CWE + MITRE ATT&CK mapping, 0–100 score, A+…F grade
- Hardened configuration templates for every server
- Exports TXT/MD/JSON/CSV/SARIF; --demo self-test
- Strictly read-only and offline — never queries DNS

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OBindX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
