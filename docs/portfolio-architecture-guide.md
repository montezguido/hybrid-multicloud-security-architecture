# Architecture Portfolio — Reviewer Guide

This guide distinguishes three **sanitized WGU-derived design case studies** from separately developed, executable projects. The three architecture repositories preserve different decisions and business contexts; none contains a deployed cloud environment or runnable implementation.

## Why retain three case studies?

| Case study | Distinct engineering question | Primary deliverable | What it demonstrates | What it does *not* establish |
|---|---|---|---|---|
| **[Hybrid & Multicloud Security](../README.md)** — primary | How should a merged on-premises, AWS, Azure, and Google Cloud environment reduce immediate security risk and move toward Zero Trust? | Comparison of centralized telemetry/connectivity versus identity-centric Zero Trust, with a phased recommendation | Threat-oriented design, security control selection, tradeoffs, migration sequencing | Implemented identity federation, deployed CSPM, security findings, or a production assessment |
| **[Healthcare Hybrid Cloud Modernization](https://github.com/montezguido/healthcare-hybrid-cloud-modernization)** — supporting | Which healthcare workloads should stay on-premises versus migrate to cloud, and how should the transition be governed? | Workload-placement matrix, hybrid reference architecture, five-phase modernization plan | Dependency awareness, latency/data locality, compatibility, migration risk, operational governance | Running Kubernetes clusters, completed migration, quantified operational improvements |
| **[AI-Enhanced Network Operations & Security](https://github.com/montezguido/ai-enhanced-network-operations-security)** — supporting | How should an AI-assisted multi-site network proposal be assessed and monitored by engineers? | Architecture refinement method, illustrative KPIs, capacity/cost analysis | Human review of AI output, segmentation strategy, monitoring design, KPI selection | Deployed AI detection, measured throughput gains, achieved savings, running automation |

The three studies overlap on segmentation, logging, security, and automation because those are common cross-cutting requirements. Their distinct value is in the **decision under review**, rather than repeated claims about the technologies listed.

**Original WGU source checks:** The [E028 modernization evidence map](https://github.com/montezguido/healthcare-hybrid-cloud-modernization/blob/main/docs/e028-design-evidence.md) summarizes the original hybrid-cloud proposal. The [E026 AI architecture evidence map](https://github.com/montezguido/ai-enhanced-network-operations-security/blob/main/docs/e026-design-evidence.md) summarizes the original network presentation. Both distinguish documented design decisions from production deployment. The academic sources themselves remain private.

## Primary security decision: why a phased approach?

The security case study evaluates two alternatives:

1. **Secure connectivity and centralized telemetry first.** Improves early visibility across legacy on-premises and multicloud environments while retaining compatibility with existing systems. Main risks: incomplete log coverage, cross-cloud ingestion cost, and limited initial identity modernization.
2. **Identity-centric Zero Trust and posture management.** Provides stronger granular authorization and continuous posture verification but requires more coordination, policy engineering, and legacy application adaptation.

**Case-study recommendation:** establish reliable security telemetry and controlled hybrid connectivity, then phase in identity federation, least-privilege reviews, conditional access, and more granular segmentation. This is a documented architectural recommendation, not proof that either environment was deployed.

## Evidence map: design versus executable proof

| Evidence type | Where to look | Level of verification |
|---|---|---|
| Security decisions and tradeoffs | [Security architecture README](../README.md) | Documented analysis; no live configuration |
| Hybrid modernization and workload placement | [Healthcare case study](https://github.com/montezguido/healthcare-hybrid-cloud-modernization) | Documented design; no migrated workloads |
| AI-assisted network design and projected KPIs | [AI network operations case study](https://github.com/montezguido/ai-enhanced-network-operations-security) | Documented methodology; financial/performance numbers are scenario assumptions |
| Independently implemented Python source and CI | [Network Reliability Lab](https://github.com/montezguido/network-reliability-lab) | Automated unit tests and loopback HTTP lifecycle; not a cloud deployment |
| Independently implemented network access-model tests | [Hybrid Network Capstone portfolio examples](https://github.com/montezguido/hybrid-cloud-network-engineering-capstone) | Synthetic model tests plus historical capstone case study |
| Independently implemented AWS Terraform reference | [AWS IaaS/Linux reference](https://github.com/montezguido/aws-iaas-linux-infrastructure/tree/main/reference) | Mocked Terraform tests and Linux bootstrap syntax; not applied to AWS |
| Independently implemented DNS incident model | [Python Network Automation](https://github.com/montezguido/network-automation-incident-response) | Offline Python incident simulation and CI; no real ticket integrations |
| Independently implemented diagnostic classification | [Enterprise Troubleshooting](https://github.com/montezguido/enterprise-network-troubleshooting) | Offline Python triage and CI; not a live network diagnosis |

## Suggested recruiter review path

For **Cloud Engineer / Cloud Operations / SRE** openings, review the code-backed projects above first. Use these architecture cases to evaluate how technical decisions are justified, especially around access boundaries, hybrid-cloud modernization, and operations tradeoffs.

For **Cloud Security Engineer** openings, review the security comparison first, then the hybrid capstone's source-aware policy model and AWS infrastructure guardrails.

## Publication boundaries

Original WGU submissions, institutional prompts, grading materials, student identifiers, credentials, restricted network configurations, and assessment screenshots are not included. Architecture descriptions here are sanitized professional case studies. The three supporting case studies should never be presented as separately deployed applications, production AI operations platforms, or compliance certifications.

This guide is a **navigation and evidence-honesty improvement**. It does not introduce new executable code or assert new test results.
