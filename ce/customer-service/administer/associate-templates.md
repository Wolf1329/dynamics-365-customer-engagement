---
title: Associate templates with workstreams
description: Learn how to associate the different templates with workstreams that can be used for incoming conversations.
author: neeranelli
ms.author: nenellim
ms.reviewer: nenellim
ms.date: 04/28/2025
ms.topic: how-to
---

# Associate templates with workstreams

[!INCLUDE[cc-feature-availability-embedded-yes](../../includes/cc-feature-availability-embedded-yes.md)]

The session, notification, and application tab templates that you create need to be associated with a workstream, so that the omnichannel system uses the corresponding templates for an incoming conversation.

After a customer service representative (service representative or representative) accepts the conversation request, a session starts for which the session template is used. In the session, certain application tabs are required such as dashboard, knowledge article search, and case pages. These application tabs are configured using the application tab templates and are associated with a session.

## Associate or modify templates with workstreams 

After you create a workstream, you can modify the default templates that are attached to the workstream.

1. In the site map of Copilot Service admin center, select **Workstreams** under **Support experience**.
1. Select the workstream for which you want to modify the template, and expand the **Show advanced settings** section.
1. Select **Edit** beside **Sessions**, and on the **Sessions** panel that appears, select a template in the **Default template** list.
1. Select **Save and close**.
1. Select **Edit** for **Customer service representative notifications**, and on the **Customer service representative notifications** panel that appears, select a template for each of the following types of notifications:
    - Incoming unauthenticated
    - Incoming authenticated
    - Consult
    - Transfer
    - Supervisor assign
    - Returning Conversation (available for persistent chat workstreams only)

1. Select **Save and close**.

### Related information

[Manage session templates](session-templates.md)  
[Manage application tab templates](application-tab-templates.md)  
[Manage notification templates](notification-templates.md)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
