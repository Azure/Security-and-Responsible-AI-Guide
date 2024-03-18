---
nav_order: 6
has_children: false
title: Chapter 5 - Monitoring and Auditing AI Solutions
permalink: /chapters/chapter_05_monitoring_and_auditing_ai_solutions
layout: default
---

# Chapter 5: Monitoring and Auditing AI Solutions

{% include table_of_contents.md %}

Monitoring and auditing AI solutions is crucial to ensure that they are functioning as intended, preventing potential security breaches, and not causing harm to end users. By establishing a process for observing your solution, you can ensure the efficient operation of your AI system for your customers.

This chapter explores the tools and techniques that you can employ to help continuously monitor your Azure AI solutions to ensure that they are functioning as intended.

![Monitoring and Auditing AI Solutions](../media/chapter_05.jpg)

## Establishing effective monitoring and alerting in AI solutions

Ensuring that your AI solutions are functioning as intended in a secure and responsible manner is crucial to building trust with your customers. However, monitoring and auditing them can be challenging due to the complexities of AI solutions, including:

- **Lack of transparency**: AI solutions are often considered black boxes, making it difficult to understand how they work and what they are doing.

- **Adversarial attacks**: AI solutions can be vulnerable to adversarial attacks, where an attacker tries to manipulate the system by feeding it malicious data without being detected.

- **Model drift**: AI solutions naturally drift from their original input parameters and over time produce unwanted results once deployed.

To address these challenges and more, teams should consider implementing tools and techniques that allow them to improve the observability of their AI solutions. Doing so will maximize the ability to detect and mitigate against potential threats, vulnerabilities, and comply with their regulatory requirements. The following resources provide guidance on how to establish effective monitoring and alerting in your AI solutions.

### Using Microsoft Sentinel to detect security vulnerabilities in Azure AI Services

If you are developing or using Azure AI services, such as Azure OpenAI, you need to ensure that your applications and data are secure and compliant. Azure AI services provide powerful capabilities for building intelligent solutions, but they also expose potential attack vectors and vulnerabilities that need to be monitored and mitigated.

[Building Microsoft Sentinel Detections for Azure OpenAI](https://rodtrent.substack.com/p/building-microsoft-sentinel-detection) explores how you can use Microsoft Sentinel to collect and analyze data from Azure AI services, such as audit, request and response logs to get a detailed view of your security posture.

This approach allows you to detect and investigate potential threats and vulnerabilities in your solutions integrating Azure AI services and correlate with other data sources to enrich and contextualize your security alerts. You can use Microsoft Sentinel to automate your response to security incidents and take appropriate action to mitigate against them.

### Monitoring Azure Machine Learning model performance in production

When building your custom Machine Learning models for your AI solutions, you might have developed and deployed models to solve challenges for your customers. However, deploying a model is not the end of the story. You also need to monitor its performance in production and make sure it is delivering the expected value and quality.

[Model monitoring with Azure Machine Learning](https://learn.microsoft.com/en-us/azure/machine-learning/concept-model-monitoring?view=azureml-api-2) provides a comprehensive solution for monitoring a model to help you track and improve its performance over time. Here are some of the benefits and features of using Azure Machine Learning for model monitoring:

- **Ease of setup**: You can easily set up model monitoring with a few lines of code or clicks in the studio UI. Azure Machine Learning supports both online and batch endpoints, as well as models deployed outside of Azure Machine Learning.

- **Built-in monitoring signals**: You can choose from a range of built-in monitoring signals, such as model drift, data quality, and feature attribution drift. These signals can help you detect and diagnose issues with your model or data, such as data distribution changes, training-serving skew, or feature importance shifts.

- **Alerting out-of-the-box**: You can customize your monitoring metrics and thresholds for each signal, and receive alerts via Azure Monitor when any anomaly is detected. You can also define your own monitoring signals with custom components if the built-in ones are not suitable for your scenario.

- **Detailed dashboards**: You can view and analyze your monitoring results inside the Azure Machine Learning studio, where you can access detailed reports, charts, and dashboards. You can also use the SDK or CLI to programmatically access your monitoring data and integrate it with other tools or workflows.

By using Azure Machine Learning for model monitoring, you can ensure that your models are always up to date and reliable, and that you can quickly identify and resolve any issues that might affect your business outcomes. Model monitoring is an essential part of the machine learning lifecycle, and Azure Machine Learning makes it easy and convenient for you to implement it.

### Monitoring Azure AI service solutions with confidence

Azure AI services, such as Azure OpenAI, enable you to integrate cutting-edge artificial intelligence capabilities into your applications and services. However, to ensure the optimal performance, availability, and operation of your AI solutions, you need to monitor them effectively and efficiently.

[Azure OpenAI Insights: Monitoring AI with Confidence](https://techcommunity.microsoft.com/t5/fasttrack-for-azure/azure-openai-insights-monitoring-ai-with-confidence/ba-p/4026850) provides a step-by-step guide to help you track the usage, costs, and health of your AI resources, allowing you to troubleshoot issues and optimize your AI solutions. Here are some of the benefits and features of taking advantage of this guidance to monitor Azure OpenAI using Azure Monitor:

- **Analyzing platform metrics**: This approach allows you to view and analyze metrics from your Azure OpenAI resources including HTTP requests, token usage, PTU utilization, and fine-tuning dimensions. The provided workbook allows you to visualize these metrics and gain insights into the health of your AI resources.

- **Triggering alerts on key metrics**: Azure Monitor allows you to create notifications based on various monitoring data that you can use to define alert rules for. This allows you to be notified when certain conditions are met, such as when your Azure OpenAI resource is running to capacity.

By using these Azure Monitor tooling with your Azure AI services, you can gain deep insights into Azure OpenAI service usage, performance, and operation, and take appropriate actions to manage and optimize your AI solutions.

## Conclusion

In the realm of AI solutions, monitoring and auditing play a pivotal role in ensuring functionality, security, and user safety. The complexities associated with AI, such as lack of transparency, susceptibility to adversarial attacks, and model drift, provide a spotlight on the need for observability of AI solutions. Establishing effective monitoring and alerting processes is crucial for building trust with customers.

These guidance in this chapter collectively empower engineering teams to enhance the observability of their AI solutions, detect potential threats, comply with regulatory requirements, and optimize performance for a secure and reliable user experience.
