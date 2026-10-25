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

OBindX is an offline, read-only auditor for DNS server configuration, covering BIND 9, PowerDNS Authoritative and Recursor, Unbound and Knot Resolver. A recursive parser for the named.conf dialect plus product-specific analysers flag open resolvers, AXFR-to-any, exposed controls, DNSSEC gaps and weak TSIG, and a zone-file analyzer reviews SOA timers, NS redundancy and signing. Findings map to CWE and MITRE ATT&CK with a 0–100 score, A+…F grade and hardened templates, and it never queries DNS.

---

## ✨ Features

- Recursive named.conf parser plus PowerDNS, Unbound and Knot Resolver auditors
- BIND checks: open resolver, AXFR to any, rndc exposure, DNSSEC, RRL, dynamic update
- Zone-file analysis: SOA timers, NS redundancy, unsigned zones, weak DNSKEY algorithms
- Secrets masked; auto-discovery under --root or on the live system
- CWE + MITRE ATT&CK mapping, 0–100 score and A+…F grade
- Hardened templates per server and export TXT/MD/JSON/CSV/SARIF

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OBindX --scan
./OBindX --bind /etc/bind/named.conf --format sarif -o report.sarif --fail-on high
./OBindX --zone db.example.com --signed
./OBindX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
