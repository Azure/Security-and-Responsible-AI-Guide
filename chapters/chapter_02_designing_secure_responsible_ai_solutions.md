---
nav_order: 3
has_children: false
title: Chapter 2 - Designing Secure, Responsible AI Solutions
permalink: /chapters/chapter_02_designing_secure_responsible_ai_solutions
layout: default
---

# Chapter 2: Designing Secure, Responsible AI Solutions

{% include table_of_contents.md %}

Artificial intelligence has the potential to transform the way that customers interact with services provided by ISVs and Digital Natives. But, as with any technology, it comes with significant risks and challenges. The [National Cyber Security Centre in the UK](https://www.bbc.com/news/technology-66166824) identified that security is essential for building robust AI systems, and the risks of not designing with security in mind could be significant to your organization and your customers.

For organizations building solutions with AI capabilities, you have the responsibility to ensure that your implementations are secure and trustworthy. This chapter provides guidance on how to design secure, responsible AI solutions on Azure.

![Designing Secure, Responsible AI Solutions](../media/chapter_02.jpg)

## Assessing the responsible AI impact of your solutions

The first step in designing a responsible AI solution is to explore the potential impact of your solution on your customers. This will help you to identify the risks and challenges that you need to address early in the design process.

Microsoft's [Responsible AI Impact Assessment Guide](https://blogs.microsoft.com/wp-content/uploads/prod/sites/5/2022/06/Microsoft-RAI-Impact-Assessment-Guide.pdf), and corresponding [Impact Assessment Template](https://blogs.microsoft.com/wp-content/uploads/prod/sites/5/2022/06/Microsoft-RAI-Impact-Assessment-Template.pdf) provide a framework for you to assess the potential impact that your AI use case may have, aligned to Microsoft's [principles for responsible AI](https://www.microsoft.com/en-us/ai/responsible-ai) as discussed in the previous chapter. It is a tool to:

- **Explore** the potential impact of your system on people and society, giving you the opportunity to consider both benefits and harms for different individuals and groups.

- **Identify** the relevant goals and requirements for your solution from Microsoft's principles for responsible AI including fairness, reliability and safety, privacy and security, inclusiveness, transparency, and accountability.

- **Document** your AI use case responsibility profile, data requirements, potential limitations and failures, and potential misuse scenarios.

- **Communicate** across your organization and stakeholders on the impact, challenges, and mitigation for your use case to ensure that you are building a responsible AI solution.

The Responsible AI Impact Assessment should be completed collaboratively by your team members with varying perspectives and expertise. As your system and use cases evolve, you should revisit the assessment to ensure that you are still committed to building a responsible AI solution. Adopting this process will help to make well informed decisions and guide responsible AI practices throughout the development lifecycle of your solution.

## Designing Azure OpenAI solutions with responsibility in mind

Building on your [understanding of responsible AI principles](./chapter_01_understanding_security_and_responsible_ai#responsible-ai-principles-and-frameworks), when designing generative AI solutions with Azure OpenAI, it is important to consider the potential risks and challenges that you need to address early in the design process. Microsoft lays out a [comprehensive set of guidelines](https://learn.microsoft.com/en-us/legal/cognitive-services/openai/overview) to help you design and deploy responsible AI solutions using Azure OpenAI.

Azure OpenAI's GPT models are powerful generative AI models that can produce high-quality content and code, but they also pose significant challenges, such as generating harmful, inaccurate, or misleading content, or being used for malicious purposes. To mitigate these risks, you need to follow a systematic process to identify, measure, and mitigate potential harms, and to operate your system with appropriate safeguards and transparency.

When designing AI solutions using Azure OpenAI, consider:

- **Review the Azure Well-Architected Framework guidance**: Azure Engineering provides [a comprehensive design guide for integrating Azure OpenAI](https://learn.microsoft.com/en-us/azure/well-architected/service-guides/azure-openai) into solutions following the pillars of security, reliability, performance efficiency, cost optimization, and operational excellence. This guide provides best practices and design patterns to help you build secure, reliable, and efficient AI solutions using Azure OpenAI.

- **Understanding models and their limitations**: Review the [Microsoft Transparency Note for the Azure OpenAI model](https://learn.microsoft.com/en-us/legal/cognitive-services/openai/transparency-note?context=%2Fazure%2Fcognitive-services%2Fopenai%2Fcontext%2Fcontext&tabs=text) you are using, and educate yourself about its capabilities, limitations, and safety challenges.

- **Adopting content filters**: Leverage the resource-level content filters provided by Azure OpenAI to block or flag harmful or problematic content generated by models. To understand this in [more detail, read on to chapter 3](./chapter_03_identifying_and_assessing_ai_risks#implementing-azure-openai-content-filters-to-mitigate-harmful-content).

- **Craft effective prompts and metaprompts**: Use prompt engineering techniques to guide the model's behavior and output towards your intended goals and expectations, and to avoid undesired or harmful outputs.

- **Implement user-centered design and UX interventions**: Design the user experience to encourage users to review AI-generated outputs, to disclose the role of AI in the interaction, to prevent over-reliance or misuse of the system, and to provide feedback channels.

- **Deploy and operate your system responsibly**: Follow a phased delivery approach, develop an incident response and rollback plan, collect telemetry and feedback data, and monitor your system for any regression or new harms.

- **Opt-in to the Customer Copyright Commitment**: To avoid potential risks and maintain coverage under Microsoft's Customer Copyright Commitment, you should [implement the required mitigations](https://learn.microsoft.com/en-us/legal/cognitive-services/openai/customer-copyright-commitment?context=%2Fazure%2Fai-services%2Fopenai%2Fcontext%2Fcontext#universal-required-mitigations) to ensure that your metaprompts prevent copyright infringement, and that you have a process in place to handle testing and evaluation of your system. These mitigations help you to configure your system to respect intellectual property in compliance with the Code of Conduct.

## The importance of security in AI

Security in AI is a crucial aspect of ensuring the reliability and trustworthiness of your AI systems. AI security involves protecting systems from malicious attacks, as well as ensuring that they respect the responsible AI principles and user privacy.

The [Must Learn AI Security blog and book series](https://github.com/rod-trent/OpenAISecurity/tree/main/Must_Learn) provides a comprehensive and educational guide for anyone interested in learning about the various types of attacks against AI systems and how to design and implement security to protect against them. In the series, Rod Trent dives deep with real-world examples and practical guidance on common attacks including:

- **Prompt Injection**: Particularly prevalent in solutions using large language models, such as GPT-4, prompt injection attacks involve manipulating the input prompts to AI systems to generate malicious or misleading outputs.

- **Evasion**: Even with safeguards in place, attackers can evade the detection of them by disguising their attacks as legitimate inputs or exploiting blind spots in the system.

- **Model Inversion**: With reverse engineering techniques, attackers can infer sensitive information from the outputs or parameters of your AI model, such as the data used for training or the weights of the model.

- **Denial of Service**: By overloading your AI system with invalid or malicious requests, attackers can cause it to fail or become unavailable to your users.

- **Impersonation**: AI systems can be deceived into thinking that an attacker is a legitimate user, allowing them to exploit the system to gain unauthorized access to data or resources.

As the AI landscape continues to evolve and grow, so do the threats against AI systems. It is essential for you to understand the challenges and risks that are posed by these attacks, and how you can continue to build secure AI systems that are resilient to them. The series is continuously updated with new and relevant AI security research and guidance to help you stay up to date with mitigating techniques.

## Designing security into your Azure OpenAI solutions

If you are developing or deploying generative AI applications using Azure OpenAI or other large language models (LLMs), you need to consider the security challenges and risks that come with these powerful tools. Generative AI applications can enable various scenarios such as content creation, summarization, translation, question answering, and conversational agents. However, they also pose significant security challenges that need to be addressed by developers and administrators of GenAI applications. [Freddy Ayala, a cloud solution architect at Microsoft, explores these challenges in his article](https://techcommunity.microsoft.com/t5/azure-architecture-blog/security-best-practices-for-genai-applications-openai-in-azure/ba-p/4027885) and provides guidance on:

- Protecting the confidentiality and integrity of the data used to train and query models on Azure OpenAI

- Ensuring the availability and reliability of Azure OpenAI services and the applications that consume them

- Preventing the misuse or abuse of the models by malicious actors or unintended users

- Monitoring and auditing the outputs and behaviors of Azure OpenAI models for quality, accuracy, and compliance

- Designing with responsible AI in mind for outputs generated by Azure OpenAI models

By following Freddy's guidance, you can design security and responsible AI in your generative AI applications and their data, network, access, application, and governance domains. You will also learn how to architect solutions using Azure's security services and features, such as Azure Key Vault and Azure Sentinel, to enhance your security posture and mitigate potential threats.

## Best practices for designing responsible, secure AI solutions

Secure AI design is the process of designing AI systems that are robust, fair, transparent, and privacy-preserving. It involves integrating security practices at every stage of the AI development lifecycle, from design to deployment.

Omar Santos provides a [comprehensive suite of best practices for security in AI](https://github.com/The-Art-of-Hacking/h4cker/tree/master/ai_research/AI%20Security%20Best%20Practices) which provides guidance on how to design secure AI systems that can be applied to both model training as well as consuming deployed AI models in productions. These best practices include:

- **Protecting data privacy**: The data used to train or feed your AI system should contain the minimum amount of information required to achieve your goals. Anonymization and minimization techniques can be used to reduce the risk of re-identification in your data to safeguard against unauthorized access or leakage.

- **Building robustness**: AI systems should be designed to be robust against attacks that aim to manipulate the system or cause it to fail. You should consider the potential risks and threats to your system and implement appropriate controls to mitigate against them.

- **Mitigate societal bias and ensure fairness**: Tools such as the [Responsible AI Dashboard](https://github.com/microsoft/responsible-ai-toolbox#introducing-responsible-ai-dashboard) can be used to measure societal bias and fairness in your AI system. These tools enable you to consider the impact your system may have on different groups of people, and ensure that the system does not discriminate or cause harm.

- **Provide transparency and explainability**: Design your AI systems to provide clear and understandable explanations for its predictions and decision making process. Features such as [content credentials in Azure OpenAI service](https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/content-credentials) provide a tamper-evident way to disclose the origin and history of content generated by the service. Building trust with your customers is essential to the success of your AI system, and transparency is key to building that.

- **Secure AI infrastructure**: Security should be built into every layer of your AI system, from the data source to the deployed model endpoint. Follow [Microsoft Azure's Well-Architected Framework guidance on securing your data and systems](https://learn.microsoft.com/en-us/azure/well-architected/security/) to ensure that your AI systems are designed and implemented with confidentiality, integrity, and availability in mind.

- **Establish an incident response plan**: You should have a plan in place to respond to security incidents in your AI systems. This plan should include a process for reporting incidents, investigating them, and taking appropriate action to mitigate against future incidents. Conduct regular security audits and update your system to address any vulnerabilities that are discovered.

## Conclusion

The integration of secure and responsible AI practices are essential for designing any AI solution. The potential risks and challenges that are posed by building new AI systems can have significant consequences for your organization and your customers. Designing secure, responsible AI solutions requires you to consider the potential impact, risks and challenges that you need to address early in the design process. It is imperative for organizations to not only adhere to these best practices but also to engage in ongoing research and development to stay ahead of the evolving threat landscape and ensure the responsible and secure deployment of AI technologies.
