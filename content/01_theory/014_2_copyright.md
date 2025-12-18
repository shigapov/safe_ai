# Intellectual property rights and copyright

Intellectual property rights (IPR) are legal rights that protect creations of the mind such as inventions, publications, datasets, software, designs, and trademarks.
Typical IPRs are copyright (publications, presentations, datasets [exception: facts are public domain], and software), patent rights, design rights, trademarks (names and logo), database rights, and trade secrets.
In EU countries, copyright protects your intellectual property until 70 years after your death or 70 years after the death of the last surviving author in the case of a work of joint authorship.
Outside of the EU, in any country which signed the Berne Convention, the duration of copyright protection can vary but it lasts until at least 50 years after the author's death. See also https://eur-lex.europa.eu/EN/legal-content/summary/copyright-and-related-rights-in-the-information-society.html 

## Directive 2001/29/EC on the harmonisation of certain aspects of copyright and related rights in the information society (InfoSoc)

* Art. 2-4: Authors and neighboring rightsholders have the reproduction right, the right of communication to the public and the distribution right (see Directive 2001/29/EC InfoSoc).
* Art. 5 (1): There is a mandatory exception to the right of reproduction for certain temporary acts of reproduction which are an integral and essential part of a technological process (temporary copies), and which aim to enable a lawful use or a transmission in a network between third parties by an intermediary, of a work or other subject matter.

## Directive (EU) 2019/790 on copyright in the Digital Single Market

The directive makes it easier to use copyright-protected material for different purposes, mostly related to access to knowledge, by introducing mandatory exceptions to copyright to foster:
* text- and data-mining (TDM);
* digital uses of works for the purpose of illustration for teaching; and
* the preservation of cultural heritage.

TDM
: is “any automated analytical technique aimed at analysing text and data in digital form in order to generate information which includes but is not limited to patterns, trends and correlations“, Art. 2 (2))

## Text and data mining for the purposes of scientific research

Art. 3 of the CDSM:
* (1) Exception for reproductions and extractions made by research organisations and cultural heritage institutions in order to carry out, for the purposes of scientific research, text and data mining of works or other subject matter to which they have lawful access.
* (2) Copies of works or other subject matter made in compliance with paragraph 1 shall be stored with an appropriate level of security and may be retained for the purposes of scientific research, including for the verification of research results.
* (3) Rightholders shall be allowed to apply measures to ensure the security and integrity of the networks and databases where the works or other subject matter are hosted. Such measures shall not go beyond what is necessary to achieve that objective.

## Exception or limitation for text and data mining

Art. 4 of the CDSM:
* (1) Exception for reproductions and extractions of lawfully accessible works and other subject matter for the purposes of text and data mining.
* (2) Reproductions and extractions made pursuant to paragraph 1 may be retained for as long as is necessary for the purposes of text and data mining.
* (3) The exception or limitation provided for in paragraph 1 shall apply on condition that the use of works and other subject matter referred to in that paragraph has not been expressly reserved by their rightsholders in an appropriate manner, such as machine-readable means in the case of content made publicly available online.

## Opt-out measures in practice

No single opt-out mechanism has emerged as the sole standard used by rights holders:
1. Technical measures:
   * The Robots Exclusion Protocol (REP) (https://doi.org/10.17487/RFC9309)
   * TDM reservation protocol (https://github.com/w3c/tdm-reservation-protocol)
2. Legally-driven measures: 
   * unilateral declarations by copyright holders
   * licensing constraints
   * website terms and conditions

## Tool: TDM exception decision tree for researchers

https://doi.org/10.5281/zenodo.12759960

## EUIPO’s copyright perspective on AI

Summary of opinion is available at https://www.euipo.europa.eu/en/publications/genai-from-a-copyright-perspective-2025:

* No ‘one-size-fits all’ solution for copyright holders to protect their rights has emerged yet. 
* Instead, different approaches and solutions are developing for copyright holders to protect their rights, and for AI developers to respect their regulatory obligations.
* On the one side, the rights reservation mechanisms for the INPUT phase (related to training AI models), whereby rightsholders can express their opt out from the ‘text and data mining’ (TDM)-exception.
* On the other side, transparency measures exist for the OUTPUT phase that allow the indication and recognition of AI generated content.

The opinion is published in https://data.europa.eu/doi/10.2814/3893780.

## Case Study: LAION v. Kneschke (Hamburg district court, 27 Sept 2024, 310 O 227/23)

* Background: 
   * Photographer Robert Kneschke sued LAION (https://laion.ai), a non-profit that creates AI training datasets using web-scraped publicly available images or the Common Crawl.
   * His allegation: LAION reproduced his image without permission while building its dataset https://laion.ai/blog/laion-5b .
* Court’s Decision: LAION’s activity (dataset creation) is protected under Section 60d UrhG (TDM for scientific research) implementing Article 3 CDSM Directive.
* Note: The shared dataset contains only metadata (e.g., URLs), not the images.
* Preliminary conclusion: TDM exception seems to be applicable for dataset creation. Though in this case the dataset contained only metadata. But there are also model training and model inference in AI lifecycle. 

## Case Study: GEMA v. OpenAI (Munich district court, 11.11.2025, 42 O 14139/24)

* Background:
   * GEMA, the collective management organisation for musical copyrights, sued OpenAI, alleging ChatGPT was trained on copyrighted German song lyrics.
   * The lyrics allegedly reappeared (sometimes verbatim) in ChatGPT outputs.
* Court‘s decision: Copyright infringement in both training and output. The court granted injunction, disclosure, and damages.
* Takeaways:
   * GPT-4 and GPT-4o were shown to reproduce copyrighted lyrics (“memorization”). Memorization is reproduction.
   * No justification of training via TDM exception.
   * Trainer of the models and deployer of the AI systems OpenAI was liable.
* Preliminary conclusion: Using copyrighted works for AI model training (for commercial purposes) is not permitted.

## Is “training an AI model” equal to “TDM”?

* It is complicated. 
   * If “yes”, then Art. 3 CDSM will allow training an AI model using copyrighted works for research purposes without any opt-out of rightsholders. 
   * If “not”, Art. 3 and Art. 4 will be irrelevant. Then, to train an AI model with copyrighted works, one needs to find other lawful ways to make it. For example, via contracts with explicit permission to use copyrighted works for training.

From the one side, there exist strong opinions against TDM=MT: “While GenAI training shares some methodological overlaps with TDM, its objectives and outputs significantly diverge. The legal and conceptual frameworks governing TDM and fair use may not seamlessly extend to generative AI, particularly given its potential to compete with and replicate the expressive elements of copyrighted works.” https://doi.org/10.48550/arXiv.2502.15858 and http://dx.doi.org/10.2139/ssrn.4993782.
From the other side, http://dx.doi.org/10.1093/grurint/ikaf114 when Art. 4 DSM is considered together with Art. 53 EU AI Act, then there is an opinion that Art. 4 DSM applies to model training.

Okay, it’s complicated, but what shall we do with model training for research purposes?

* The permissibility is not yet fully clear. The opinions differ. But:
* If you need copyrighted works for AI model training, get contractual permissions.
* If you take the risk of interpreting “AI model training” as TDM and of using the TDM exception for research purposes, make sure that:
* Requirements for the TDM exception are met (e.g., lawful access to copyrighted works)
* You don’t train a model with a third-party infrastructure.
* You train an open-weight model at a local secure hardware.
* You don’t share or archive the trained model before the legal basis for this is clarified.
* There is a need for case-by-case assessment and risk balancing.

Some of these recommendations are adapted from the talk "KI im Urheberrecht: Rechtsrahmen für Bibliothek und Wissenschaft" by Dr. Marion von Francken-Welz presented at UB Mannheim in April 2025.

## License agreements and contracts

See the full text in https://doi.org/10.5281/zenodo.13837688.

* A blanket reference in the contract to the term "artificial intelligence" is unsuitable. One should specify concrete user acts that are to be permitted or prohibited by the contract.
* Contracts cannot effectively prohibit end users from using texts or images made available from databases as input data for AI for adaptation and transformation.
* Contracts concluded from 1 March 2018 onwards cannot effectively restrict the use of copyrighted works by TDM for scientific purposes, including the creation of internal scientific AI systems. Making reproductions available to third parties without contractual permission is only permitted under the conditions set out in section 60d (4) UrhG.
* Contracts can effectively make provision for the use of copyrighted works for TDM for non-scientific purposes.
* Contracts can provide for measures that ensure the security and integrity of the networks and databases through appropriate security precautions and set guidelines for the copies made in the context of TDM.

## RAG and copyright

There is no clear reference to RAG as a form of TDM in the existing agreements between AI developers and rightsholders.
* Static RAG may trigger more copyright-restricted acts compared to dynamic RAG. Reasons: 
   * Locally hosted content often necessitates a longer retention of reproductions to enable ongoing reference, a requirement that may exceed the conditions of applicability of the CDSM Directive Article 4 TDM exception, as well as the (more strict) requirements for the applicability of the InfoSoc temporary reproduction exception.
   * By contrast, scraping the open internet for context references in dynamic RAG typically retains content only temporarily, aligning more closely with potential for application of either TDM or temporary reproduction exceptions.

## More resources on copyright

* EUIPO Copyright Knowledge Centre (https://www.euipo.europa.eu/en/copyright-knowledge-centre)
* Künstliche Intelligenz im Verlagsbereich: Häufig gestellte Fragen zu generativer KI https://www.boersenverein.de/beratung-service/recht/kuenstliche-intelligenz 
* Brehm, E. (2022). Guidelines zum Text und Data Mining für Forschungszwecke in Deutschland. https://doi.org/10.34657/9388 

```{exercise} ❓ Quiz

Is it legal to use copyrighted works to create a dataset for training an AI model?
* Yes, always
* No, never
* Only under specific legal conditions
* It is complicated
```

```{exercise} ❓ Quiz

Is it legal to use copyrighted works to train an AI model?
* Yes, always
* No, never
* Only under specific legal conditions
* It is complicated
```

```{exercise} ❓ Quiz

Is it legal to use outputs of an AI system containing copyrighted works?
* Yes, always
* No, never
* Only under specific legal conditions
* It is complicated
```

