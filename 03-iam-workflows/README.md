# IAM Workflow Design
### Joiner, Mover, Leaver & Entitlement Review — Enterprise IAM Framework

**Prepared by:** Alister A. Rodrigues — Security Analyst, Obsidian SecureTech Solutions
**Context:** Enterprise Reference Architecture | **Date:** October 2024

---

## Overview

This document defines a complete **Identity & Access Management workflow framework** covering the full employee lifecycle — onboarding, role transitions, offboarding, and periodic entitlement reviews. Each workflow is accompanied by a detailed process diagram and design logic explaining the security rationale behind each step.

Built around three core principles: **least privilege**, **separation of duties**, and **audit-ready access logging** — ensuring both operational efficiency and compliance with ISO/IEC 27001, GDPR, and NIST SP 800-53.

---

## Workflows Covered

**Joiners — Onboarding**
HR-triggered IAM provisioning, NDA execution, birthright RBAC assignment, managerial approval gate, security awareness training, and AUP sign-off. Access provisioning split by criticality — automated for standard systems, manager-approved for sensitive systems.

**Movers — Role Transitions**
Promotion and transfer handling — automated flagging of irrelevant permissions, RBAC-based new access assignment, managerial review, probationary period re-validation, and full audit logging of all access modifications.

**Leavers — Offboarding**
Immediate access freeze on last working day, complete automated deprovisioning, data and account ownership transfer, exit interview covering NDA obligations, device recovery, and compliance logging.

**Entitlement Reviews**
Quarterly scheduled reviews — manager-led access validation combined with security team audit, flagging and remediation of excessive or outdated permissions, audit records maintained for regulatory compliance.

---

## Connection to OCS

This workflow framework is the direct foundation for the **IAM Reference Architecture** in the [OCS Cybersecurity Strategy](https://github.com/alisterrodrigues/ocs-cybersecurity-strategy) (Fig 3) — which layers these same Joiner/Mover/Leaver flows into a three-tier architecture covering the Identity Management Layer, Access Control Layer, and Governance Layer at enterprise scale.

---

## Document

📄 [`IAM_Workflows_Joiner_Mover_Leaver_Entitlement_Review.pdf`](https://github.com/alisterrodrigues/cybersecurity-analysis-series/blob/main/03-iam-workflows/Identity%20%26%20Access%20Management%20(IAM)%20Workflows%20for%20Organizational%20Security%20%26%20Compliance.pdf)

---

*© 2024 Obsidian SecureTech Solutions. All rights reserved.*
