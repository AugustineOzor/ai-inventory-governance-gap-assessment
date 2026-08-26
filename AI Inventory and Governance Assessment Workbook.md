# AI Governance Portfolio Workbook 4 — AI Inventory and Governance Assessment

## Read Me

**Portfolio purpose:** A practical demonstration of AI inventory management, risk categorisation, governance control assessment, gap analysis, and executive reporting.

**Scope:** Six illustrative AI systems used by a fictional mid-sized organisation. Replace the sample entries with verified organisational data before operational use.

**Deliverables:**

1. AI Inventory Register
2. AI Risk Register
3. Governance Gap Assessment
4. Executive Summary Dashboard

**Framework alignment:** EU AI Act risk-based approach; ISO/IEC 42001 AI management system concepts; NIST AI RMF Govern, Map, Measure, Manage; UK principles of safety, transparency, fairness, accountability, and contestability.

**How to use:** Update blue-font input cells. Formula-driven scores and dashboard metrics update in Excel. Review risks monthly and whenever a system, data source, vendor, or use case materially changes.

**Important note:** All systems, ratings, owners, dates, and findings are synthetic portfolio examples, not verified facts about any real organisation.

## AI Inventory

| System ID | AI System | Primary Purpose | System Type | Business Function | Data Processed | Vendor / Hosting | Primary Owner | Users | Decision Impact | Human Oversight | Lifecycle Status | Risk Tier | Last Review | Next Review | Notes |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| AI-001 | Microsoft 365 Copilot | Drafting, search and productivity support | Generative AI assistant | Corporate Services | Email, documents, meeting content | Cloud SaaS | Digital Workplace Lead | Employees | Advisory | Human reviews output | Production | Medium | 2026-07-15 | 2026-10-15 | Use limited to approved tenant and business content. |
| AI-002 | Customer Support Chatbot | Answer common customer questions | Generative AI agent | Customer Service | Customer queries, help articles | Cloud SaaS | Customer Service Manager | Customers and agents | Advisory | Agent escalation available | Production | Medium | 2026-07-20 | 2026-10-20 | Knowledge base retrieval and escalation controls required. |
| AI-003 | Recruitment Screening Tool | Rank job applications | Predictive decision support | Human Resources | CVs, employment history, assessment data | Cloud SaaS | Head of Talent Acquisition | Recruiters | Material | Human approves shortlist | Pilot | High | 2026-08-01 | 2026-09-01 | High impact on employment opportunity. |
| AI-004 | Invoice Anomaly Detector | Flag unusual invoices for review | Machine learning classifier | Finance | Invoices, supplier records, payment history | Private cloud | Finance Operations Lead | Finance analysts | Advisory | Analyst validates alert | Production | Medium | 2026-06-30 | 2026-09-30 | Does not block payment automatically. |
| AI-005 | Security Log Triage Agent | Prioritise security alerts and enrich cases | AI agent | Cybersecurity | Security logs, alerts, asset metadata | Private cloud | SOC Manager | Security analysts | Operational | Analyst approves containment | Pilot | High | 2026-08-05 | 2026-09-05 | Tool access must use least privilege and full logging. |
| AI-006 | Meeting Transcription Assistant | Create transcripts and meeting summaries | Speech and generative AI | Corporate Services | Voice, transcript, participant names | Cloud SaaS | Collaboration Services Lead | Employees | Low | User reviews summary | Production | Low | 2026-07-10 | 2027-01-10 | Consent, retention and access settings must be clear. |

## AI Risk Register

*Inherent Score = Inherent Likelihood × Inherent Impact. Residual Score = Residual Likelihood × Residual Impact. Residual Rating: ≥15 Critical, ≥10 High, ≥5 Medium, else Low — computed from the workbook's own formulas.*

| Risk ID | System ID | AI System | Risk Statement | Category | Affected Stakeholders | Inherent Likelihood | Inherent Impact | Inherent Score | Current Controls | Control Effectiveness | Residual Likelihood | Residual Impact | Residual Score | Residual Rating | Risk Owner | Treatment | Action | Target Date | Status | Evidence | Framework Link |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| R-001 | AI-003 | Recruitment Screening Tool | Biased ranking could disadvantage qualified candidates. | Fairness | Applicants, recruiters | 4 | 5 | 20 | Human review; periodic outcome testing; vendor documentation | 3 | 2 | 4 | 8 | Medium | Head of Talent Acquisition | Mitigate | Complete independent bias test and define appeal route | 2026-09-15 | Open | Bias test report; review records | EU AI Act; NIST MAP/MEASURE; ISO 42001 impact assessment |
| R-002 | AI-001 | Microsoft 365 Copilot | Sensitive content could be exposed through poor permissions or sharing. | Privacy / Security | Employees, clients | 3 | 5 | 15 | Tenant controls; sensitivity labels; access reviews | 3 | 2 | 4 | 8 | Medium | Digital Workplace Lead | Mitigate | Review oversharing and high-risk repositories | 2026-10-01 | In Progress | Access review; label policy; monitoring logs | NIST GOVERN/MANAGE; ISO 42001 controls |
| R-003 | AI-002 | Customer Support Chatbot | Incorrect answers could mislead customers or create service harm. | Reliability | Customers | 4 | 3 | 12 | Approved knowledge base; escalation; response monitoring | 3 | 2 | 3 | 6 | Medium | Customer Service Manager | Mitigate | Add high-risk topic blocklist and quality sampling | 2026-09-30 | In Progress | Sample results; escalation logs | EU AI Act transparency; NIST MEASURE/MANAGE |
| R-004 | AI-005 | Security Log Triage Agent | Excessive permissions could cause unintended system actions. | Agentic / Security | IT operations, customers | 3 | 5 | 15 | Least privilege; approval gate; action logging; sandbox | 3 | 2 | 4 | 8 | Medium | SOC Manager | Mitigate | Test kill switch and quarterly permission review | 2026-09-05 | Open | Permission review; test results; audit logs | NIST MANAGE; ISO 42001 operational controls |
| R-005 | AI-004 | Invoice Anomaly Detector | Model drift could reduce detection accuracy and delay valid payments. | Performance | Finance, suppliers | 3 | 3 | 9 | Monthly performance review; analyst validation | 3 | 2 | 2 | 4 | Low | Finance Operations Lead | Monitor | Define drift thresholds and retraining trigger | 2026-09-30 | Open | Performance dashboard; validation records | NIST MEASURE; ISO 42001 monitoring |
| R-006 | AI-006 | Meeting Transcription Assistant | Transcripts could be retained or accessed beyond business need. | Privacy | Meeting participants | 3 | 4 | 12 | Restricted access; retention setting; user notification | 3 | 2 | 3 | 6 | Medium | Collaboration Services Lead | Mitigate | Document consent and retention standard | 2026-10-15 | Open | Retention policy; access logs | UK privacy principle; ISO 42001 data controls |
| R-007 | AI-002 | Customer Support Chatbot | Prompt injection could manipulate retrieval or reveal restricted content. | Security | Customers, organisation | 4 | 4 | 16 | Input filtering; scoped retrieval; red-team testing | 2 | 3 | 4 | 12 | High | Customer Service Manager | Mitigate | Segment knowledge index and strengthen retrieval authorization | 2026-09-20 | Open | Red-team report; retrieval logs | NIST MANAGE; secure-by-design |
| R-008 | AI-001 | Microsoft 365 Copilot | Users may rely on hallucinated or incomplete output without verification. | Human Factors | Employees, decision-makers | 4 | 3 | 12 | User guidance; citations; human review | 2 | 3 | 3 | 9 | Medium | Digital Workplace Lead | Mitigate | Launch AI literacy module and verification checklist | 2026-09-30 | Open | Training records; guidance document | EU AI Act Article 4; NIST GOVERN |

## Gap Assessment

| Gap ID | Governance Domain | Current State | Target State | Gap / Finding | Risk Priority | Recommended Action | Owner | Target Date | Status | Evidence Required | Framework Mapping |
|---|---|---|---|---|---|---|---|---|---|---|---|
| G-001 | AI Inventory | Known tools listed manually | Complete, owned, regularly reviewed inventory | No formal discovery process for new or unapproved AI tools. | High | Establish intake process, quarterly attestation, and Shadow AI discovery review. | AI Governance Lead | 2026-10-31 | Open | Approved inventory; attestations; discovery report | NIST GOVERN 1; ISO/IEC 42001 context and inventory |
| G-002 | Risk and Impact Assessment | Assessments vary by project | Consistent risk-based assessment before approval | No standard AI impact assessment template or approval threshold. | High | Adopt one assessment covering purpose, stakeholders, data, rights, safety, security, and residual risk. | Enterprise Risk Lead | 2026-09-30 | Open | Completed AIIA; approval decision | NIST MAP; EU AI Act risk-based approach |
| G-003 | Human Oversight | Oversight exists but is not consistently documented | Clearly defined HITL, HOTL, or HIC controls | Override authority and escalation triggers are unclear for two high-impact systems. | High | Document oversight model, pause authority, escalation trigger, and appeal route. | Business System Owners | 2026-09-30 | In Progress | RACI; operating procedure; test record | EU AI Act human oversight; OECD accountability |
| G-004 | Data Governance | Existing security controls apply | AI-specific provenance, quality, bias and retention controls | Data lineage and quality evidence is incomplete for recruitment and chatbot sources. | High | Create source register, provenance checks, quality rules, and retention review. | Data Governance Lead | 2026-10-15 | Open | Data sheet; lineage; quality report | EU AI Act data governance; NIST MAP/MEASURE |
| G-005 | Monitoring and Logging | Technical logs exist | Risk-based monitoring tied to incidents and thresholds | No unified AI monitoring metrics or retained evidence standard. | Medium | Define performance, bias, security, drift, incident, and human-override metrics. | AI Operations Lead | 2026-11-15 | Open | Monitoring standard; dashboards; log samples | NIST MEASURE/MANAGE; EU AI Act logging |
| G-006 | Third-Party AI | General vendor process | AI-specific due diligence and contract clauses | Vendor reviews do not consistently cover training use, retention, model changes, and incident notice. | High | Add AI vendor checklist and minimum contractual safeguards. | Procurement Lead | 2026-10-31 | Open | Vendor assessment; contract clauses | NIST GOVERN; ISO/IEC 42001 supplier controls |
| G-007 | AI Literacy | Informal awareness | Role-based training and competence records | Users lack consistent guidance on verification, sensitive data, and escalation. | Medium | Launch role-based AI literacy and maintain completion evidence. | Learning and Development Lead | 2026-10-15 | Open | Training material; attendance; assessment results | EU AI Act Article 4; ISO/IEC 42001 competence |
| G-008 | Incident Response | Cyber incident process exists | AI incident playbook integrated with governance feedback | AI-specific containment, evidence preservation, and retraining decisions are undefined. | High | Create AI incident playbook and test through a tabletop exercise. | CISO / AI Governance Lead | 2026-11-30 | Open | Playbook; exercise record; lessons learned | NIST MANAGE; ISO/IEC 42001 improvement |

## Dashboard — Executive Summary

*Portfolio demonstration using synthetic data. Figures below are computed from the workbook's own `COUNTA`/`COUNTIF` formulas against the sheets above.*

| Total AI Systems | High-Risk Systems | Open Risks | High-Priority Gaps |
|---|---|---|---|
| 6 | 2 | 6 | 6 |

**Risk Tier (AI Inventory)**

| Tier | Count |
|---|---|
| High | 2 |
| Medium | 3 |
| Low | 1 |

**Gap Priority (Gap Assessment)**

| Priority | Count |
|---|---|
| High | 6 |
| Medium | 2 |
| Low | 0 |

**Residual Rating (AI Risk Register)**

| Rating | Count |
|---|---|
| Critical | 0 |
| High | 1 |
| Medium | 6 |
| Low | 1 |

**Risk Status (AI Risk Register)**

| Status | Count |
|---|---|
| Open | 6 |
| In Progress | 2 |
| Closed | 0 |
| Accepted | 0 |

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

**Reference sources (official framework pages):**

- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)
- [ISO/IEC 42001](https://www.iso.org/standard/81230.html)
- [EU AI Act](https://artificialintelligenceact.eu/)
- [UK AI Regulation: A Pro-Innovation Approach](https://www.gov.uk/government/publications/ai-regulation-a-pro-innovation-approach)
