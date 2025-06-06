---
title: Configure mobile apps with Microsoft Intune
description: How to configure the Dynamics 365 Sales mobile app with Microsoft Intune. This includes how to add, and deploy, the application. And, how to create the mobile application policy to control security.
ms.date: 05/02/2025
ms.topic: how-to
author: sbmjais
ms.author: shjais
ms.reviewer: shjais 
---

# Configure mobile apps with Microsoft Intune 

Microsoft Intune enables organizations to manage devices and applications. The Dynamics 365 Sales mobile applications for iOS and Android integrate with Intune. This integration enables you to manage the application on your devices, and to control security. Through configuration policies, you can control items like requiring an access pin, how data is handled by the application, and even encrypting application data when the app is not in use.

The Microsoft Dynamics 365 Sales mobile app allows you to get access to your important business information. You can view and interact with your dashboards and reports for all your organization's managed device and app business data. For more information about supported Intune apps, see [Microsoft Intune protected apps](/mem/intune/apps/apps-supported-intune-apps).

## General mobile device management configuration

This article assumes that Intune is configured properly and you have devices enrolled with Intune. The article is not meant as a full configuration guide for Microsoft Intune. For more information on Intune, see [What is Intune?](/mem/intune/fundamentals/what-is-intune).

Microsoft Intune can co-exist with Mobile Device Management (MDM) within Microsoft 365. If you're using MDM, the device will show as enrolled with MDM, but is available to manage in Intune.

Before end users can use the Dynamics 365 Sales mobile app on their devices, an Intune admin must add the app to Intune and also assign the app to end users.

## Step 1: Add the Dynamics 365 Sales mobile app to Intune

To add the Dynamics 365 Sales mobile app to Intune, use the steps provided in the following topics:
- [Add iOS store apps to Microsoft Intune](/mem/intune/apps/store-apps-ios)
- [Add Android store apps to Microsoft Intune](/mem/intune/apps/store-apps-android)

## Step 2: Assign the app to your end users

After you've added the Dynamics 365 Sales mobile app to Microsoft Intune, you can assign the app to users and devices. It's important to note that you can assign an app to a device whether or not the device is managed by Intune.

To assign the Dynamics 365 Sales mobile app to users and devices, use the steps provided in [Assign apps to groups with Microsoft Intune](/mem/intune/apps/apps-deploy).

## Step 3: Create and assign app protection policies

App protection policies (APP) are rules that ensure an organization's data remains safe or contained in a managed app. A policy can be a rule that is enforced when the user attempts to access or move "corporate" data, or a set of actions that are prohibited or monitored when the user is inside the app. A managed app is an app that has app protection policies applied to it, and can be managed by Intune.

Mobile Application Management (MAM) app protection policies allows you to manage and protect your organization's data within an application. With MAM without enrollment (MAM-WE), a work or school-related app that contains sensitive data can be managed on almost any device, including personal devices in bring-your-own-device (BYOD) scenarios. For more information, see [App protection policies overview](/mem/intune/apps/app-protection-policy).

To create and assign an app protection policy for the Dynamics 365 Sales mobile app, use the steps provided in [How to create and assign app protection policies](/mem/intune/apps/app-protection-policies).

## Step 4: Use the application on a device

Managed apps are apps that your company support can set up to help protect company data that you can access in that app. When you access company data in a managed app on your device, you may notice that the app works a little differently than what you expect. For example, you might not be able to copy and paste protected company data, or you might not be able to save that data to certain locations.

To understand how your end users can use the Dynamics 365 Sales mobile app on their device, review the steps provided in the following articles:
- [Use managed apps on your iOS device](/mem/intune/fundamentals/manage-apps)
- [Use managed apps on your Android device](/mem/intune/fundamentals/manage-apps)

## Related information

[How to create and assign app protection policies](/mem/intune/apps/app-protection-policies) 

