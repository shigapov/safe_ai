# EU AI Act

The summary of EU AI Act is available at https://artificialintelligenceact.eu/high-level-summary.

## The AI Act classifies AI according to its risk

* Unacceptable risk is prohibited (e.g. social scoring systems and manipulative AI).
* Most of the text addresses high-risk AI systems, which are regulated.
* A smaller section handles limited risk AI systems, subject to lighter transparency obligations: developers and deployers must ensure that end-users are aware that they are interacting with AI (chatbots and deepfakes).
* Minimal risk is unregulated (including the majority of AI applications currently available on the EU single market, such as AI enabled video games and spam filters – at least in 2021; this is changing with generative AI).

## EU AI Act and research

* Art. 2 (6): „This Regulation does not apply to AI systems or AI models, including their output, specifically developed and put into service for the sole purpose of scientific research and development“ https://artificialintelligenceact.eu/article/2/ 
* Recital 25: „This Regulation should support innovation, should respect freedom of science, and should not undermine research and development activity. It is therefore necessary to exclude from its scope AI systems and models specifically developed and put into service for the sole purpose of scientific research and development. […] In any event, any research and development activity should be carried out in accordance with recognised ethical and professional standards for scientific research and should be conducted in accordance with applicable Union law.“

## The majority of obligations fall on providers (developers) of high-risk AI systems

* Those that intend to place on the market or put into service high-risk AI systems in the EU, regardless of whether they are based in the EU or a third country.
* And also third country providers where the high risk AI system’s output is used in the EU.
* Deployers of high-risk AI systems have some obligations, though less than providers.

‘provider’ (developer)
: develops an AI system or a general-purpose AI model or has an AI system or a general-purpose AI model developed and places it on the market or puts the AI system into service under its own name or trademark, whether for payment or free of charge

‘deployer’ (user)
: uses an AI system under its authority except where the AI system is used in the course of a personal non-professional activity

## Prohibited AI Systems (AI Act, Art. 5)

* AI using subliminal, manipulative, or deceptive techniques
* AI exploiting vulnerabilities related to age, disability, or socio-economic circumstances
* Biometric categorisation inferring sensitive attributes
* Social scoring systems
* Assessing the risk of an individual committing criminal offenses solely based on profiling or personality traits
* Compiling facial recognition databases by untargeted scraping of facial images
* Inferring emotions in workplaces or educational institutions
* ‘Real-time’ remote biometric identification (RBI) in publicly accessible spaces for law enforcement
   * Exceptions: missing persons; imminent threats to life or terrorism; suspects of serious crimes

## High-Risk AI Systems (AI Act – Chapter III)

Scope is complex, see Art. 6.
* For example, „Education and vocational training: AI systems determining access, admission or assignment to educational and vocational training institutions at all levels. Evaluating learning outcomes, including those used to steer the student’s learning process. Assessing the appropriate level of education for an individual. Monitoring and detecting prohibited student behaviour during tests. “
* Provider requirements: risk-management system, data governance for training/validation/testing, technical documentation, built-in record-keeping, clear instructions for deployers, human-oversight capability, accuracy/robustness/cybersecurity by design, quality-management system

## General purpose AI (GPAI)

All providers of GPAI models must (https://artificialintelligenceact.eu/chapter/5):
1. Draw up technical documentation, including training and testing process and evaluation results.
2. Draw up information and documentation to supply to downstream providers that intend to integrate the GPAI model into their own AI system in order that the latter understands capabilities and limitations and is enabled to comply.
3. Establish a policy to respect the Copyright Directive.
4. Publish a sufficiently detailed summary about the content used for training the GPAI model. 
Exception for free and open licence GPAI models: The providers only have to comply with the latter two obligations above, unless the free and open licence GPAI model is systemic.

## GPAI models with systemic risks 

GPAI models
: present systemic risks when the cumulative amount of compute used for its training is greater than 1025 floating point operations (FLOPs).

Providers of GPAI models with systemic risk must also:
* Perform model evaluations, including conducting and documenting adversarial testing to identify and mitigate systemic risk.
* Assess and mitigate possible systemic risks, including their sources.
* Track, document and report serious incidents and possible corrective measures to the AI Office and relevant national competent authorities without undue delay.
* Ensure an adequate level of cybersecurity protection.

See https://artificialintelligenceact.eu/chapter/5.

## EU AI Act and Copyright

Specific obligations on the providers of general–purpose AI (GPAI) models (https://artificialintelligenceact.eu/article/53):
* Compliance with the TDM opt-outs expressed by copyright
* Publish ‘sufficiently’ detailed summaries of the training data they utilise, to facilitate copyright holders enforcing their rights holders
Specific obligations on the providers of GenAI systems (https://artificialintelligenceact.eu/article/50):
* Providers of AI systems, including general-purpose AI systems, generating synthetic audio, image, video or text content, shall ensure that the outputs of the AI system are marked in a machine-readable format and detectable as artificially generated or manipulated.

## The General-Purpose AI Code of Practice

* The GPAI Code of Practice is a voluntary tool, prepared by independent experts in a multi-stakeholder process, designed to help industry comply with the AI Act’s obligations for providers of general-purpose AI models.
* The Code of Practice has three chapters:
   1. The Transparency chapter offers a Model Documentation Form (https://ec.europa.eu/newsroom/dae/redirection/document/118118) which allows providers to easily document the information necessary to comply with the AI Act obligation to on model providers to ensure sufficient transparency.
   2. The Copyright chapter offers providers practical solutions to meet the AI Act's obligation to put in place a policy to comply with EU copyright law.
   3. The Safety and Security chapter outlines concrete state-of-the-art practices for managing systemic risks, i.e. risks from the most advanced models. Providers can rely on this chapter to comply with the AI Act obligations for providers of general-purpose AI models with systemic risk.

See https://digital-strategy.ec.europa.eu/en/policies/contents-code-gpai.

## EU AI Act and GPAI Code of Practice: Transparency and Model Documentation Form

* The “Transparency” chapter has one Commitment on “Documentation” (https://ec.europa.eu/newsroom/dae/redirection/document/118118)
* The Model Documentation Form contains the following parts:
   * General information
   * Model properties
   * Methods of distribution and licenses
   * (Acceptable and intended) Use
   * Training process
   * Information on the data used for training, testing, and validation
   * Computational resources (during training)
   * Energy consumption (during training and inference)

## EU AI Act and GPAI Code of Practice: Copyright

The “Copyright” chapter has one Commitment on “Copyright policy” (https://ec.europa.eu/newsroom/dae/redirection/document/118115):
* Measure 1.1 Draw up, keep up-to-date and implement a copyright policy
* Measure 1.2 Reproduce and extract only lawfully accessible copyright-protected content when crawling the World Wide Web
* Measure 1.3 Identify and comply with rights reservations when crawling the World Wide Web
* Measure 1.4 Mitigate the risk of copyright-infringing outputs
* Measure 1.5 Designate a point of contact and enable the lodging of complaints

## EU AI Act and GPAI Code of Practice: Safety and Security

The “Safety and Security” chapter has ten Commitments (https://ec.europa.eu/newsroom/dae/redirection/document/118119).
1. Commitment 1 “Safety and Security Framework”
   * Measure 1.1 Creating the Framework
   * Measure 1.2 Implementing the Framework
   * Measure 1.3 Updating the Framework
   * Measure 1.4 Framework notifications
2. Commitment 2 “Systemic risk identification”
   * Measure 2.1 Systemic risk identification process
   * Measure 2.2 Systemic risk scenarios
3. Commitment 3 “Systemic risk analysis”
   * Measure 3.1 Model-independent information
   * Measure 3.2 Model evaluations
   * Measure 3.3 Systemic risk modelling
   * Measure 3.4 Systemic risk estimation
   * Measure 3.5 Post-market monitoring
4. Commitment 4 “Systemic risk acceptance determination”
   * Measure 4.1 Systemic risk acceptance criteria and acceptance determination
   * Measure 4.2 Proceeding or not proceeding based on systemic risk acceptance determination
5. Commitment 5 “Safety mitigations”
   * Measure 5.1 Appropriate safety mitigations
6. Commitment 6 “Security mitigations”
   * Measure 6.1 Security Goal
   * Measure 6.2 Appropriate security mitigations
7. Commitment 7 “Safety and Security Model Reports”
   * Measure 7.1 Model description and behaviour
   * Measure 7.2 Reasons for proceeding
   * Measure 7.3 Documentation of systemic risk identification, analysis, and mitigation
   * Measure 7.4 External reports
   * Measure 7.5 Material changes to the systemic risk landscape
   * Measure 7.6 Model Report updates
   * Measure 7.7 Model Report notifications
8. Commitment 8 “Systemic risk responsibility allocation”
   * Measure 8.1 Definition of clear responsibilities
   * Measure 8.2 Allocation of appropriate resources
   * Measure 8.3 Promotion of a healthy risk culture
9. Commitment 9 “Serious incident reporting”
   * Measure 9.1 Methods for serious incident identification
   * Measure 9.2 Relevant information for serious incident tracking, documentation, and reporting
   * Measure 9.3 Reporting timelines
   * Measure 9.4 Retention period
10. Commitment 10 “Additional documentation and transparency”
   * Measure 10.1 Additional documentation
   * Measure 10.2 Public transparency

## Tool: EU AI Act Compliance Checker 1

```{admonition} 🛠️ Tool
:class: note

* https://artificialintelligenceact.eu/assessment/eu-ai-act-compliance-checker 
```

## EU AI Act Compliance Checker 2

```{admonition} 🛠️ Tool
:class: note

+ https://ai-act-service-desk.ec.europa.eu/en/eu-ai-act-compliance-checker 
```

```{admonition} ❓ Quiz
:class: note

Can a researcher train an AI model with systemic risk and openly share it?
* Yes
* No
* Yes, but with obligations
```


