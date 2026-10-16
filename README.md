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

Varnish Cache VCL / varnishd / Hitch configuration hardening auditor

---

## ✨ Features

- Stdlib VCL parser — comments, long strings {"..."}, include "..."; following with loop detection, backend / probe / acl blocks, sub bodies (concatenated like varnishd)
- varnishd command line — /etc/default/varnish DAEMON_OPTS, /etc/sysconfig/varnish, varnish.params, systemd ExecStart + drop-ins: -a -T -S -M -f -s -j -u -n -p parameters
- Management CLI exposure (-T 0.0.0.0 / public), -S secret missing / world-readable / weak, jail & privilege checks
- VCL logic — PURGE / BAN without ACL, wide purge ACLs, return(pipe) for all, builtin bypass caching Authorization and Cookie requests, Set-Cookie TTL, hash_data(host), X-Forwarded-Host poisoning, XFF trust, std.log credentials, synthetic error leaks, ESI, inline C, backend timeouts
- varnishncsa logging and Hitch TLS terminator (hitch.conf)
- Secrets masked everywhere; --root offline trees; CWE + MITRE
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Self-test --demo, CI gates --fail-on / --min-severity

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OVarnishX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
