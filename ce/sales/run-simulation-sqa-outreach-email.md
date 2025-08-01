---
title: Run simulation to review outreach email content (preview)
description: Learn how to run a simulation to review the drafts of outreach emails generated by the Sales Qualification Agent in Dynamics 365 Sales.
ms.topic: how-to 
ms.date: 08/01/2025
ms.service: dynamics-365-sales
content_well_notification:
  - AI-contribution
ms.custom: bap-template
author: udaykirang
ms.author: udag
ms.reviewer: udag
search.app: salescopilot-docs
ms.collection: bap-ai-copilot
ai-usage: ai-assisted
---


# Run simulation to review outreach email content (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

This feature is available only for **Research and engage** (fully autonomous) mode.  
You can run a simulation to review the drafts of outreach emails generated by the Sales Qualification Agent. This helps you ensure that the emails are customized and relevant to the leads before they are sent out.  

>[!IMPORTANT]
>Simulation consumes tokens from your Copilot capacity. Ensure you have enough tokens available in your Copilot capacity to run the simulation. Learn more in [Manage Copilot Studio messages and capacity](/power-platform/admin/manage-copilot-studio-messages-capacity?tabs=new).

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

After you complete the configuration of the Sales Qualification Agent, do the following:

1. Go to the **Simulation** section and then select **Outreach emails**.  

    > [!NOTE]
    > The **Outreach emails** option is enabled only if you have leads that match the configured selection criteria.  

1. In the **Review outreach emails** page, select **Start testing**. The agent performs the following actions:  
    1. Research the assigned leads.  
    1. Draft outreach emails based on the research.  

    > [!NOTE]
    > The **Start testing** option is enabled only if you complete and save the configurations.

1. After the research is complete, the drafts are available for review, select **Review**.  
1. Review the drafts and provide feedback or make edits as necessary.  

## Next steps

[Start the Sales Qualification Agent](start-sales-qualification-agent.md)

## Related information

[Configure the Sales Qualification Agent](configure-sales-qualification-agent.md)
