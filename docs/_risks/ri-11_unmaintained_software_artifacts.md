---
sequence: 11
title: Unmaintained Software Artifact
layout: risk
doc-status: Draft
type: SEC
nist-sp-800-53r5_references:
  - SI‑2 – Flaw Remediation - Requires timely identification, reporting, and correction of software flaws.

  - RA‑5 – Vulnerability Monitoring and Scanning - Mandates scanning for vulnerabilities and tracking remediation.

  - SI‑7 – Software, Firmware, and Information Integrity - Ensures protection against unauthorized modification.

  - CM‑7 – Least Functionality - Reduces attack surface by limiting unnecessary components.

  - SR‑3 – Supply Chain Controls - Addresses risks from unsupported or abandoned third‑party components.

ffiec-itbooklets_references:
  
related_risks:
  - ri-4   # Vulnerable Software in Production
  - ri-2   # Software Supply Chain Vulnerability
---


## Summary

Unmaintained software artifacts are software components, systems, or deliverables that are no longer actively supported, updated, or monitored by their original maintainers or responsible teams. This poses risks spanning security, operations, compliance, and business continuity.
## Description

Unmaintained software artifacts are more than just “old code”—they represent blind spots in an organization’s technology ecosystem. These artifacts can include AI Models, libraries, containers, build scripts, APIs, infrastructure-as-code templates, CI/CD pipelines, or even entire applications that are still in use but no longer have an active owner. Because they fall outside regular maintenance cycles, they tend to drift away from current security, compatibility, and compliance standards.

- **Unpatched Vulnerabilities** — Known vulnerabilities (CVEs) remain unpatched, and newly discovered ones are never addressed.
- **Regulatory Compliance is unmet** — Regulatory requirements (e.g., patching SLAs, encryption standards, auditability) may no longer be met.
- **RepoJacking** — Attackers compromise an abandoned artifact repository and replaces the code with something malicious

### Consequences



## Links
* https://owasp.org/Top10/2025/A03_2025-Software_Supply_Chain_Failures/
