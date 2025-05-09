---
title: Enable address suggestions
description: Learn how to enable the address suggestion feature in Dynamics 365 Sales to help sellers save time and reduce errors when they enter address information.
author: lavanyakr01
ms.author: lavanyakr
ms.reviewer: lavanyakr
ms.topic: how-to
ms.collection: get-started
ms.date: 03/25/2025
ms.custom:
 - bap-template
 - ai-gen-docs-bap
 - ai-gen-desc
 - ai-seo-date:08/30/2023
---

# Enable address suggestions

Enable the address suggestion feature in Dynamics 365 Sales to help sellers save time and reduce errors when they enter the addresses of their contacts, leads, and accounts. When a seller starts typing in the address field, Bing Maps suggests a list of addresses that match what the seller is typing. When the seller selects an address in the list, the address fields in the form are filled automatically. You need to enable Bing Maps before you can enable address suggestions.

> [!IMPORTANT]
> The address suggestion feature works only on out-of-the-box forms. If you have customized the form or the address field in the out-of-the-box form, the feature doesn't work.

## Enable Bing Maps

When you enable Bing Maps in the Sales settings, sellers can see the address of their accounts, contacts, and leads on a map and get directions. You must enable Bing Maps before you can enable the address suggestion feature in Sales.

Bing Maps is enabled by default in new environments that are located outside the European Union (EU). To opt in to use Bing Maps, EU customers must view the privacy notice and consent to share data with an external system.

> [!IMPORTANT]
> By connecting to a mapping service, you consent to allow the system&mdash;including systems in Government Cloud environments&mdash;to share your data. "Mapping service" refers to Bing Maps or any other third-party mapping service that's designated by you or your operating system. Data that's shared with external systems outside of your Microsoft Dynamics 365 environment includes, but is not limited to, addresses and coordinates. Your use of the mapping service is also subject to the service's separate terms of use. Data imported from external systems into Microsoft Dynamics 365 are subject to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).

1. In the sales app, go to **Settings** > **Advanced Settings**.

1. Go to **System** > **Administration**, and then select **General**.

1. Under **Enable Bing Maps**, set the **Show Bing Maps on forms** toggle to **Yes**.

1. Select **Save**.

## Enable the address suggestion feature


1. In the Sales Hub app at the bottom of the left side panel, select **App Settings**.

1. Go to **General Settings** > **Productivity tools** > **Enable address suggestions**.

1. Turn on the toggle and select **Save**.

To verify the changes, open a contact, lead, or account form. You should see a new **Address** field and a Bing map after all the individual address fields. The field suggests addresses as you type and populates address fields when you select an address as shown in the following screenshot:

:::image type="content" source="media/address-suggestion-field-map.png" alt-text="Screenshot of the new address field in a form" lightbox="media/address-suggestion-field-map.png":::

> [!NOTE]
>- If your organization is using Dynamics 365 Field Service and has [enabled address suggestions](/dynamics365/field-service/field-service-maps-address-locations#enable-address-suggestions), then the address suggestions for the main contact and account forms are controlled by the Field Service settings.

