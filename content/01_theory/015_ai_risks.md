# AI risks, AI safety, and AI security

According to https://doi.org/10.48550/arXiv.2506.18932, AI safety and AI security differ in the following way:
* AI Safety: risks from accidental or unintended behaviors.
* AI Security: risks from intentional or adversarial actions by malicious actors.

## Main documents on AI safety and AI security

* The International AI Safety Report is the world’s first comprehensive review of the latest science on the capabilities and risks of general-purpose AI systems:
   * https://internationalaisafetyreport.org/publication/international-ai-safety-report-2026 (~220 pages)
   * https://internationalaisafetyreport.org/publication/international-ai-safety-report-2025 (~300 pages)
   * https://internationalaisafetyreport.org/publication/first-key-update-capabilities-and-risk-implications 
   * https://internationalaisafetyreport.org/publication/second-key-update-technical-safeguards-and-risk-management 
* OWASP AI Exchange is a practical resource on AI security and privacy (>200 pages)
   * https://owaspai.org 
* Federal Office for Information Security issues studies, catalogues, and checklists on AI: https://www.bsi.bund.de/EN/Themen/Unternehmen-und-Organisationen/Informationen-und-Empfehlungen/Kuenstliche-Intelligenz/kuenstliche-intelligenz_node.html 

## AI Safety risks from the AI Safety report

### Selected risks from the AI safety report relevant in research context

1. Risks from malicious use
   * Harm to individuals through fake content. AI-generated fake content can be used to manipulate governance processes, sabotage collaborations, or personally target researchers and undermine trust in science.
   * Manipulation of public opinion. AI-generated fake content and narrative manipulation can directly target researchers, research projects, research ideas, and public trust in science.
   * Cyber offence. AI-assisted cyber attacks may affect research infrastructures, collaborations, and sensitive scientific outputs.
   * Biological and chemical attacks. 
2. Risks from malfunctions
   * Reliability issues. This can lead violations of research ethics, research integrity, and research governance due to irresponsible use of AI systems having reliability issues.
   * Bias. Biased data, models, and AI systems can lead to discriminatory or misleading results violating research ethics principles. Researchers have an ethical duty to identify, mitigate, and transparently report bias.
3. Systemic risks
   * Risks to the environment. Key ethical question for research projects: Is the environmental cost of using an AI system justified by the expected scientific and societal benefit?
   * Risks to privacy. This can lead to violations of research ethics, research integrity, and research governance.
   * Risks of copyright infringement. This can lead to violations of research ethics, research integrity, and research governance.
4. Impact of open-weight general-purpose AI models on AI risks.

### Risks from open-weight general-purpose AI models on AI risks

The AI safety report has the following points:
* Risks posed by open-weight models are largely related to enabling malicious or misguided use, because general-purpose AI models are dual-use:
* Safeguards against misuse are easier to remove for open models
* Model vulnerabilities found in open models can also expose vulnerabilities in closed models
* Once model weights are available for public download, there is no way back
* There are risk mitigation approaches for open-weight models throughout the AI lifecycle. The most robust risk mitigation strategies will aim to address potential issues at every stage from data collection to post-release measures such as vulnerability disclosure.

From the other side:
* Security by obscurity is not recommended by NIST: "System security should not depend on the secrecy of the implementation or its components."
* The Kerckhoffs's principle: "A system should be secure, even if everything about the system is public knowledge."
* "In modern computer security, a hard-fought broad-based consensus has been established: Despite the intuitive idea that hiding a system should protect it, transparency is often more beneficial for protection. The consensus on this general principle is broad, though perspectives on how to implement the principle in specific contexts can be more varied." https://doi.org/10.1609/aaai.v39i27.35022 
* In research: Open Science + Safety + Security = As open as possible, as closed as necessary.

```{exercise} gpt-oss-safeguard
* Open-weight safety reasoning models
* Trained to reason about safety
* Support custom safety policies
* Configurable reasoning effort
* Apache 2.0 license
* Test it: https://huggingface.co/spaces/openai/gpt-oss-safeguard-20b 
* Sample policy: https://github.com/openai/gpt-oss-safeguard/blob/main/example_policies/spam/policy.txt 
```

```{exercise} ❓ Quiz

A researcher is an open science enthusiast and shares code, data, and model weights of an in-house developed AI system openly and in accordance with FAIR principles. How can dual-use risks be prevented?
* Open science automatically prevents misuse
* Share only model weights, but not data
* Apply risk mitigation measures to every stage of AI lifecycle
* Avoid publishing AI research entirely
```

## AI Security Exchange

### Threat model: Types of threats

Three types of threats (https://owaspai.org/goto/threatsoverview):
1. threats during development-time: when data is obtained and prepared, and the model is trained/obtained. Example: data poisoning (injecting bad data into the training data)
2. threats through using the model: through inference; providing input and getting the output. Examples: 
   * direct prompt injection (malicious prompt into the user interface), 
   * indirect prompt injection (malicious prompt is embedded in external content) or
   * evasion (hidden malicious instructions via obfuscation, encoding, hidden text, and payload splitting)
3. other threats to the system during runtime: in operation - not through inference. Example: stealing model input

### Threat model: Impacts

6 types of impacts that align with three types of attacker goals (disclose, deceive and disrupt):
1. disclose: hurt confidentiality of train/test data
2. disclose: hurt confidentiality of model Intellectual property (the model parameters or the process and data that led to them)
3. disclose: hurt confidentiality of input data
4. deceive: hurt integrity of model behaviour (the model is manipulated to behave in an unwanted way and consequentially, deceive users)
5. disrupt: hurt availability of the model (the model either doesn’t work or behaves in an unwanted way - not to deceive users but to disrupt normal operations)
6. disrupt/disclose: confidentiality, integrity, and availability of non AI-specific assets

``` {figure} threats.png
:width: 100%
```

### Threats to agentic AI

Threats:
* Hallucinations and prompt injections can change commands or even escalate privileges. 
* Leak of sensitive data due to the „lethal trifecta“:
   * Data: Control of the attacker of data that find its way into an LLM at some point in the session of a user that has the desired access, to perform indirect prompt injection
   * Access: Access of that LLM or connected agents to sensitive data
   * Send: The ability of that LLM or connected agents to initiate sending out data to the attacker

```{exercise} ❓ Quiz

Which security risk is introduced when researchers use an AI system (e.g., an agentic research assistant or coding assistant such as Cursor) that has unrestricted access to local files, code repositories, and credentials?
* Reduced model accuracy 
* Increased energy consumption 
* Unauthorized data access and data exchange with third parties
* Loss of explainability
```

```{exercise} ❓ Quiz

Which of the following is a core AI security concern (as opposed to AI safety)?
* Bias against minority groups
* Misleading scientific conclusions
* Intentional misuse or exploitation of AI systems by adversaries
* Lack of reproducibility
```
