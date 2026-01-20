# Introduction

+++ {"part": "abstract"}

AI tools increasingly support all stages of research projects. At the same time, their use is constrained by ethical principles, research-integrity standards, and governance (legal and regulatory) requirements. This workshop introduces these constraints, presents the risks of AI use in research, and provides practical strategies for mitigating them across the entire research lifecycle. Both unintentional harms (AI safety) and deliberate threats (AI security) will be addressed. Participants will learn how to use AI tools safely, securely, and in compliance with ethical, integrity, and governance expectations.

+++

+++ {"part": "availability"}

GitHub: https://github.com/shigapov/safe_ai/. Zenodo: https://doi.org/10.5281/zenodo.17940942.

+++

## Basic definitions

There exist many definitions of AI. None of them are perfect. But when we talk about AI, we often mean AI systems.

AI system
: is a special type of information technology (IT) system consisting of hardware, software, data, AI model(s) and networks, which can (not necessarily deterministically) generate outputs based on data it receives and data it was trained on.

Local AI system
: runs fully on a device you control, meaning you also have more control over its safety and security.

Cloud AI system
: runs on remote infrastructure managed by a provider. Using a cloud AI system means trusting a complex supply chain of hardware, software, data, models, and networks that you do not control.

An Agentic AI system
: is an AI system that can set or interpret goals, plan actions, and carry out tasks with minimal human intervention or autonomously. To achieve these goals, it may interact with other IT systems via networks or execute code and communicate with software components locally on an IT system. Agentic AI may use multiple models, including a router model that decides which model or tool to use next.

An AI model
: consists of the model architecture, model parameters (including weights) and inference code for running the model. AI weights are the set of learned parameters that overlay the model architecture to produce an output from a given input. Source: https://opensource.org/ai/open-source-ai-definition

An Open Source AI
: is one made freely available with all necessary code (for data pre-processing; training, validation, and testing; inference; supporting libraries and tools), data (datasets, data card, technical report, and research paper) and model (architecture and parameters) under legal terms approved by the Open Source Initiative. Source: https://opensource.org/ai/open-source-ai-definition

Generative AI system
: is a special type of AI system, which was trained to generate content (text, image, audio, video, code, etc.).

(Pre-)training
: “Developers feed models massive amounts of diverse data – such as text, code, and images – to instil general knowledge. Pre-training produces a ‘base model’. This is a highly compute-intensive process.“ See {cite:p}`bengio_international_2025`.

Fine-tuning
: „Developers further train the base model to optimise it for a specific application or make it more useful generally. This is typically done with the help of a large amount of human-generated feedback. This is a moderately compute-intensive and highly labour-intensive process.“ See {cite:p}`bengio_international_2025`.

A Retrieval-Augmented Generation (RAG) system
: is an AI system that retrieves relevant information from either static sources (e.g., a local vector database) or dynamic sources (e.g., internet search), and uses this retrieved information to augment the model’s internal knowledge when generating outputs.
The model parameters are not updated in RAG.

## Reproducibility and replicability of AI systems

``` {figure} ./figures/reproducible-definitiongrid.jpg
:width: 100%
```

Image source: {cite:p}`the_turing_way_community_2024_13882307`.

Various aspects influence reproducibility of outputs in AI systems:

1. Pseudorandomness in computers:
   * Computers use pseudorandom sequences, not true randomness. 
   * A random seed initializes the sequence.
2. GenAI models choose tokens by sampling from probability distributions:
   * Temperature sampling: adjusts shape of the distribution. Higher temperature flattens distribution, making generator more random. Lower temperature sharpens distribution, making generator more deterministic.
   * Top-K sampling: samples from the K most likely tokens.
   * Top-P sampling: samples from the smallest set of tokens whose cumulative probability ≥ P.
3. Floating-point non-associativity (a+b)+c ≠ a+(b+c) in GPUs, TPUs, and CPUs:
   * https://doi.org/10.64434/tml.20250910
   * https://doi.org/10.48550/arXiv.2506.09501

```{exercise} Testing reproducibility of an AI system at your laptop
* Let’s choose an open-weight model from from the European Open Source AI index (https://osai-index.eu/the-index). Olmo-3-1125-32B is the current number one. Test it via https://huggingface.co/allenai/Olmo-3-1125-32B. 
* If that model is too big for your laptop, let‘s choose a smaller Olmo 7b model provided by ollama as well. First, install ollama https://ollama.com. Then, run “ollama run olmo2:7b”.
* Adapt the script on the right side and test multiple runs with different parameters. Check the definitions of parameters and find their combination providing reproducible outputs.

```

To access your local ollama instance via API, you can use the code:

```python
import requests


def query(prompt: str):
    url = "http://localhost:11434/api/generate"
    payload = {
        "model": "olmo2:7b",
        "prompt": prompt,
        "stream": False,
        "options": {
            "seed": 42,
            "temperature": 1,
            "top_k": 10,
            "top_p": 1,
        }
    }

    resp = requests.post(url, json=payload)
    resp.raise_for_status()
    data = resp.json()
    return data["response"]
```

For your reproducibility tests, you can adapt:

```python
from collections import Counter

def test_reproducibility(prompt: str, runs: int = 10):
    outputs = []

    print(f"Running reproducibility test for prompt:\n{prompt}\n")

    for i in range(runs):
        out = query(prompt)
        outputs.append(out)
        print(f"Run {i+1}:")
        print(out.strip()[:300] + ("..." if len(out) > 300 else ""))
        print("-" * 40)

    # Count unique outputs
    counts = Counter(outputs)
    print("\n=== Summary ===")
    print(f"Total runs: {runs}")
    print(f"Unique outputs: {len(counts)}\n")

    for text, count in counts.items():
        print(f"Occurrences: {count}")
        print("Sample:")
        print(text.strip()[:300] + ("..." if len(text) > 300 else ""))
        print("-" * 40)


# Run the reproducibility test
test_reproducibility("What is reproducibility of an LLM?", runs=10)
```

##  Safe and secure AI system

There are no zero-risk AI systems. The only fully safe and fully secure AI system is the one that is never used. But modern research and everyday life rely increasingly on AI systems. Therefore, it is important to identify AI risks and learn how to manage them.

Safety and security of AI system include safety and security of its components: hardware, software, data (including training, validation, testing, augmented, input, output, and database), models, and networks. This makes the topic very complex.

Safe and secure use of AI in research (projects) is shaped by ethical, integrity, and governance (legal and regulatory) requirements and expectations. They are complex as well.

## AI Safety and AI Security

According to {cite:p}`lin_ai_2025` AI safety considers risks from accidental or unintended behaviors. AI Security deals with risks from intentional or adversarial actions by malicious actors

## Safety and security in context of research

The trinity of good research: Research ethics, research integrity, and research governance {cite:p}`kolstoe_trinity_2024`. Safety and security are parts of all of them.

## Risk management

[OWASP AI Risk Analysis page](https://owaspai.org/goto/riskanalysis/) describes the Risk Management Framework:
* Identifying Risks
* Evaluating Risks by Estimating Likelihood and Impact
* Deciding What to Do (Risk Treatment):
   * Risk Mitigation,
   * Transfer, 
   * Avoidance,
   * Acceptance. 
* Risk Communication and Monitoring

We cannot treat risks unless we can identify them. We identify risks within research ethics, research integrity, and research governance. The general risks in AI safety and AI security will be also introduced. In Part 2 we do risk management across the entire research lifecycle.

## Defense in depth

Defense in depth
: is a risk-mitigation approach that relies on multiple, overlapping, and complementary layers of safeguards, so that if one control fails, others remain effective.

**Key assumption:** any single mitigation measure can fail.

Dimensions of defense in research (projects) for an AI use case:
* **People:** individual researchers, research teams, project partners, and participants
* **Infrastructure/Technology:** hardware, software, data, models, networks, and the entire supply chain
* **Processes:** research process including research ethics, research integrity, and research governance

## Risk management framework adapted to the trinity of risks in research (projects)

* **Identifying Risks:** Recognizing potential risks related to research ethics, research integrity, and research governance. 
* **Evaluating Risks:** Subjectively as low, medium, high.
* **Risk Treatment:** Choosing an appropriate strategy to address the risk:
   * Risk Mitigation,
   * Transfer (to another party),
   * Avoidance (eliminating the source),
   * Acceptance.
* **Risk Communication and Monitoring:** Regularly sharing risk information with stakeholders. Creating a Risk Register, a list of risks and their attributes (e.g. severity, treatment plan, ownership, status, etc). 

This framework is adapted specifically for research context from the Risk management framework: https://owaspai.org/goto/riskanalysis/  


```{note}
Note: Any mitigation measure can fail. Apply defense in depth to all three dimensions (people, technology, and processes) in Risk Mitigation.
```

## Questions

Before you use any AI system, ask yourself the following questions:
* Is the hardware safe and secure?
* Is the software safe and secure?
* Is the data (including training, validation, testing, augmented, input, and output) safe and secure?
* Is the model safe and secure?
* Are the networks safe and secure?

There are three kinds of AI systems:
* **Cloud AI:** Choose a compliant provider (check certifications and trust portals) + use case
* **Local AI (self-built):** You are responsible for safety, security, and use case
* **Hybrid (Local AI with third-party open-weight models):** Shared responsibility (see licenses)
