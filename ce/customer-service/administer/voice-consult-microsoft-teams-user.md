---
title: Enable voice consult with Microsoft Teams user in the voice channel
description: Learn how to enable the consult experience between a customer service representative and Microsoft Teams user in the voice channel in Dynamics 365 Contact Center and Customer Service.
author: neeranelli
ms.author: nenellim
ms.reviewer: nenellim
ms.date: 07/28/2025
ms.topic: how-to
ms.collection:
ms.custom: bap-template
---

# Enable voice consult with Microsoft Teams users

[!INCLUDE[cc-feature-availability](../../includes/cc-feature-availability.md)]

[!INCLUDE[cc-rebrand-bot-agent](../../includes/cc-rebrand-bot-agent.md)]

Customer service isn't always limited to contact centers. Employees within the enterprise are often required to assist service representatives in customer service scenarios and talk to customers directly for highly technical or VIP engagements. You can enable your representative to consult with or transfer voice calls in Omnichannel for Customer Service to subject matter experts (SMEs) in Microsoft Teams using Voice Over Internet Protocol (VOIP). This feature is available through Azure Communication Services Call Automation.

With this feature, SMEs can participate in customer service conversations from Microsoft Teams directly without having to configure a phone number. Any Teams users in your tenant who is displayed in the Teams search box can receive calls from your representatives.

## Enable representatives to consult with Microsoft Teams users via VOIP

> [!NOTE]
> - Consult with and transfer to Microsoft Teams users via PSTN on the **Teams** tab of the dialer isn't supported. Use the **External number** tab to call numbers via PSTN.
> - You can enable consult with and transfer to Teams users via VOIP only. [Teams auto attendants](/microsoftteams/create-a-phone-system-auto-attendant) and [call queues](/microsoftteams/create-a-phone-system-call-queue) aren't supported.

To allow the representatives to consult with Microsoft Teams users, enable the **External Microsoft Teams users** in **Consult** and **Transfer** settings in the voice channel section of the voice workstream.

Calling services are charged on a per minute per participant basis at 0.004 per participant per minute and is less than the Public Switched Telephone Network (PSTN) charges of $0.013 per participant per minute.

Representatives can transfer or consult with Microsoft Teams users on certain Teams clients only. Learn more at [Supported Teams clients](/azure/communication-services/concepts/call-automation/call-automation-teams-interop#supported-teams-clients).

If the Teams user rejects the call or is unavailable, there isn't an option to leave a voicemail for the caller and the call isn't forwarded to another number. The call from Dynamics 365 is considered as a group call, and Teams doesn't honor voicemail or call forwarding settings when you add a Teams user to a group call.

To enable the consult and transfer experience through VOIP, perform the following prerequisites:

- The enhanced voice channel must be enabled for your organization.
- The following IP address ranges must be allowed:
   - Azure Communication Services: [Firewall configuration](/azure/communication-services/concepts/voice-video-calling/network-requirements#firewall-configuration)
   - Microsoft Teams: [Skype for Business Online and Microsoft Teams](/microsoft-365/enterprise/urls-and-ip-address-ranges#skype-for-business-online-and-microsoft-teams)
- The Teams users who are added to calls must have [Teams Phone System Licenses](/microsoftteams/setting-up-your-phone-system) assigned.
-  Enterprise Voice must be enabled. To enable Enterprise Voice, run the following PowerShell command.
    ```powershell
    Set-CSPhoneNumberAssignment –Identity [user email address] -EnterpriseVoiceEnabled $true
    ```
-  [External Access Policy](/azure/communication-services/concepts/interop/enable-interoperability-teams#4-enable-tenant-policy) must be enabled. Run the following PowerShell command to enable External Access:
    ```powershell
    Set-CsExternalAccessPolicy -Identity Global -EnableAcsFederationAccess $true
    ```
-  The [Teams and Azure Communication Services federation](/azure/communication-services/concepts/interop/enable-interoperability-teams#enable-interoperability-in-your-teams-tenant) for a Teams tenant must be enabled and the Azure Communication Services resources that can connect to Teams is specified. Perform the following steps:
Get the [immutable resource ID](/azure/communication-services/concepts/troubleshooting-info#getting-immutable-resource-id) of the Azure Communications Service resource and then run the following PowerShell cmdlets on your computer. Make sure you have **Reader** access to the Azure Communications Service resource.
- Run `Get-module *teams*` to verify if the Microsoft Teams is installed. If it isn't installed, perform the following steps:
    - `Install-Module -Name MicrosoftTeams`
    - `Update-Module MicrosoftTeams`
- Connect to Microsoft Teams and run `Connect-MicrosoftTeams`. This command opens a sign-in window. The user must sign in with their Microsoft Teams admin account.
- Get Microsoft Teams Azure Communication Services allowlist.
    - Run `Get-CsTeamsAcsFederationConfiguration` and note the existing Azure Communication Services resource IDs in the allowlist. The Azure Communication Services resource IDs are existing resource IDs for orgs that are enabled for Teams Azure Communications Service federation.
    - Add current Azure Communications Service resource ID to these existing resource IDs when you run the `Set-CsTeamsAcsFederationConfiguration` command in the next step.
 - Set Teams Azure Communications Service allowlist.
     - Run `$allowlist = @('<UPDATED_ACS_RESOURCE_IDs>') Set-CsTeamsAcsFederationConfiguration -EnableAcsUsers $True -AllowedAcsResources $allowlist`
  

To revoke External Access and disable this feature, run

```powershell
   Set-CsExternalAccessPolicy -Identity Global -EnableAcsFederationAccess $false
```

### Related information

[Introduction to the voice channel](voice-channel.md)  
[Representative consult with Microsoft Teams users](../use/voice-channel-transfer-consult.md)  
