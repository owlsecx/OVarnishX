# 🦉 OVarnishX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OWeb-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OVarnishX** — Varnish Cache Configuration Hardening Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview


OVarnishX is an offline, read-only Varnish Cache configuration auditor that parses VCL files and systemd/init service arguments with stdlib-only parsers. It reviews the admin/CLI interface and secret-file exposure, ACL definitions for PURGE/BAN, backend TLS, header handling and cache-poisoning risks. Findings are mapped to CWE and MITRE ATT&CK, scored and graded, and exported as TXT, Markdown, JSON, CSV or SARIF.

---

## ✨ Features


- VCL parser (vcl_recv/backend/deliver subs, ACLs, backends, includes) plus systemd/init varnishd args
- Admin interface checks: -T bind address, -S secret file presence/perms and management exposure
- PURGE/BAN ACL review, client.ip trust, X-Forwarded-For handling and cache-poisoning vectors
- Backend security: TLS to origin, host-header validation and health-probe exposure
- Header hygiene (Set-Cookie caching, Vary, sensitive header leakage) and VMOD risk notes
- CWE+ATT&CK mapping, offline --root trees, score/grade and TXT/MD/JSON/CSV/SARIF export

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage


```bash
./OVarnishX --scan -f sarif -o varnish.sarif
./OVarnishX --vcl /etc/varnish/default.vcl --service /etc/systemd/system/varnish.service
./OVarnishX -r /mnt/image --fail-on high --json
./OVarnishX --demo
./OVarnishX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
