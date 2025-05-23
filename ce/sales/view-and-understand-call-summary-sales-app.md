---
title: View and understand the call summary page
description: Use the call summary to get a high-level view of how a conversation with a customer went, action items, keywords, the call timeline, and a transcript in the Dynamics 365 Sales Hub app.
ms.date: 11/05/2024
ms.topic: how-to
ms.custom: bap-template
ms.service: dynamics-365-sales
author: lavanyakr01
ms.author: lavanyakr
ms.reviewer: lavanyakr
---

# View and understand the call summary page

Sellers and their managers need an easy way to review their conversations with customers and quickly find talking points and insights. The call summary page provides that high-level view of how a conversation with a customer went. It includes action items and relevant keywords, a timeline, and a transcript of the call to help both sellers and managers.

- Sellers can quickly review past conversations with a customer and highlight important topics and commitments.
- Managers can get a high-level view of how their sales team is managing their relationships with customers.

## Prerequisites

[Configure conversation intelligence to process call recordings](intro-admin-guide-sales-insights.md#administer-conversation-intelligence).

## View the call summary page

The call summary for a phone call activity is available after the call ends and the call recording is processed by conversation intelligence.  

1. In the Sales Hub app, select **Change area** > **Sales**, and then select **Activities**.

1. Select a phone call activity for which you want to view the call summary.

1. Select the **Call summary** tab.

    :::image type="content" source="media/si-app-activities-call-insights-tab.png" alt-text="Screenshot of the Call Summary tab in a phone call activity.":::

If one or more opportunities are associated with the call, select the **Related opportunity** tab to view them. To add a related opportunity to the call, search for and select the opportunity.

## Understand the call summary page

The call summary page includes the following sections:

- [Overview, notes, action items, mentions, and highlights](#overview-notes-action-items-mentions-and-highlights)
- [Call transcript and translation](#call-transcript-and-translation)  
- [Call playback timeline and segmentation](#call-playback-timeline-and-segmentation)

### Overview, notes, action items, mentions, and highlights

This section is where you'll find key insights generated from conversation intelligence.

#### Overview tab

The **Overview** tab displays the following information about the conversation:

- The date, time, and length of the call
- Tags that were added to the conversation to improve searchability
- The names of the people who participated in the call
- KPIs for each person

  - For the seller: Talk to listen ratio, average talking speed, number of switches per conversation, and average pause length
  - For the customer: Length of the longest monologue

:::image type="content" source="media/ci-summary-call-overview.png" alt-text="Screenshot of the Overview tab of the call summary page.":::

##### View categorization tag for short duration calls (Preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner-section.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

Conversation intelligence can detect and tag short duration calls for the following categories:

- Voicemail
- Contact is unavailable
- Short calls with reschedule requests
- Short calls in which the contact indicates the call is unwanted

If the tag is inappropriate, you can delete it.  

Your administrator must [enable the **Call categorization (preview)**](fre-setup-ci-sales-app.md#enable-call-categorization-for-short-calls-preview) feature for the system to tag short duration calls. You can also view these tags in the [Conversation intelligence app](https://sales.ai.dynamics.com/) under **Seller Details** > **Call History** section. For more information, see [View a seller’s performance to identify best practices and coaching opportunities](conversation-intelligence-seller-details.md).  

#### Notes tab

> [!NOTE]
> Starting June 2024, the **Action items** tab is removed and the **Notes** tab is enhanced to include action items. However, unlike the **Action items** tab, the **Notes** tab doesn't have the option to create tasks, calls, or emails directly from the action items. 

The **Notes** tab helps reduce the time it takes you to summarize the call by offering intelligent suggestions, including action items, commitments, call minutes, and next steps. Writing a personalized summary of the call helps you to focus on the customer's need, quickly review key points, and understand the next course of action. You can share the summary with stakeholders through email.

:::image type="content" source="media/ci-summary-call-summary-sales-app.png" alt-text="Screenshot of the Notes tab of the call summary page.":::

##### Write a call summary

1. On the **Notes** tab, edit any notes you took during the call, and check the **Suggested notes** pane for call highlights and action items. If you don't see the **Suggested notes** pane, select the bulb icon to open the pane.

    - Select **Add** to add a call highlight or action item to your summary.
    - To add all the call highlights or action items, select **More options** (**&hellip;**), and then select **Add all**.
    - To understand the context of a call highlight or action item, select the timestamp to go to that point in the call transcript and playback.

    :::image type="content" source="media/ci-summary-call-summary-suggested-notes-sales-app.png" alt-text="Screenshot of Suggested notes in the Notes tab.":::

1. Select **Save**.

##### Share a call summary

1. In the notes section of the **Notes** tab, select **Copy to clipboard**.

    This option doesn't appear if you haven't saved your notes.

    :::image type="content" source="media/ci-summary-call-summary-copy-summary-notes-sales-app.png" alt-text="Screenshot of the call summary Notes tab, with Copy to clipboard highlighted.":::

1. Paste the notes in the body of an email.


#### Mentions tab

The **Mentions** tab displays talking points&mdash;keywords, stakeholders, products, questions, and competitors&mdash;that were mentioned during the call. When you select any of these items, the call transcript is highlighted and a pointer on the playback indicates when it was mentioned.

:::image type="content" source="media/ci-summary-keywords.png" alt-text="Screenshot of the Mentions tab of the call summary page.":::

- **Tracked keywords**: Predefined keywords that customers mentioned during the call
- **People**: The names of people mentioned during the call
- **Products**: The names of the products mentioned during the call
- **Competitors**: Predefined competitors that customers mentioned during the call
- **Best-practice keywords**: Keywords that can be used as best practices during the call
- **Other brands and organizations**: Brand and organization names, other than your own, that the customer mentioned during the call
- **Questions asked by sellers**: Questions that the Dynamics 365 user&mdash;the seller&mdash;asked during the call
- **Questions asked by others**: Questions asked by the other participants during the call

### Call transcript and translation

The **Transcript** tab displays a timeline and written record of the call, which you can read, comment on, and translate. Icons indicate where comments have been added to the timeline. Brands, tracked keywords, and competitors mentioned in the conversation are formatted in bold in the transcript.

:::image type="content" source="media/ci-transcript-conversation-transcript.png" alt-text="Screenshot of the Transcript tab of the call summary page.":::

If the transcript is in a language other than English and the language is one that Microsoft supports, select the translate icon ![Translate icon](media/ci-transcript-translate-icon.png "Translate icon") to convert the transcript to English.

Credit card details that were shared during the call are visible in the transcript unless your administrator has turned on the [**Hide personal data (preview)** setting](fre-setup-ci-sales-app.md#hide-personal-data-preview) to comply with Payment Card Industry regulations. If that setting is turned on, the account number, expiration date, and CVV are masked in the transcript.

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner-section.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

#### Comment on the transcript

As a manager, you can review the transcript and leave a comment&mdash;for example, suggesting how the seller might handle a similar situation in the future. As a seller, you can review the transcript and comments from your manager or coach, reply to their comments, and add your own.

1. Hover over the part of the transcript you want to comment on and select **Add comment**.

1. Enter a comment or reply to a comment.

1. Select **Save**.

    :::image type="content" source="media/ci-transcript-comment.png" alt-text="Screenshot of adding a comment to a transcript.":::

### Call playback timeline and segmentation

Use the call playback feature to listen to the recorded call. To skip to a specific point, drag the progress bar or select a location in the playback. The call transcript automatically scrolls to that moment in the call. You can also pause, rewind, and move forward through the call and adjust the volume. The playback timeline also displays the sentiments detected in the conversation, positive, neutral, or negative.

:::image type="content" source="media/ci-summary-playback-sales-app.png" alt-text="Screenshot of the playback timeline on the call summary page.":::

When you go to the **Highlights** tab and hover over or select a keyword or other highlight, a diamond icon appears on the playback timeline to indicate the time that it was mentioned.

You can quickly go to comments from the timeline. Select the comment icon (:::image type="icon" source="media/comment-icon.png" border="false":::) on the timeline to go to the corresponding comment in the transcript.

The timeline shows how the conversation was segmented and the topics that were discussed in a segment. You can choose a specific segment to drill down into relevant insights. The transcript adjusts to display the start of the segment and highlights the segment in the playback timeline. If the selected segment contains any action items or keywords, they're displayed on their respective tabs.

[!INCLUDE [cant-find-option](../includes/cant-find-option.md)]

## Related information

[Overview of Conversation Intelligence](../sales/dynamics365-sales-insights-app.md)  
[Track and manage activities](manage-activities.md)  
[View call recordings and transcripts in Dynamics 365 Customer Service](../customer-service/use/voice-channel-call-recordings-transcripts.md)  
[View and share auto-summarized conversations in Dynamics 365 Customer Service](../customer-service/cs-ai-generated-summary.md)  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
