---
nav_order: 4
has_children: false
title: Chapter 3 - Identifying and Assessing AI Risks
permalink: /chapters/chapter_03_identifying_and_assessing_ai_risks
layout: default
---

# Chapter 3: Identifying and Assessing AI Risks

{% include table_of_contents.md %}

AI solutions are increasingly being adopted and used in critical industries, but they are not immune to security threats. Common security threats like data breaches, unauthorized access, and adversarial attacks have even more exposure with AI-powered solutions whereby actions in the system could be undetermined. Consumers of your AI solutions need to be confident that the system is secure and that their data is protected.

Mitigating these risks requires teams to consider approaches to identifying potential security threats to their AI systems, assess the impact, and establish best practices to mitigate them. This chapter explores useful resources that will help teams to establish a process for identifying and assessing risks in their Azure AI solutions.

![Identifying and Assessing AI Risks](../media/chapter_03.jpg)

## Assessing the risks of machine learning models

Solutions that take advantage of AI can offer benefits for various domains and applications, but they also pose significant risks and challenges. To ensure the accountability of machine learning models built for these systems, data scientists and machine learning professionals need to assess and debug their models and data before deploying into a production environment.

The [Responsible AI Dashboard](https://learn.microsoft.com/en-us/azure/machine-learning/concept-responsible-ai-dashboard?view=azureml-api-2) is a tool that brings together several mature tools including data analysis, model fairness, error analysis, and counterfactual what-if. Available within Azure Machine Learning, the dashboard takes advantage of these tools to provide a comprehensive view of the challenges and risks that your machine learning model may have. Using this tool can help you to not only identify, but also improve the overall effectiveness of your model through data-driven insights.

Great use cases for the Responsible AI Dashboard include:

- **Identifying the fairness of predictions**: It is important to understand the potential harms that may arise from using a model that makes more errors for certain individuals. The dashboard can help to identify how your model may expose societal bias and fairness issues using various group-fairness metrics across sensitive features.

- **Diagnosing and debugging model errors across different features**: The dashboard can help you to identify the most impactful features that cause errors in your model. This helps you to understand the predictions that your model makes and how you can improve them to provide a more accurate, reliable, and trustworthy model.

- **Understanding how your model makes decisions**: To build trust with your customers, it is important to identify and assess how your model predicts a result and how changes to the input can alter the outcomes. The dashboard provides capabilities to provide such explanations and insights into your model that is easy to understand and interpret.

The Responsible AI Dashboard emerges as a valuable tool, empowering teams to assess and mitigate risks to build trustworthy models, fostering responsible AI practices. As you continue to advance AI technologies, prioritizing responsible and transparent practices remains imperative for establishing trust and maximizing the positive impact of AI in your solutions.

## Identifying risks in AI solutions leveraging large language models

The era of generative AI is enabling new and existing systems to take advantage of powerful pre-trained models capable of generating natural language. Trained on massive amounts of text data, LLMs such as OpenAI's GPT models can produce fluent and coherent text on demand. However, these models also pose significant challenges and risks for AI developers and users.

Some of these challenges and risks include:

- **Societal bias and harm**: LLMs may inherit and amplify societal biases and harms that exist in their training data, such as stereotypes, prejudices, and hate speech. This can lead to harmful or offensive outputs that may affect the reputation, trust, and safety of an AI solution.

- **Misinformation and manipulation**: LLMs may generate false or misleading information that can deceive or influence users. This can have serious consequences for the credibility and accountability of an AI solution.

- **Legal and regulatory compliance**: LLMs may raise legal and regulatory issues, such as data privacy, intellectual property, and human rights. This can expose the AI solution to potential liabilities and penalties.

To address these challenges and risks, AI developers and users should implement the following initiative:

[The responsible AI principles and practices for LLMs](https://github.com/Azure/FTALive-Sessions/blob/main/content/ai/responsible-ai/en/responsible-ai-for-llms.md) provides a set of guidelines that aim to ensure that teams can build and use LLMs in a responsible and risk-aware manner.

By applying the principles and practices for AI solutions built with LLMs, AI developers can identify and assess the potential harms and benefits of LLMs, and mitigate or prevent the negative impacts.

### Red teaming and adversarial testing for AI solutions

Red teaming is a practice of systematically testing and probing AI systems for potential vulnerabilities and harms. It is especially important for identifying responsible AI risks when using large language models, which can produce harmful outputs such as hate speech, incitement of violence, or sexual content. By conducting red teaming exercises, you can uncover and identify RAI risks, measure the effectiveness of mitigations, and provide feedback for improvement.

Microsoft's [guide to planning red teaming for LLMs](https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/red-teaming) provide a step-by-step process for preparing, executing, and reporting your findings from red teaming exercises.

Here's an overview of the best practices for red teaming LLMs and their applications:

- **Start early and iterate**: Begin by testing the model to understand the risk surface and guide the development of responsible AI mitigations. Test versions of your AI solution iteratively with and without mitigations to assess their impact.

- **Have a diverse and multi-disciplinary team**: Include team members with different backgrounds, expertise, and perspectives to cover a wide range of scenarios and harms. For example, if you are building a call centre chatbot, you might want to have a mix of people with experience in natural language processing, responsible AI, and customer service.

- **Use a list of harms as a guideline**: Create a list of harms, with definitions and examples, that are relevant to your solution's domain and context. Use this list to inform your testing and prioritization. Be open to discovering new harms and updating your list accordingly.

- **Plan your process and data collection**: Decide on the composition, focus, and time allocation of your team. Choose a simple and shared method for collecting and reporting data. Include essential information such as the input, output, and unique ID of each example.

- **Share your results and feedback**: Communicate your findings and recommendations to key stakeholders on a regular basis. Clarify that red teaming is not a replacement for systematic measurement and rigorous mitigation work, but a way to expose and raise awareness of responsible AI risks.

### Implementing Azure OpenAI content filters to mitigate harmful content

As you build and deploy AI solutions using Azure OpenAI, you may encounter scenarios where user inputs and model responses contain harmful or inappropriate content. Such content can pose legal and reputational risks to your business, as well as harm to your users. It is essential to implement responsible AI measures to prevent or reduce the exposure to harmful content in your AI solutions.

One of the key responsible AI practices for AI solution is to [use Azure OpenAI content filters](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/content-filters), which are integrated directly into the service. Content filters use a collection of multi-class classification models to detect and filter harmful content in four categories at three severity levels. The categories include violence, hate, sexual, and self-harm, with the ability to set severity levels from low to high for each.

{: .important }

> For special use cases, approved Microsoft Partners can apply to partially or fully disable content filters in your Azure OpenAI service. These scenarios are subject to review and approval by Microsoft and require you to comply with Microsoft's Code of Conduct for Azure OpenAI.

The content filters feature in Azure OpenAI allows you to configure dedicated content filters in your Azure OpenAI service to filter content based on your use case needs. These filters can then be applied to any model deployments to the Azure OpenAI service. Once configured, the content filters will automatically detect and filter content in your AI solutions calling the Azure OpenAI endpoints.

When implementing content filters in your AI solutions, it is important to measure the effectiveness of the filters to ensure that they are working as intended. Deployed content filters can later be evaluated and iterated on to improve their performance.

## Using standard frameworks to identify threats to AI solutions

To identify and mitigate against risks in AI solutions, teams need to adopt a systematic and comprehensive approach to assessment. Frameworks such as the [ATLAS Matrix](https://atlas.mitre.org/matrices/ATLAS/) map out tactics and techniques that can compromise AI solutions across the entire lifecycle of the system, from development to operation, based on the MITRE ATT&CK framework for cybersecurity.

OWASP, the Open Web Application Security Project, has also developed a guide to the [top 10 most critical vulnerabilities in LLM applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/) that highlights their potential impact, ease of exploitation, and prevalence in real-world AI solutions. These vulnerabilities include:

- **Sensitive Information Disclosure**: This occurs when an LLM inadvertently reveals confidential data in its responses, leading to unauthorized data access, privacy violations, and security breaches. It is crucial to implement data sanitization and strict user policies to mitigate this.

- **Insecure Plugin Design**: This occurs when LLM plugins have insecure inputs and insufficient access control. This lack of application control makes them easier to exploit and can result in consequences like remote code execution.

- **Over-reliance**: This occurs when systems overly depend on LLMs without oversight and may face misinformation, miscommunication, legal issues, and security vulnerabilities due to incorrect or inappropriate content generated by them.

To identify and mitigate against threats to AI solutions, it is essential to implement a comprehensive and robust risk management assessment using standard frameworks such as the ATLAS Matrix and OWASP's vulnerabilities, following their best practices and guidelines. Applying these techniques early, and throughout, the development lifecycle will help you to design and implement appropriate controls to protect your AI solutions against potential threats.

## Conclusion

As we continue to build new innovative solutions with AI, it is essential to identify and assess the potential risks and challenges that they may have. Using the tools and resources outlined in this chapter, teams can establish their own process for risk management from the design of machine learning models to the deployment of LLMs in production. It is imperative to adopt responsible and transparent practices, prioritizing the security and privacy of your end users to ensure that your AI solutions are trustworthy and reliable.
