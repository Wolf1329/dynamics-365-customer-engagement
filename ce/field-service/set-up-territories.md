---
title: Service territories for accounts, work orders, and resources.
description: Learn how to use territories for accounts, work orders, and scheduling in Dynamics 365 Field Service.
ms.date: 06/23/2025
ms.topic: how-to
author: ryanchen8
ms.author: chenryan
---
# Territories for accounts, work orders, and resources

Territories help you divide your business into geographical regions for work order management, scheduling, and reporting. You can group customers, work orders, and resources based on a custom region.

Use territories with work orders and resources to help dispatchers schedule work orders to resources with a matching territory. Territories are useful filters on the schedule board, the schedule assistant, and the [Resource Scheduling Optimization add-in](rso-overview.md).

## Create a territory

Create your territories in Field Service settings or import them from Excel.

1. In **Field Service**, open the **Settings** area.

1. Under **General**, select **Territories**, and then select **New**.

1. Enter a **Territory Name**.

1. Enter the following information (optional).

   - **Manager**: The specific user who manages the territory.

   - **Parent**: The parent territory if this territory is in a hierarchy.
  
1. Select **Save & Close**.  
  
## Assign resources to territories

Bookable resources like field technicians, equipment, or facilities can belong to one or more territories.
  
1. Open the **Resources** area. Under **Resource**, select **Resources**.

1. Select the resource you want to assign to a territory.
  
1. On the Bookable Resource form, select **Related** > **Resource Territories**.

1. Select **New Resource Territory**.

1. Choose the **Territory** or create a new one.  

1. Select **Save & Close**.

:::image type="content" source="media/territory-resource.png" alt-text="Screenshot of the Bookable Resource record with an associated Territory record.":::

## Add accounts to territories

Customer accounts can belong to a single service territory.

1. Open the **Service** area. Under **Customers**, select **Accounts**.

1. Select the account you want to assign to a territory.
  
1. On the Account form, select **Related** > **Servicing**.

1. In the Service section, choose a Service Territory or create a new one.

1. Select **Save & Close**.

## Territories in the scheduling assistant

While scheduling, you can match the required service territory to the resources in those territories.

If you attempt to [book a work order with the schedule assistant](schedule-assistant.md), the **Service Territory** gets added as a filter. The listed resources are part of that territory.

:::image type="content" source="media/territoryfilters.png" alt-text="Screenshot of the schedule assistant, showing a list of resources filtered by territory.":::

## Territories on the schedule board

Territories are also used on the schedule board to more effectively manage resources. For example, create schedule board tabs specific to a single territory that dispatcher manages.

On a new schedule board tab, add one or more territories as filters, and the resources shown adjust accordingly. Select **Save as Default** so the filters remain when you return later.

:::image type="content" source="media/territory-filter-schedule-board.png" alt-text="Screenshot of the schedule board, showing the territory tab.":::

To filter requirements by territories in the lower pane, select **Scheduler settings**. In **Board view settings**, set the **Apply territory filter to requirements** to **On**.

## Relate territories and postal codes

You can relate territories to postal codes. When the postal code is present on the account or work order address, the related territory is automatically filled in. Learn more in [Create and manage postal codes](set-up-postal-codes.md).

## Advanced scenarios

- **Territories as more than location.** Organizations frequently use territories in combination with the purpose of the resource group. For example, if there are resources who operate in Seattle and some are responsible for maintenance and others inspection, the organization can create two territories: "Seattle - maintenance" and "Seattle - inspection." It's helpful if different dispatchers manage each territory because they can have separate schedule board tabs for each resource group.

- **Variable territories.** Sometimes resources belong to different territories during different time periods. For example, a resource covers a small territory during the day, but a larger territory at night when demand is low. Field Service doesn't support variably territories by default. However, you could use a workflow to add and remove a resource from a territory based on the time of day.

- **Resources crews and territory filters.** Resource crews show on the schedule board if the crew header resource matches the territory. All crew members show even if resource children aren't part of that territory. Learn more in [Group resources in crews](resource-crews.md).

- **Using territories for non-field service scenarios.** Beyond field service, territories are useful in other scenarios. For example, salespeople assigned to sales territories that schedule time with leads, quotes, or opportunities. For this scenario, you can use a lookup to the service territory on the **Resource Requirement** form. Learn more in [Enable an entity for scheduling](schedule-new-entity.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
