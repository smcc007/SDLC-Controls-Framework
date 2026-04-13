---
sequence: 11
title: Unmaintained Software Artifact
layout: risk
doc-status: Draft
type: SEC
nist-sp-800-53r5_references:
SI‑2 – Flaw Remediation - Requires timely identification, reporting, and correction of software flaws.

RA‑5 – Vulnerability Monitoring and Scanning - Mandates scanning for vulnerabilities and tracking remediation.

SI‑7 – Software, Firmware, and Information Integrity - Ensures protection against unauthorized modification.

CM‑7 – Least Functionality - Reduces attack surface by limiting unnecessary components.

SR‑3 – Supply Chain Controls - Addresses risks from unsupported or abandoned third‑party components.

ffiec-itbooklets_references:
  
related_risks:
  - ri-4   # Vulnerable Software in Production
  - ri-2   # Software Supply Chain Vulnerability
---


## Summary

Unmaintained software artifacts are software components, systems, or deliverables that are no longer actively supported, updated, or monitored by their original maintainers or responsible teams. This poses risks spanning security, operations, compliance, and business continuity.
## Description

While unauthorised system access (ri-6) concerns access governance failures, environment breach describes a more severe state: the attacker has moved beyond access to achieve persistent execution capability within the production environment, running their own code alongside legitimate services. This can result from exploitation of vulnerabilities in exposed services, compromised container orchestration platforms, misconfigured cloud IAM policies, or abuse of legitimate deployment mechanisms. The attacker operates within the organisation's own infrastructure, making detection significantly harder and the potential impact far greater.

- **Unauthorised container or workload deployment** — Attackers deploying their own containers, serverless functions, or processes within the organisation's orchestration platform (e.g., Kubernetes, ECS)
- **Compromised orchestration plane** — Exploitation of container orchestration APIs or management interfaces to schedule and run attacker-controlled workloads alongside legitimate services
- **Cryptojacking and resource abuse** — Attackers deploying cryptocurrency mining workloads or using compromised infrastructure for computational tasks, consuming resources and increasing costs
- **Staging ground for further attacks** — Using the breached environment as a launch point for lateral movement into other internal systems, data stores, or connected partner networks
- **Persistent backdoor deployment** — Installing persistent access mechanisms such as reverse shells, web shells, or rogue services that survive routine maintenance and restarts

### Consequences

* **Deep infrastructure access** — An attacker running workloads in production has broad access to the environment, potentially including network access to databases, internal APIs, secret stores, and adjacent systems that are not directly exposed to the internet.
* **Customer data theft at scale** — With operational presence in the production environment, attackers can systematically exfiltrate customer data, transaction records, and financial information over extended periods while evading perimeter-based detection.
* **Financial losses from resource abuse** — Unauthorised workloads — particularly cryptomining operations — can generate significant unexpected cloud computing costs before detection, directly impacting operational budgets.
* **Regulatory escalation** — An environment breach represents a fundamental control failure. Regulators will treat the ability of an external attacker to run workloads in a financial institution's production environment as a critical finding, triggering mandatory incident reporting under DORA Article 17, PCI DSS Requirement 12.10, and GLBA breach notification obligations.
* **Supply chain risk to customers** — Attacker-controlled workloads running within the institution's infrastructure can potentially intercept, modify, or inject data into legitimate business processes, affecting downstream customers and partners.
* **Prolonged and costly incident response** — Detecting and eradicating an attacker with operational presence requires thorough forensic investigation of all running workloads, comprehensive review of deployment history, and potentially rebuilding affected infrastructure from known-good state.
* **Severe reputational damage** — Disclosure that an external attacker was running their own workloads inside a financial institution's production environment represents a serious breach of trust that can significantly damage the institution's standing with customers, partners, and regulators.

## Links
* https://owasp.org/Top10/2025/A03_2025-Software_Supply_Chain_Failures/
