---
title: Install Dynamics 365 Field Service
description: Learn how to install Dynamics 365 Field Service on a Power Platform environment.
ms.topic: how-to
ms.date: 02/26/2025
ms.author: jacoh
author: jasonccohen
---

# Install Dynamics 365 Field Service

After purchasing licenses for Field Service, an administrator installs the application on a Power Platform environment.

## Install on a new environment

Create a Power Platform environment with an attached **Dataverse data store** and turn on the **Enable Dynamics 365 apps** setting. Installing Field Service on an environment that doesn't meet these prerequisites isn't supported.

For detailed information, see [Create a Power Platform environment](/power-platform/admin/create-environment).

## Install on an existing environment

If your organization already maintains environments, you can [install the app on an existing environment with a database](/power-platform/admin/manage-apps#install-an-app). Similar to other Dynamics 365 business applications, the environment must have a Dataverse data store attached and Dynamics 365 apps enabled.

## Install a trial

When you [get a free trial](trial-signup.md), the Field Service application installs automatically on a new environment. After purchasing a license, you can [change the environment type to a production environment](/power-platform/admin/switch-environment).

## Access Field Service

Once the installation is complete, the "Field Service" and "Field Service Mobile" apps appear in the list of apps when you sign in to your Dynamics 365 organization. You can find these apps by going to:

```https://[your-environment-URL].crm.dynamics.com/apps```

:::image type="content" source="media/admin-apps.svg" alt-text="Screenshot of Field Service apps.":::

## Install and set up the Dynamics 365 Field Service mobile app

[Set up the mobile app](mobile/set-up-field-service-mobile.md) for frontline workers to use to view and complete work orders in the field.

## Next steps

After installing Field Service and the Field Service mobile app, see the following articles to configure the system to create, schedule, view, and complete work orders.

- [Set up users and security roles](users-licenses-permissions.md)
- [Create a bookable resource](set-up-bookable-resources.md)
- [Get started with Dynamics 365 Field Service](field-service-get-started.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
