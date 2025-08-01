---
title: Configure selection criteria for Sales Qualification Agent (preview)
description: Learn how to configure the selection criteria for the Sales Qualification Agent in Dynamics 365 Sales.
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

# Configure selection criteria for Sales Qualification Agent (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

The selection criteria helps you to group the incoming leads into a segment and assign them to the agent based on the defined conditions. For example, the leads that are unprocessed, unattended, and potentially lower value could be mapped under this segment and worked on by the agent. The segment groups these leads, and helps agent to drive net-positive outcome, ensuring every opportunity is assessed without adding manual workload for sellers.  

Read the [create and activate a segment](wa-create-and-activate-a-segment.md#create-and-activate-a-segment) article for more information.

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

> [!NOTE]
> The priority of the segment created for the agent is always low and one above the default segment. So, ensure that the segment you're creating for the agent doesn't overlap with the segments used for work assignment to sellers. If there's an overlap, leads will be assigned to sellers instead of the agent.

**Follow these steps**:

1. [Go to the agent settings page](open-sales-qualification-agent-settings.md).  
1. In the **Guidance** section, select **Selection criteria**.  

    :::image type="content" source="media/sqa-settings-selection-criteria.png" alt-text="Screenshot of the Sales Qualification Agent settings page with selection criteria highlighted.":::

1. Enter a name and description for the selection criteria.
1. In the **Segment conditions** section, you can edit or remove the default conditions, or add conditions that are used to evaluate leads for assignment to the segment.  
    By default, the following conditions are defined for the agent.  

    | Field name | Operator | Value | Description |
    |------------|----------|-------|-------------|
    | Status | Equals | Open | The lead’s status should be open. |
    | Rating | Equals | Cold | The lead’s rating should be cold, which requires nurturing and consistent follow-up. |
    | Lead Source | Does not equal | Employee Referral and Partner | Exclude the leads that are sourced from employee referrals and partners. |
    | Email | Contains data | &mdash;| Emails from the leads should contain data such as information related to sales, customer, or feedback. |

    > [!NOTE]
    > You can have up to 10 conditions at any given time including conditions that are based on groups and related entities.

1. To add more conditions, select **Add** and then use the following options to build the conditions of the segment:
    - **Add row**: Add condition. Select an attribute, an operator, and a value; for example, *Created by Equals John Thomas*.  
        Add more conditions as needed, for a total of 10, to further filter the records that should be assigned to the segment.
    - **Add group**: Add a group of conditions to filter records using multiple attributes that are combined by **And** or **Or**. If you select **And**, leads must meet all the conditions in the group. If you select **Or**, leads can meet any condition in the group.
    - **Add related entity**: Add a condition that's based on the attributes of related tables. Select an attribute in the **Related Entity** list, then select **Contains data** or **Does not contain data**, and then define the condition.  
1. By default, the agent only considers new leads created after the agent is turned on. If you want the agent to also research on leads created before it was enabled, select the **Consider opportunities created in the last** checkbox and specify the number of days for the look back period.  
1. (Optional) When you've finished defining the conditions, select **Preview leads** to view a list of records that satisfy the conditions.  
    If you are satisfied with the results, you can continue with the next configuration step.

## Next step

[Configure email instructions and address validation](sales-qualification-agent-email-instruction-validation.md)

## Related information

[Configure the Sales Qualification Agent](configure-sales-qualification-agent.md)
