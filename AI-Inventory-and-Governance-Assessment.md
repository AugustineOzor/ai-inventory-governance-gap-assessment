# AI Inventory and Governance Assessment

**Portfolio purpose:** A practical demonstration of AI inventory management, risk categorisation, governance control assessment, gap analysis, and executive reporting.

**Scope:** Six illustrative AI systems used by a fictional mid-sized organisation. Replace the sample entries with verified organisational data before operational use.

**Deliverables:**
1. AI Inventory Register
2. AI Risk Register
3. Governance Gap Assessment
4. Executive Summary Dashboard

**Framework alignment:** EU AI Act risk-based approach; ISO/IEC 42001 AI management system concepts; NIST AI RMF Govern, Map, Measure, Manage; UK principles of safety, transparency, fairness, accountability, and contestability.

**How to use:** Update blue-font input cells in the source workbook. Formula-driven scores and dashboard metrics update in Excel. Review risks monthly and whenever a system, data source, vendor, or use case materially changes.

> **Important note:** All systems, ratings, owners, dates, and findings are synthetic portfolio examples, not verified facts about any real organisation.

## Table of Contents

1. [AI Inventory Register](#ai-inventory-register)
2. [AI Risk Register](#ai-risk-register)
3. [Governance Gap Assessment](#governance-gap-assessment)
4. [Executive Summary Dashboard](#executive-summary-dashboard)
5. [Framework Mapping](#framework-mapping)

## AI Inventory Register

| System ID | AI System | Primary Purpose | System Type | Business Function | Risk Tier | Lifecycle Status |
|---|---|---|---|---|---|---|
| AI-001 | Microsoft 365 Copilot | Drafting, search and productivity support | Generative AI assistant | Corporate Services | Medium | Production |
| AI-002 | Customer Support Chatbot | Answer common customer questions | Generative AI agent | Customer Service | Medium | Production |
| AI-003 | Recruitment Screening Tool | Rank job applications | Predictive decision support | Human Resources | High | Pilot |
| AI-004 | Invoice Anomaly Detector | Flag unusual invoices for review | Machine learning classifier | Finance | Medium | Production |
| AI-005 | Security Log Triage Agent | Prioritise security alerts and enrich cases | AI agent | Cybersecurity | High | Pilot |
| AI-006 | Meeting Transcription Assistant | Create transcripts and meeting summaries | Speech and generative AI | Corporate Services | Low | Production |

### System Details

**AI-001 · Microsoft 365 Copilot**
Data processed: Email, documents, meeting content · Vendor/hosting: Cloud SaaS · Owner: Digital Workplace Lead · Users: Employees · Decision impact: Advisory · Human oversight: Human reviews output · Last/next review: 2026-07-15 / 2026-10-15
Notes: Use limited to approved tenant and business content.

**AI-002 · Customer Support Chatbot**
Data processed: Customer queries, help articles · Vendor/hosting: Cloud SaaS · Owner: Customer Service Manager · Users: Customers and agents · Decision impact: Advisory · Human oversight: Agent escalation available · Last/next review: 2026-07-20 / 2026-10-20
Notes: Knowledge base retrieval and escalation controls required.

**AI-003 · Recruitment Screening Tool**
Data processed: CVs, employment history, assessment data · Vendor/hosting: Cloud SaaS · Owner: Head of Talent Acquisition · Users: Recruiters · Decision impact: Material · Human oversight: Human approves shortlist · Last/next review: 2026-08-01 / 2026-09-01
Notes: High impact on employment opportunity.

**AI-004 · Invoice Anomaly Detector**
Data processed: Invoices, supplier records, payment history · Vendor/hosting: Private cloud · Owner: Finance Operations Lead · Users: Finance analysts · Decision impact: Advisory · Human oversight: Analyst validates alert · Last/next review: 2026-06-30 / 2026-09-30
Notes: Does not block payment automatically.

**AI-005 · Security Log Triage Agent**
Data processed: Security logs, alerts, asset metadata · Vendor/hosting: Private cloud · Owner: SOC Manager · Users: Security analysts · Decision impact: Operational · Human oversight: Analyst approves containment · Last/next review: 2026-08-05 / 2026-09-05
Notes: Tool access must use least privilege and full logging.

**AI-006 · Meeting Transcription Assistant**
Data processed: Voice, transcript, participant names · Vendor/hosting: Cloud SaaS · Owner: Collaboration Services Lead · Users: Employees · Decision impact: Low · Human oversight: User reviews summary · Last/next review: 2026-07-10 / 2027-01-10
Notes: Consent, retention and access settings must be clear.

## AI Risk Register

| Risk ID | System | Category | Inherent Score | Residual Score | Residual Rating | Status |
|---|---|---|---|---|---|---|
| R-001 | Recruitment Screening Tool | Fairness | 20 | 8 | Medium | Open |
| R-002 | Microsoft 365 Copilot | Privacy / Security | 15 | 8 | Medium | In Progress |
| R-003 | Customer Support Chatbot | Reliability | 12 | 6 | Medium | In Progress |
| R-004 | Security Log Triage Agent | Agentic / Security | 15 | 8 | Medium | Open |
| R-005 | Invoice Anomaly Detector | Performance | 9 | 4 | Low | Open |
| R-006 | Meeting Transcription Assistant | Privacy | 12 | 6 | Medium | Open |
| R-007 | Customer Support Chatbot | Security | 16 | 12 | High | Open |
| R-008 | Microsoft 365 Copilot | Human Factors | 12 | 9 | Medium | Open |

*Scores are Likelihood × Impact on a 1–5 scale (Inherent = before controls, Residual = after controls).*

### Risk Details

**R-001 · Biased ranking could disadvantage qualified candidates.**
Stakeholders: Applicants, recruiters · Inherent: Likelihood 4 × Impact 5 = 20 · Current controls: Human review; periodic outcome testing; vendor documentation (effectiveness 3) · Residual: Likelihood 2 × Impact 4 = 8 (Medium)
Owner: Head of Talent Acquisition · Treatment: Mitigate · Action: Complete independent bias test and define appeal route · Target: 2026-09-15 · Evidence: Bias test report; review records · Framework: EU AI Act; NIST MAP/MEASURE; ISO 42001 impact assessment

**R-002 · Sensitive content could be exposed through poor permissions or sharing.**
Stakeholders: Employees, clients · Inherent: 3 × 5 = 15 · Current controls: Tenant controls; sensitivity labels; access reviews (effectiveness 3) · Residual: 2 × 4 = 8 (Medium)
Owner: Digital Workplace Lead · Treatment: Mitigate · Action: Review oversharing and high-risk repositories · Target: 2026-10-01 · Evidence: Access review; label policy; monitoring logs · Framework: NIST GOVERN/MANAGE; ISO 42001 controls

**R-003 · Incorrect answers could mislead customers or create service harm.**
Stakeholders: Customers · Inherent: 4 × 3 = 12 · Current controls: Approved knowledge base; escalation; response monitoring (effectiveness 3) · Residual: 2 × 3 = 6 (Medium)
Owner: Customer Service Manager · Treatment: Mitigate · Action: Add high-risk topic blocklist and quality sampling · Target: 2026-09-30 · Evidence: Sample results; escalation logs · Framework: EU AI Act transparency; NIST MEASURE/MANAGE

**R-004 · Excessive permissions could cause unintended system actions.**
Stakeholders: IT operations, customers · Inherent: 3 × 5 = 15 · Current controls: Least privilege; approval gate; action logging; sandbox (effectiveness 3) · Residual: 2 × 4 = 8 (Medium)
Owner: SOC Manager · Treatment: Mitigate · Action: Test kill switch and quarterly permission review · Target: 2026-09-05 · Evidence: Permission review; test results; audit logs · Framework: NIST MANAGE; ISO 42001 operational controls

**R-005 · Model drift could reduce detection accuracy and delay valid payments.**
Stakeholders: Finance, suppliers · Inherent: 3 × 3 = 9 · Current controls: Monthly performance review; analyst validation (effectiveness 3) · Residual: 2 × 2 = 4 (Low)
Owner: Finance Operations Lead · Treatment: Monitor · Action: Define drift thresholds and retraining trigger · Target: 2026-09-30 · Evidence: Performance dashboard; validation records · Framework: NIST MEASURE; ISO 42001 monitoring

**R-006 · Transcripts could be retained or accessed beyond business need.**
Stakeholders: Meeting participants · Inherent: 3 × 4 = 12 · Current controls: Restricted access; retention setting; user notification (effectiveness 3) · Residual: 2 × 3 = 6 (Medium)
Owner: Collaboration Services Lead · Treatment: Mitigate · Action: Document consent and retention standard · Target: 2026-10-15 · Evidence: Retention policy; access logs · Framework: UK privacy principle; ISO 42001 data controls

**R-007 · Prompt injection could manipulate retrieval or reveal restricted content.**
Stakeholders: Customers, organisation · Inherent: 4 × 4 = 16 · Current controls: Input filtering; scoped retrieval; red-team testing (effectiveness 2) · Residual: 3 × 4 = 12 (High)
Owner: Customer Service Manager · Treatment: Mitigate · Action: Segment knowledge index and strengthen retrieval authorization · Target: 2026-09-20 · Evidence: Red-team report; retrieval logs · Framework: NIST MANAGE; secure-by-design

**R-008 · Users may rely on hallucinated or incomplete output without verification.**
Stakeholders: Employees, decision-makers · Inherent: 4 × 3 = 12 · Current controls: User guidance; citations; human review (effectiveness 2) · Residual: 3 × 3 = 9 (Medium)
Owner: Digital Workplace Lead · Treatment: Mitigate · Action: Launch AI literacy module and verification checklist · Target: 2026-09-30 · Evidence: Training records; guidance document · Framework: EU AI Act Article 4; NIST GOVERN

## Governance Gap Assessment

| Gap ID | Governance Domain | Priority | Status |
|---|---|---|---|
| G-001 | AI Inventory | High | Open |
| G-002 | Risk and Impact Assessment | High | Open |
| G-003 | Human Oversight | High | In Progress |
| G-004 | Data Governance | High | Open |
| G-005 | Monitoring and Logging | Medium | Open |
| G-006 | Third-Party AI | High | Open |
| G-007 | AI Literacy | Medium | Open |
| G-008 | Incident Response | High | Open |

### Gap Details

**G-001 · AI Inventory**
Current state: Known tools listed manually → Target state: Complete, owned, regularly reviewed inventory
Finding: No formal discovery process for new or unapproved AI tools.
Recommended action: Establish intake process, quarterly attestation, and Shadow AI discovery review.
Owner: AI Governance Lead · Target: 2026-10-31 · Evidence required: Approved inventory; attestations; discovery report · Framework: NIST GOVERN 1; ISO/IEC 42001 context and inventory

**G-002 · Risk and Impact Assessment**
Current state: Assessments vary by project → Target state: Consistent risk-based assessment before approval
Finding: No standard AI impact assessment template or approval threshold.
Recommended action: Adopt one assessment covering purpose, stakeholders, data, rights, safety, security, and residual risk.
Owner: Enterprise Risk Lead · Target: 2026-09-30 · Evidence required: Completed AIIA; approval decision · Framework: NIST MAP; EU AI Act risk-based approach

**G-003 · Human Oversight**
Current state: Oversight exists but is not consistently documented → Target state: Clearly defined HITL, HOTL, or HIC controls
Finding: Override authority and escalation triggers are unclear for two high-impact systems.
Recommended action: Document oversight model, pause authority, escalation trigger, and appeal route.
Owner: Business System Owners · Target: 2026-09-30 · Evidence required: RACI; operating procedure; test record · Framework: EU AI Act human oversight; OECD accountability

**G-004 · Data Governance**
Current state: Existing security controls apply → Target state: AI-specific provenance, quality, bias and retention controls
Finding: Data lineage and quality evidence is incomplete for recruitment and chatbot sources.
Recommended action: Create source register, provenance checks, quality rules, and retention review.
Owner: Data Governance Lead · Target: 2026-10-15 · Evidence required: Data sheet; lineage; quality report · Framework: EU AI Act data governance; NIST MAP/MEASURE

**G-005 · Monitoring and Logging**
Current state: Technical logs exist → Target state: Risk-based monitoring tied to incidents and thresholds
Finding: No unified AI monitoring metrics or retained evidence standard.
Recommended action: Define performance, bias, security, drift, incident, and human-override metrics.
Owner: AI Operations Lead · Target: 2026-11-15 · Evidence required: Monitoring standard; dashboards; log samples · Framework: NIST MEASURE/MANAGE; EU AI Act logging

**G-006 · Third-Party AI**
Current state: General vendor process → Target state: AI-specific due diligence and contract clauses
Finding: Vendor reviews do not consistently cover training use, retention, model changes, and incident notice.
Recommended action: Add AI vendor checklist and minimum contractual safeguards.
Owner: Procurement Lead · Target: 2026-10-31 · Evidence required: Vendor assessment; contract clauses · Framework: NIST GOVERN; ISO/IEC 42001 supplier controls

**G-007 · AI Literacy**
Current state: Informal awareness → Target state: Role-based training and competence records
Finding: Users lack consistent guidance on verification, sensitive data, and escalation.
Recommended action: Launch role-based AI literacy and maintain completion evidence.
Owner: Learning and Development Lead · Target: 2026-10-15 · Evidence required: Training material; attendance; assessment results · Framework: EU AI Act Article 4; ISO/IEC 42001 competence

**G-008 · Incident Response**
Current state: Cyber incident process exists → Target state: AI incident playbook integrated with governance feedback
Finding: AI-specific containment, evidence preservation, and retraining decisions are undefined.
Recommended action: Create AI incident playbook and test through a tabletop exercise.
Owner: CISO / AI Governance Lead · Target: 2026-11-30 · Evidence required: Playbook; exercise record; lessons learned · Framework: NIST MANAGE; ISO/IEC 42001 improvement

## Executive Summary Dashboard

*Portfolio demonstration using synthetic data.*

| Total AI Systems | High-Risk Systems | Open Risks | High-Priority Gaps |
|---|---|---|---|
| 6 | 2 | 6 | 6 |

| Risk Tier | Count |   | Gap Priority | Count |   | Residual Rating | Count |   | Risk Status | Count |
|---|---|---|---|---|---|---|---|---|---|---|
| High | 2 |   | High | 6 |   | Critical | 0 |   | Open | 6 |
| Medium | 3 |   | Medium | 2 |   | High | 1 |   | In Progress | 2 |
| Low | 1 |   | Low | 0 |   | Medium | 6 |   | Closed | 0 |
|  |  |   |  |  |   | Low | 1 |   | Accepted | 0 |

### Management Priorities

1. Formalise AI intake, inventory ownership and Shadow AI discovery.
2. Complete impact and bias assessment for the recruitment screening pilot.
3. Define human oversight, pause authority and escalation triggers for high-impact systems.
4. Strengthen provenance, quality and access controls for AI knowledge sources.
5. Launch role-based AI literacy and an AI incident response tabletop exercise.

## Framework Mapping

| Project Activity | NIST AI RMF | ISO/IEC 42001 | EU AI Act | UK Principles | Portfolio Evidence |
|---|---|---|---|---|---|
| Maintain AI inventory | GOVERN; MAP | AI management system scope, roles, operational planning | Supports classification and provider/deployer obligations | Accountability | AI Inventory Register |
| Assess risks and impacts | MAP; MEASURE | AI risk and impact assessment | Risk-based classification; high-risk requirements | Safety; fairness | AI Risk Register and AIIA evidence |
| Define controls and treatment | GOVERN; MANAGE | Risk treatment and operational controls | Risk management, data, logging, transparency, human oversight | Safety; accountability | Control descriptions and treatment actions |
| Monitor performance and incidents | MEASURE; MANAGE | Performance evaluation, internal audit, improvement | Post-market monitoring, logging, incident duties | Safety; contestability | Monitoring logs and incident records |
| Report to leadership | GOVERN | Leadership, objectives, management review | Demonstrates accountability and compliance oversight | Accountability; transparency | Executive Summary Dashboard |

### Reference Sources (Official Framework Pages)

- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)
- [ISO/IEC 42001](https://www.iso.org/standard/81230.html)
- [EU AI Act](https://artificialintelligenceact.eu/)
- [UK — A Pro-Innovation Approach to AI Regulation](https://www.gov.uk/government/publications/ai-regulation-a-pro-innovation-approach)
