# Risk management in research projects

## Defense in depth for your research (project)

Defense in depth is a risk-mitigation approach that relies on multiple, overlapping, and complementary layers of safeguards, so that if one control fails, others remain effective.

Key assumption: any single mitigation measure can fail.

Dimensions of defense in research (projects) for an AI use case:
* People: individual researchers, research teams, project partners, and participants
* Infrastructure/Technology: hardware, software, data, models, networks, and the entire supply chain
* Processes: research process including research ethics, research integrity, and research governance

## Trinity of risks related to AI use in research 

Using AI in research (projects) introduces the following risks:
* Ethical: intentional and unintentional harms to participants, communities, society, and the environment (privacy and data protection, copyright and other intellectual rights, confidentiality, bias, discrimination, malicious use, and dual use)
* Integrity: intentional and unintentional harms to the truth and scientific quality including scientific misconduct, questionable research practices, and irresponsible use of AI systems 
* Governance: intentional and unintentional breaches of the laws and regulations including GDPR, copyright, EU AI Act, dual-use and export control regulations, and contractual requirements

## Practical risk management

There is an AI use case in a research project.
* It contains three dimensions: people (users, developers, co-authors, etc.), technology (AI system and alternatives), and processes (ethics, integrity, and governance).
* Apply the risk management framework adapted to the trinity of risks in research projects to your AI use case. [see the next slide]

## Risk management framework adapted to the trinity of risks in research (projects)

Let's adapt the Risk management framework (https://owaspai.org/goto/riskanalysis/) to the trinity of risks:
* Identifying Risks: Recognizing potential risks related to research ethics, research integrity, and research governance. 
* Evaluating Risks: Subjectively: low, medium, high.
* Risk Treatment: Choosing an appropriate strategy to address the risk: Risk Mitigation, Transfer (to another party), Avoidance (eliminating the source), or Acceptance.
* Risk Communication and Monitoring: Regularly sharing risk information with stakeholders. Creating a Risk Register, a list of risks and their attributes (e.g. severity, treatment plan, ownership, status, etc). 

```{note}
*Any mitigation measure can fail. Apply defense in depth to all three dimensions (people, technology, and processes) in Risk Mitigation.
```
## People (Researchers, Teams, and Partners)

General mitigation measures involving people and human factor
* Competence & awareness
   * Define minimum AI literacy expectations for project members (what AI can/cannot do).
   * Ensure researchers understand the trinity or risks. Treat AI literacy as continuous.
* Clear responsibility
   * Explicitly state: humans remain responsible for scientific outputs, not AI systems.
   * Assign AI-use responsibility at project level (e.g., PI or work-package lead).
* Disclosure & transparency
   * Agree on when and how AI use must be disclosed
   * Encourage a culture where declaring AI use is normal, not penalised.
* Collaboration safeguards
   * Align expectations on AI use with project partners, co-authors, and student assistants
   * Explicitly clarify AI rules for junior researchers and external collaborators.

## Technology & Infrastructure: AI Systems

General mitigation measures involving technology and infrastructure
* Tool selection
   * Prefer AI systems (including models) that provide compliance documentation (trust portals and certifications)
* Access control
   * Apply least-privilege principles to AI systems (e.g., limit file system access)
   * Never grant agentic AI unrestricted access to personal, sensitive, and confidential data
* Data protection
   * Don‘t input personal or sensitive data into third-part AI systems. Use fully local, self-managed AI systems
   * Use pseudonymisation, anonymisation, or synthetic data where possible.
* Model limitations
   * Any AI model has limitations. Check them. 
* Technical safeguards
   * Ensure appropriate technical and organisational measures

## Processes: Ethics, Integrity, and Governance

General mitigation measures for three processes in research
* Research ethics:
   * Integrate AI use into ethics self-assessment, even if formal ethics approval is not required.
   * Get support from ethics committees 
* Research integrity:
   * Require AI-use documentation
   * Preserve input and output data, models, and ensure reproducibility/replicability of your research
   * Define red lines: no fabrication, falsification, and plagiarism
* Research governance:
   * Apply legal and regulatory checklists 
   * Conduct legal pre-checks 
   * Get institutional support: DPO, legal team, RDM-team, IT- and IT-security-teams, etc.

## Mapping the trinity of risks and existing guidelines and recommendations on AI use in research

| Trinity of risks | EU Guidelines on the responsible use of generative AI in research | Helmholtz “Recommendations for the use of artificial intelligence” |
|---|---|---|
| **Ethical risks** | • Privacy, confidentiality, and IP rights<br>• Bias and prejudices due to training data | • Privacy and confidentiality |
| **Integrity risks** | • Responsibility for scientific output<br>• Transparent AI use<br>• Continuous AI literacy | • Sensitive activities impacting others<br>• (Scientific) information integrity |
| **Governance risks** | • National, EU & international legislation | • AI-related regulation<br>• Copyright and IP rights<br>• Privacy and confidentiality |
