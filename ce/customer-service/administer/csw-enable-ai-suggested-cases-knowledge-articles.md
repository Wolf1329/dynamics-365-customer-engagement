---
title: Enable AI suggestions for cases and knowledge articles
description: Enable AI suggestions for cases and knowledge articles in Dynamics 365 Customer Service.
ms.date: 06/30/2025
ms.update-cycle: 180-days
ms.topic: how-to
author: lalexms
ms.author: laalexan
ms.reviewer: laalexan
ms.collection: bap-ai-copilot
search.audienceType:
  - admin
ms.custom: 
  - dyn365-customerservice
  - bap-template
feedback_product_url: https //experience.dynamics.com/ideas/categories/list/?category=a7f4a807-de3b-eb11-a813-000d3a579c38&forum=b68e50a6-88d9-e811-a96b-000d3a1be7ad
---

# Enable AI suggestions for similar cases and knowledge articles

[!INCLUDE[cc-feature-availability-embedded-yes](../../includes/cc-feature-availability.md)]

> [!NOTE]
> Case information is applicable to Customer Service only.

With the use of AI, customer service representatives in your organization can review similar cases that were previously resolved successfully. This feature can help them find the right solutions quickly, increase their productivity, and provide better and faster service to customers.

The key highlights of the feature are as follows:

- AI-driven case and knowledge article suggestions that are based on case context and historical success rate.
- Secondary actions that representatives can take, such as collaborating with an expert, when a similar case is found.
- Capability of the AI model to process up to 1 million of the most recent cases for listing them at runtime.

> [!NOTE]
> - The AI suggestions feature is currently available in a few geographical locations only. Learn more in [Regional availability and Service limits for Customer Service](cs-region-availability-service-limits.md).
> - When you enable AI suggestions, if representatives don't interact with the AI-suggested content for 21 days, the feature is deactivated. The administrator can enable it again.

## Prerequisites

Make sure that the following requirements are met:

- Copilot Service workspace is installed and accessible. Learn more in [Copilot Service workspace](../implement/csw-overview.md).
- The	productivity pane is enabled. Learn more in [Productivity pane](productivity-pane.md).
- The System Administrator role is granted.
- The workflow processes used by the AI model and AI configuration entities are in the activated status. Learn more in [Workflow processes](#workflow-processes).
- If administration mode is enabled, make sure that background operations are also enabled. Learn more in [Administration Mode](/power-platform/admin/admin-mode).
- For the AI suggestions to work, customer-managed keys should be disabled.

## How AI suggestions for similar cases and knowledge articles work

The AI suggestions are displayed in smart assist, an intelligent assistant that provides real-time recommendations to representatives to help them take action during their interactions with customers. When you enable the productivity pane in Copilot Service workspace, the smart assist cards with suggestions appear on the productivity pane.

The AI suggestions use a set of pretrained natural language understanding models. These models are designed to help representatives find relevant knowledge articles or similar cases quickly, based on the context of active cases or ongoing conversations. 

The AI models work as follows:

- AI suggests knowledge articles and similar cases based on the semantic meaning in case context and knowledge article content.
- When you enable the settings, it might take up to 24 hours for the models to process data and complete the first time setup. 
- The model preprocesses published knowledge articles and resolved cases every day to prepare suggestion candidates. For the first time preprocessing, up to 1,500 published articles and 15,000 recently resolved cases are processed. Then, newly published articles and resolved cases are processed up to the daily limit. Over time, accumulatively, up to 1 million of the latest resolved cases are processed to serve suggestions.
- When a case is created or updated, or during an ongoing conversation, the model finds out matching knowledge articles and similar cases from suggestion candidates.
- A brief summary is autogenerated for each preprocessed knowledge article, based on its content. When the system suggests a knowledge article, both the article title and autogenerated summary are surfaced to representatives. This data can help representatives get a better idea about an article before they select through it.
- In addition to the suggestions, representatives can also tell why the system suggests an article or similar case is through a list of key phrases that the system autoextracts from knowledge articles and cases. These key phrases highlight the relevance between a suggestion and an active case or an ongoing conversation in addition to the confidence score (a percentage number that indicates the degree to which an article or similar case matches with the active case).
- During an ongoing conversation, for the first three messages sent by the customer, the AI suggestions are triggered for each message. Following these first three customer messages, AI suggestions are triggered for every third customer message. The AI suggestions are based on the context described in the last 18 messages.
- When you enable the settings, the suggestions will be in place only when representatives refresh or reopen their browser. They won't appear in the currently active sessions or on a session switch.

## Language support for AI suggestions

Learn about supported languages in [Language support for AI-based analytics and insights in Customer Service](cs-region-availability-service-limits.md#language-support-for-ai-based-analytics-and-insights-in-customer-service)

When a representative opens a case or accepts a conversation, smart assist checks the language from the following sources:

- Whether the language selected in the language settings is supported.

- Whether the language that AI detects in the case or conversation that the representative accepts matches the language settings.

If the language verification passes, the suggestions are displayed in the language used in the case or the conversation. Suggestions aren't displayed if the language doesn't match or isn't supported. In such cases, the representative should update the settings to use supported languages. The language settings used in AI suggestions are listed as follows:

- For similar case suggestions, the language selected in the user's **User Interface Language** settings is used to display similar cases and knowledge article suggestions.

- For knowledge article suggestions, smart assist first checks for the language set in the **Knowledge Personalization** settings. If no language setting is found, the user's **User Interface Language** setting is used to display knowledge article suggestions. Learn more in [Personalize your knowledge search article filters](../use/filter-articles.md#personalize-your-knowledge-search-article-filters).

## Enable AI suggestions for similar cases

You can enable AI suggestions for similar cases in the Copilot Service admin center app.

1. In the site map of Copilot Service admin center, select **Insights** in **Operations**. The **Insights** page appears.
1. In the **Suggestions for agents** section, select **Manage**.

1. In the **Settings** > **Summary** area, set the **Enable similar case suggestions** toggle to **Yes**.

1. In the **Data mapping** > **Case entity data fields** area, select values for the **Case summary** and **Case details** boxes respectively, if you don't want to use **Case Title** and **Description** that are set by default. You can choose up to three more fields for the case suggestion model to use to find similar cases. For example, you can look at cases with a similar age, cases owned by a particular team, and so forth. The AI model uses the data that corresponds to the selected boxes to understand the case context to provide similar case suggestions.

   > [!NOTE]
   > We recommend that you use text fields with plain text because suggestions might not be generated for text fields that are enabled for rich text format.

   > ![Enable AI-suggested similar cases.](../media/csac-enable-ai-suggested-cases.png "Enable AI-suggested similar cases")

1. Select **Save**.

## Enable AI suggestions for knowledge articles

You can enable AI suggestions for knowledge articles in the Copilot Service admin center app.

1. In the site map, select **Insights** in **Operations**. The **Insights** page appears.

1. In the **Suggestions for knowledge article authors** section, select **Manage**.
    
2. In the **Summary** area, set the **Enable keywords and description suggestions** toggle to **Yes**.

3. In the **Data mapping** > **Knowledge article data fields** area, ensure that **KB articles** is selected for **Article entity**, and **Title** and **Content** are selected in the **Article title** and **Article content** boxes, respectively. You can choose three more fields for the model to find similar knowledge articles, such as article keywords, description, and so forth. The selected options are used by the AI model to understand and find a good match for a case or conversation. The AI model uses the article content is to generate a brief article summary that displays to the representative at runtime.

4. Select **Save**.

## Model preprocessing rules

You can use model preprocessing rules to limit the preprocessed cases that the AI model suggests to your representatives. You can choose from various conditions, such as, sentiment value and associated with the resolved case.

You can also apply model preprocessing rules to knowledge articles to limit the suggestions to knowledge articles based on things such as keywords, language, the number of views on the knowledge article, and so forth.

## Model preprocessing status

The **Model preprocessing status** area displays the following metadata pertaining to the AI processing. The run frequency is set out of the box. Every day, the model preprocesses newly published or updated knowledge articles and resolved or updated cases to prepare the candidates for suggestions.

- **Last successful run**: Displays the date and time the model was last run.
- **Case records**: Displays the number of new or updated resolved case records that were processed.
- **Knowledge articles**: Displays the number of new or updated published knowledge articles that were processed.
- **Run frequency**: Displays the frequency that is set for the model to run.

### Workflow processes

The AI model and AI configuration entities use the following workflow processes. Make sure these processes are in the activated status. By default, these processes are activated:

- IsPaiEnabled
- Predict
- PredictionSchema
- Train
- QuickTest
- BatchPrediction
- ScheduleTraining
- SchedulePrediction
- ScheduleRetrain
- UnschedulePrediction
- UnscheduleTraining
- CancelTraining
- PublishAIConfiguration
- UnpublishAIConfiguration

## Service protection limits for AI suggestions

AI suggestions for Case and Knowledge became available as of October 2020. We're introducing service protection limits on these capabilities to maintain a consistent quality of service for all our customers, but there's no penalty if customers exceed predefined limits. Over time, Microsoft might adjust these limits in keeping with customer usage patterns and provide options for customers with high usage scenarios and patterns to purchase more capacity in a manner disruptive to those customers.

The service protection limits for AI suggestions are defined in the following table. The total limits are pooled at the tenant level based on the number of Customer Service Enterprise user licenses that are available in the tenant.

| Area    | Limits     | Notes     |
|----------|------------|-----------|
| AI suggestions for active cases | 30 cases/month per user license | Each user license adds 30 active cases, where representatives can get AI-suggested knowledge articles and similar cases in real time. |
| AI suggestions for conversations | 150 conversations/month per user license | Each user license adds 150 omnichannel conversations, where representatives can get AI-suggested knowledge articles and similar cases in real time.|
||||

### Related information

[View AI-suggested similar cases and knowledge articles for active cases](../use/csw-view-ai-suggested-cases-knowledge-articles.md)  
[View smart assist suggestions for knowledge articles and similar cases using AI for ongoing conversations](../use/oc-view-ai-suggested-cases-articles.md)  
[FAQ on AI-suggested cases and knowledge articles](csw-faqs-ai-suggestions.md)  
[Create a new similarity rule to view similar cases](suggest-similar-cases-for-a-case.md#create-a-new-similarity-rule-to-view-similar-cases)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
