# Red Teaming Large Language Models

## Table of contents:
- [Configuring solution environment]((https://github.com/Max-Headspace/GPT-RedTeaming-Concepts-1/tree/main#configuring-solution-environment)
- [Lesson 1: Overview of LLM Vulnerabilities]((https://github.com/Max-Headspace/GPT-RedTeaming-Concepts-1/tree/main#lesson-1-overview-of-llm-vulnerabilities)
- [Lesson 2: Red Teaming LLMs]((https://github.com/Max-Headspace/GPT-RedTeaming-Concepts-1/tree/main#lesson-2-red-teaming-llms)
- [Lesson 3: Red Teaming at Scale]((https://github.com/Max-Headspace/GPT-RedTeaming-Concepts-1/tree/main#lesson-3-red-teaming-at-scale)
- [Lesson 4: Red Teaming LLMs with LLMs]((https://github.com/Max-Headspace/GPT-RedTeaming-Concepts-1/tree/main#lesson-4-red-teaming-llms-with-llms)
- [Lesson 5: A Full Red Teaming Assessment]((https://github.com/Max-Headspace/GPT-RedTeaming-Concepts-1/tree/main#lesson-5-a-full-red-teaming-assessment)

## Configuring solution environment
1. To use Azure OpenAI backend, assign the API endpoint name, key and version, along with the Azure OpenAI deployment names of GPT and Embedding models to **AZURE_OPENAI_API_BASE**, **AZURE_OPENAI_API_KEY**, **AZURE_OPENAI_API_VERSION**, **AZURE_OPENAI_API_DEPLOY** (for GPT) and **AZURE_OPENAI_API_DEPLOY_EMBED** (for Embedding) environment variables respectively.
2. Install the required Python packages, by using the **pip** command and the provided requirements.txt file.
```
pip install -r requirements.txt
```

## Lesson 1: Overview of LLM Vulnerabilities
First lesson provides an overview of LLM vulnerabilities. It describes hypothetical scenarios, causes of observed behaviour and potential impact. Four main categories of described LLM vulnerabilities are:
- Bias and stereotypes;
- Sensitive information disclosure;
- Service disruption;
- Hallucinations.

## Lesson 2: Red Teaming LLMs
Second lesson focuses on the aspects of LLM Red Teaming. It explores different techniques to bypass the model's safeguards:
- Exploiting text completion;
- Using biased prompts;
- Direct prompt injection;
- Grey box prompt attacks;
- Advanced technique: prompt probing.

## Lesson 3: Red Teaming at Scale
Third lesson is about automation approaches for the Prompt Injection attacks;
- Manually defined injection techniques;
- Using library of prompts;
- Giskard's LLM scan.

## Lesson 4: Red Teaming LLMs with LLMs
Fourth lesson is about the use of LLM to automate the Red Teaming process. Here you can find how to use custom scripting to automate generation of adversarial inputs and evaluation of the app's outputs. Then it's shown how the same process can be automated by using Giskard's Python library.

## Lesson 5: A Full Red Teaming Assessment
Fifth lesson provides an example of a full Red Teaming assessment. It consists of 2 rounds:
- Round one is about more general probing of the company bot, to search for any signs of vulnerabilities in various categories, e.g. toxicity and offensive content, off-topic content, excessive agency, sensitive information disclosure, etc. You can use either custom prompts or automate prompts generation with Giskard's Python library;
- Round two is about exploiting specific functionality, e.g. prompt injection, to achieve a malicious goal. In this fictitious scenario, we persuade the bot to refund the order, even if it's not eligible any more.
