# Risk management

ISO 31000 is an international standard providing principles, a framework, and a process for organizations to manage risks

Specific AI risk management documents:
* ISO/IEC 23894:2023 is an international standard that provides guidance on managing risks associated with AI for organizations that develop, produce, deploy, or use AI.
* The NIST AI Risk Management Framework (AI RMF) is a framework to better manage risks to individuals, organizations, and society associated with AI (https://doi.org/10.6028/NIST.AI.100-1).
* Chapter 3 of the AI Safety Report provides overview of AI risk management approaches (https://internationalaisafetyreport.org/publication/international-ai-safety-report-2025#3-technical-approaches-to-risk-management)
* AI Exchange on AI Security refers to the Risk Management Framework of ISO/IEC 23894:2023 (https://owaspai.org/goto/riskanalysis/).
* Guidance for Risk Management of Artificial Intelligence systems by European Data Protection Supervisor (https://www.edps.europa.eu/system/files/2025-11/2025-11-11_ai_risks_management_guidance_en.pdf)

## Selected risk management mechanisms and practices from the AI safety report

* Risk Identification: Risk Taxonomy, Threat Modelling
* Risk Assessment: 
   * Impact Assessment (e.g., Fundamental Rights Impact Assessment for High-Risk AI Systems due to the EU AI Act https://artificialintelligenceact.eu/article/27, Data Protection Impact Assessment due to GDPR https://gdpr-info.eu/art-35-gdpr). Question: What’s about copyright & Co?
   * Audit (https://www.edpb.europa.eu/our-work-tools/our-documents/support-pool-experts-projects/ai-auditing_en)
   * Red-Teaming (deliberately attacking your own AI systems in order to identify vulnerabilities)
   * Benchmarks
   * Model Evaluation
   * Safety Analysis
* Risk Evaluation: Risk Tolerance, Risk Thresholds
* Risk Mitigation: 
   * Safety by Design (remember Chapter 3 “Safety and Security” of the Code of Conduct EU AI Act)
   * Defense in Depth (implementing multiple independent and overlapping layers of defense, multiple preventive measures)
* Risk Governance: 
   * Documentation (model cards, system cards, etc. Remember Chapter 1 “Transparency” of the Code of Conduct EU AI Act)
   * Risk Register
   * Incident Reporting
   * Risk Management Frameworks

## Risk management framework

* Identifying Risks: Recognizing potential risks that could impact the organization. 
* Evaluating Risks by Estimating Likelihood and Impact: To determine the severity of a risk, it is necessary to assess the probability of the risk occurring and evaluating the potential consequences should the risk materialize. 
* Deciding What to Do (Risk Treatment): Choosing an appropriate strategy to address the risk. These strategies include:
   * Risk Mitigation,
   * Transfer,
   * Avoidance,
   * Acceptance. 
* Risk Communication and Monitoring: Regularly sharing risk information with stakeholders to ensure awareness and continuous support for risk management activities. Ensuring effective Risk Treatments are applied. This requires a Risk Register, a comprehensive list of risks and their attributes (e.g. severity, treatment plan, ownership, status, etc). 

## Risk identification via risk taxonomy: MIT AI Risk Repository

https://doi.org/10.48550/arXiv.2408.12622



```{exercise} ❓ Quiz

Which of the following best describes risk management of AI use in research projects?
* Avoiding AI use whenever risks are identified
* Identifying, evaluating, treating, and monitoring risks throughout the research lifecycle
* Delegating all responsibility to IT departments
* Focusing only on legal compliance after deployment
```
