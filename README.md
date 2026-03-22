# 🛡️ AI Threat Model for Agentic Deployments

> A professional-grade security assessment of an AI-powered threat
> modeling agent — applying MAESTRO methodology, OWASP Agentic Top 10,
> and MITRE ATLAS to identify and prioritize risks in agentic LLM systems.

![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![Framework](https://img.shields.io/badge/Framework-MAESTRO-red)
![OWASP](https://img.shields.io/badge/OWASP-Agentic%20Top%2010-blue)
![MITRE](https://img.shields.io/badge/MITRE-ATLAS-orange)
![Type](https://img.shields.io/badge/Type-Security%20Research-purple)

---

## 📌 Project Overview

This project delivers a **consulting-grade AI threat model** for an
agentic system — a Claude-powered agent that autonomously performs
cybersecurity threat assessments. The project demonstrates how to
systematically identify, analyze, and prioritize security risks
in modern AI agent deployments.

This is the type of deliverable that **AI security consultants
produce for enterprise clients** — combining three industry
frameworks into a unified threat model.

---

## 🎯 Target System

**System:** AI Threat Modeling Agent
**Stack:** Claude (Anthropic) · LangGraph · Pinecone · Tavily API · AWS

An autonomous AI agent that:
- Accepts target system descriptions from security consultants
- Performs MAESTRO layer-by-layer threat analysis automatically
- Maps findings to OWASP Agentic Top 10 vulnerabilities
- Cross-references MITRE ATLAS adversarial techniques
- Generates and delivers professional consulting reports

---

## 🧰 Frameworks Used

| Framework | Purpose | Version |
|-----------|---------|---------|
| **MAESTRO** | Layer-by-layer AI threat modeling | 2025 |
| **OWASP Agentic Top 10** | Agentic vulnerability classification | 2025 |
| **MITRE ATLAS** | Adversarial ML technique mapping | v4.5 |
| **NIST AI RMF** | Risk management reference | 1.0 |

---

## 📁 Repository Structure
```
ai-threat-model-agentic-deployments/
│
├── 📄 README.md
│
├── 📂 architecture/
│   ├── agent-architecture.png     ← 7-layer architecture diagram
│   └── agent-architecture.xml     ← draw.io source file
│
├── 📂 threat-model/
│   ├── system-description.md      ← target system definition
│   └── maestro-analysis.md        ← full MAESTRO threat analysis
│
├── 📂 frameworks/
│   └── framework-mapping.md       ← OWASP + MITRE ATLAS mapping
│
└── 📂 report/
    └── AI_Threat_Model_Report.pdf ← final consulting report
```

---

## 🔍 Key Findings Summary

### Critical Risks Identified (P1 — Immediate Action Required)

| Risk ID | Threat | OWASP | MITRE ATLAS |
|---------|--------|-------|-------------|
| R-01 | Prompt Injection via user input | OAT-01 | AML.T0051 |
| R-02 | Indirect injection via web results | OAT-01 | AML.T0051.000 |
| R-03 | Trust escalation via tool chaining | OAT-03 | AML.T0007 |
| R-04 | Memory poisoning via vector DB | OAT-04 | AML.T0020 |
| R-05 | API key theft from context window | OAT-06 | AML.T0052 |
| R-06 | Supply chain compromise | OAT-10 | AML.T0010 |
| R-07 | Cross-session data leakage | OAT-06 | AML.T0037 |
| R-11 | Sandbox escape via generated code | OAT-05 | AML.T0052 |

### Risk Distribution
```
Critical  ████████████████████  11 threats
High      ████████████          8 threats  
Medium    ████                  4 threats
Low       ██                    3 threats
```

---

## 🏗️ Architecture Overview

The target system is analyzed across 7 architectural layers,
each with defined trust boundaries:

| Layer | Component | Trust Zone |
|-------|-----------|------------|
| L1 | User Interface / API Gateway | ⚠️ Untrusted |
| L2 | LangGraph Orchestrator | 🔶 Semi-trusted |
| L3 | Claude LLM Core | ✅ Trusted |
| L4 | Tool Executor (Web/Code/Email) | ⚠️ Untrusted |
| L5 | Pinecone Vector DB (Memory) | 🔶 Semi-trusted |
| L6 | External Data Sources | ⚠️ Untrusted |
| L7 | Output / Report Delivery | ⚠️ Untrusted |

> 📊 See full architecture diagram in `/architecture/`

---

## 🔬 Methodology

### Phase 1 — System Definition
Defined the target agentic system including technology stack,
trust boundaries, data flows, and attack surface.

### Phase 2 — MAESTRO Threat Modeling
Applied MAESTRO framework layer-by-layer across all 7
architectural layers. Identified 28 individual threats with
severity, likelihood, and risk scores.

### Phase 3 — OWASP Agentic Top 10 Assessment
Assessed the system against all 10 OWASP agentic vulnerability
categories. Result: **9 out of 10 categories confirmed vulnerable.**

### Phase 4 — MITRE ATLAS Mapping
Cross-referenced all identified threats against MITRE ATLAS
adversarial technique library. Mapped 15 unique ATLAS techniques
across 5 adversarial tactics.

### Phase 5 — Report Generation
Compiled findings into a professional consulting-grade report
with executive summary, risk register, and prioritized
remediation roadmap.

---

## 📊 OWASP Agentic Top 10 Results

| # | Vulnerability | Status | Severity |
|---|--------------|--------|----------|
| OAT-01 | Prompt Injection | 🔴 Vulnerable | Critical |
| OAT-02 | Insecure Output Handling | 🔴 Vulnerable | High |
| OAT-03 | Excessive Agency | 🔴 Vulnerable | Critical |
| OAT-04 | Memory Poisoning | 🔴 Vulnerable | Critical |
| OAT-05 | Insecure Plugin Design | 🟠 Partial | High |
| OAT-06 | Sensitive Info Disclosure | 🔴 Vulnerable | Critical |
| OAT-07 | Insufficient Logging | 🟠 Partial | High |
| OAT-08 | Model Denial of Service | 🟡 Low Risk | Medium |
| OAT-09 | Overreliance on LLM | 🔴 Vulnerable | High |
| OAT-10 | Agentic Supply Chain | 🔴 Vulnerable | Critical |

**Result: 8/10 fully vulnerable · 2/10 partially vulnerable**

---

## 🗡️ MITRE ATLAS Techniques Identified

| Tactic | Technique | ID |
|--------|-----------|-----|
| Initial Access | LLM Prompt Injection | AML.T0051 |
| Initial Access | Indirect Prompt Injection | AML.T0051.000 |
| Initial Access | Exploit Public-Facing Application | AML.T0040 |
| Initial Access | ML Supply Chain Compromise | AML.T0010 |
| Persistence | Poison Training Data | AML.T0020 |
| Persistence | Compromise ML Model | AML.T0031 |
| Collection | Data from ML Artifact | AML.T0037 |
| Credential Access | Unsecured Credentials | AML.T0052 |
| Discovery | Discover ML Artifacts | AML.T0007 |
| Exfiltration | Functional Extraction | AML.T0013 |
| Exfiltration | Exfil via ML Inference API | AML.T0040.002 |
| Defense Evasion | Evade ML Model | AML.T0015 |
| Impact | Denial of ML Service | AML.T0029 |
| Impact | Influence Operations | AML.T0019 |

---

## 🛠️ Top Security Recommendations

### 🔴 P1 — Immediate (Critical Risks)
1. Deploy prompt injection detection at all input boundaries
2. Enforce least privilege — explicit permission manifest per agent
3. Never store API keys in LLM context window
4. Implement namespace isolation in Pinecone per client session
5. Validate and sanitize all tool outputs before LLM ingestion
6. Pin all dependency versions — no auto-updates

### 🟠 P2 — Short Term (High Risks)
7. Implement agent identity tokens with cryptographic signing
8. Add human review gate before final report delivery
9. Deploy comprehensive structured audit logging
10. Ground all MITRE/CVE references against live authoritative APIs

### 🟡 P3 — Medium Term (Ongoing Hardening)
11. Conduct AI-SBOM audit of all integrated components
12. Red team exercise targeting agentic-specific attack vectors
13. Implement behavioral anomaly detection on agent action sequences

---

## 📚 References

- [MITRE ATLAS](https://atlas.mitre.org)
- [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
- [NIST AI Risk Management Framework](https://www.nist.gov/artificial-intelligence)
- [Anthropic Claude Safety Documentation](https://www.anthropic.com/safety)
- [LangGraph Documentation](https://langchain-ai.github.io/langgraph/)
- [MAESTRO Framework](https://github.com/maestro-security)

---

## 👤 Author

**Devansh Jaiswal**
Cybersecurity Analyst | AI Security Learner

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://linkedin.com/in/devansh-jaiswal-45410619b)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black)](https://github.com/Anshyaansh)

---

## ⚠️ Disclaimer

This threat model is produced for educational and research purposes.
All attack scenarios are hypothetical and intended to improve
security posture. No real systems were targeted or compromised.

---

*This project demonstrates professional AI security methodology
applicable to real-world agentic deployments.*
