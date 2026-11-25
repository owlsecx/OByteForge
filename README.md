# 🦉 OByteForge

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-Security-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0-cyan?style=flat-square"/>
</p>

> **OByteForge** — part of the OwlSec Toolkit.

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OByteForge brings the everyday binary-analysis tasks together in one tool. It identifies file types, shows an interactive hex view, extracts strings and IOCs, measures entropy and compares binaries. It can also patch bytes, carve embedded files, brute-force XOR keys and check the hardening flags of ELF, PE and Mach-O executables.

---

## ✨ Features

- File inspection: 60+ type signatures, MD5/SHA-1/SHA-256 and an entropy verdict
- Interactive hex viewer and search by hex (with ?? wildcards), ASCII, UTF-16LE or regex
- String extraction (ASCII + UTF-16LE) with IOC tagging: URLs, IPs, emails, paths, registry keys, base64
- Per-block entropy map and ent-style statistics (chi-square, serial correlation, Monte-Carlo π)
- Binary diff, byte patching with .bak backup, range extraction and signature-based file carving
- XOR with a key or single-byte brute force, ELF/PE/Mach-O analysis with checksec-style hardening flags, and export to C/Python/Go arrays

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OByteForge                                 # interactive menu
./OByteForge --info sample.bin
./OByteForge --strings sample.bin --ioc
./OByteForge --carve firmware.img --out carved/
./OByteForge --binary /usr/bin/ssh
```

Run `./OByteForge --help` for the full list of options.

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, the Go toolchain version it was built with, and every bundled
  component with its exact version and license. Feed it to Grype, Trivy or
  Dependency-Track to audit our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
