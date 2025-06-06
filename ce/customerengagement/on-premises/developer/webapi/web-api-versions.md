---
title: "Dynamics 365 Customer Engagement Web API Versions (Developer Guide for Dynamics 365 Customer Engagement)| MicrosoftDocs"
description: "Read how versioning of Dynamics 365 Customer Engagement Web API works. Dynamics 365 Customer Engagement Web API versions support version specific differences in the same environment, which is different from the behavior in the v8.x releases in which new capabilities were additive"
ms.custom: 
ms.reviewer: pehecke

ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
applies_to: 
  - Dynamics 365 Customer Engagement (on-premises)
ms.assetid: d9bb79a5-2bfa-4ffe-8cb4-60f192359489
caps.latest.revision: 34
author: JimDaly
ms.author: jdaly
search.audienceType: 
  - developer

---
# Dynamics 365 Customer Engagement Web API Versions

Beginning with the [!INCLUDE[pn_crm_9_0_0_online](../../includes/pn-crm-9-0-0-online.md)] (v9.x) release, the [!INCLUDE[pn_ms_dyn_365](../../includes/pn-ms-dyn-365.md)] for Customer Engagement (on-premises) Web API supports version specific differences in the same environment.  
  
 This support is different from the behavior for the v8.*x* releases. In the previous releases, new capabilities were available to any version of the service depending on the update applied to the environment. After an upgrade to v8.2, the v8.0, and v8.1 services were all identical. This commonality was possible because all the changes were additive. Nothing was removed or introduced breaking changes. As a result, the specific version referenced in the service URL for the v8.*x* wasn't important.  
  
 Going forward, the capabilities of the service can change, including potentially breaking changes such as removing specific operations. This flexibility will allow for improvements to be applied on an on-going basis. This topic will record any version specific differences and any limitations where the Web API hasn't yet achieved parity with the organization service.  
  
## Web API Limitations  

 The [!INCLUDE[pn_ms_dyn_365](../../includes/pn-ms-dyn-365.md)] for Customer Engagement (on-premises) Web API provides complete parity with the capabilities of the organization service. For [!INCLUDE[pn_crm_9_0_0_online](../../includes/pn-crm-9-0-0-online.md)], this topic describes the limitations carried forward from the [!INCLUDE[pn_crm_8_2_0_online](../../includes/pn-crm-8-2-0-online.md)] release.          For earlier releases, see [Dynamics CRM 2016 Web API Limitations](https://msdn.microsoft.com/library/mt628816\(CRM.8\).aspx).  
  
## Limitations addressed in [!INCLUDE[pn_crm_9_0_0_online](../../includes/pn-crm-9-0-0-online.md)]  
 In version 8.2, some custom actions were not available in Web API.
> [!NOTE]
>  This issue is addressed in [!INCLUDE[pn_crm_9_0_0_online](../../includes/pn-crm-9-0-0-online.md)].  
  
 If you defined a custom action, which includeed a complex return value and a simple return value, a corresponding Action was not available in the Web API but was available using the Organization service. A complex return value is an `EntityReference`, `Entity`, or `EntityCollection`. You can have any combination of simple return values or a single complex return value. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Create your own actions](../create-own-actions.md)  
 
## New operations added  
 The following operations have been added to the Web API for [!INCLUDE[pn_crm_9_0_0_online](../../includes/pn-crm-9-0-0-online.md)].  
  
- <xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest>
- <xref:Microsoft.Crm.Sdk.Messages.ModifyAccessRequest>
- <xref:Microsoft.Crm.Sdk.Messages.RetrieveSharedPrincipalsAndAccessRequest>| 
  
### See also  
 [Use the Dynamics 365 Customer Engagement Web API](../use-microsoft-dynamics-365-web-api.md)   
 [Authenticate to Dynamics 365 Customer Engagement (on-premises) with the Web API](authenticate-web-api.md)   
 

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]