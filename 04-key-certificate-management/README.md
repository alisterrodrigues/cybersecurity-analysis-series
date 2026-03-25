# Key & Certificate Management Lifecycle
### Enterprise PKI & TLS Certificate Management Reference Architecture

**Prepared by:** Alister A. Rodrigues — Security Analyst, Obsidian SecureTech Solutions
**Context:** Enterprise Reference Architecture | **Date:** October 2024

---

## Overview

This reference architecture defines the complete lifecycle for cryptographic key and digital certificate management — from key generation through active usage, monitoring, compromise response, audit, and secure end-of-life disposal.

Technology choices are grounded in current standards: **ChaCha20 CSPRNG** for entropy, **HSM FIPS 186-5** for key generation, **RSA-4096** for asymmetric key pairs, **AES-256** for storage encryption, and **TLS 1.3** throughout. Each lifecycle stage is documented with both a narrative description and a process flowchart.

---

## Architecture Stages

| Stage | Key Elements |
|---|---|
| **Key Generation** | ChaCha20 CSPRNG → HSM (FIPS 186-5) → RSA-4096 key pair → AES-256 encrypted private key storage |
| **Certificate Generation** | CSR creation, CA identity verification, TLS 1.3 digital certificate issuance, certificate database storage |
| **Distribution** | Registered Authority intermediary, public key directory, secure certificate delivery |
| **Active Usage** | Deprecated TLS versions disabled, Perfect Forward Secrecy enabled, cipher suite hardening |
| **Monitoring & Renewal** | Centralized CMS with interval alerts (90/60/30 days), automated renewal pipeline, post-deployment testing |
| **Compromise Detection** | SIEM + IDS deployment, OCSP stapling, CRL maintenance, emergency revocation plan, MPA authorization |
| **Audit & Compliance** | Quarterly internal/external audits, automated compliance tooling, action plans, policy update cycle |
| **End of Life** | HSM secure key destruction, manual verification, AES-256 encrypted certificate archival |

---

## Connection to OCS

This reference architecture is the direct predecessor to the **PKI Architecture** in the [OCS Cybersecurity Strategy](https://github.com/alisterrodrigues/ocs-cybersecurity-strategy) (Fig 5 & 6) — which extends this lifecycle framework into a dual-path PKI with separate internal (Root CA → Intermediate CA) and external CA paths, tailored to OCS's split requirements for internal systems and public-facing e-commerce assets.

---

## Document

📄 `Key_and_Certificate_Management_Lifecycle_Reference_Architecture.pdf`

---

*© 2024 Obsidian SecureTech Solutions. All rights reserved.*
