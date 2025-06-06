---
title: "Privacy notices for Sales Insights | Microsoft Docs"
description: "Privacy notices for Sales Insights capabilities such as, standard features, premium features, conversation intelligence, and data protection."
keywords: "privacy notice, privacy statement addition"
ms.date: 02/27/2025
ms.custom: "dyn365-ai-sales"
ms.topic: legal
author: udaykirang
ms.author: udag
ms.reviewer: udag
---


# Sales Insights privacy notice 

This article covers privacy notices for Sales Insights capabilities. Your privacy is important to us. For Microsoft Online Services, read the [Microsoft Online Services privacy Statement](https://go.microsoft.com/fwlink/p/?LinkID=389041).

## Sales Insights standard features

For specific privacy information about Sales insights standard features, refer to the paragraphs below.

[!INCLUDE[cc_privacy_relationship_insights_relationship_assistant](../includes/cc-privacy-relationship-insights-relationship-assistant.md)]  
[!INCLUDE[cc_privacy_relationship_insights_email_engagement](../includes/cc-privacy-relationship-insights-email-engagement.md)]  
[!INCLUDE[cc_privacy_relationship_insights_auto_capture](../includes/cc-privacy-relationship-insights-auto-capture.md)]

## Sales Insights premium features

For specific privacy information about Dynamics 365 Sales Insights premium features, refer to the paragraphs below.  
By enabling [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] capabilities, [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Data will be sent to and used by (1) Azure Data Factory for the purpose of data movement and transformation for KPI computation, and (2) Azure Container Instance for the purpose of predictive model training and scoring. By installing this solution, you agree for this limited set of data to be sent to Azure Data Factory service and Azure Container Instance. The data that is sent include contacts, opportunities, leads, accounts, activities, and additional metadata information.  
Azure components and services that are involved with Dynamics 365 Sales Insights are detailed in the following sections.
[!Include[cc_privacy_note_azure_trust_center](../includes/cc-privacy-note-azure-trust-center.md)]  

**Azure Data Factory**  
[!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] uses Azure Data Factory, a cloud data integration service, to orchestrate and automate the movement and transformation of data (including Customer Data) between services.

**Azure batch services**   
[!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] uses Azure batch service, a cloud-based batch service, to create predictive model training and scoring pipelines dynamically. 

**Installation and Removal of Dynamics 365 Sales Insights**    
An administrator can enable [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] capabilities by installing it as a solution in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] organization. In addition, an administrator can subsequently disable the feature by uninstalling this solution from the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] organization.

## Conversation intelligence

For specific privacy information about conversation intelligence of Dynamics 365 Sales, refer to the paragraphs below.

**Azure Services**   
Azure components and services that are involved with conversation intelligence are detailed in the following sections.  
[!Include[cc_privacy_note_azure_trust_center](../includes/cc-privacy-note-azure-trust-center.md)]

**Azure Data Factory**  
[!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] Preview uses Azure Data Factory, a cloud data integration service, to orchestrate and automate the movement and transformation of data (including Customer Data) between services.

**Installation and removal of conversation intelligence**    
[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] users and administrators who are allowed to register new applications in Microsoft Entra ID, can enable conversation intelligence by signing in to the app and consenting to the required permissions. Administrators can change these permissions, which can include removing access to the app, at https://myapps.microsoft.com 

**Handling privacy laws for conversation intelligence data**    
It is the enterprise customer’s responsibility to comply with the privacy laws and regulations. If you choose to honor and execute a data subject rights (DSR) request for delete or edit, review the information in the following note:

[!INCLUDE [gdpr-dsr-azure-note](~/../shared-content/shared/privacy-includes/gdpr-dsr-azure-note.md)]

## Data protection

Data as it is in transit between user devices and the Microsoft datacenters are secured. Connections established between customers and Microsoft datacenters are encrypted, and all public endpoints are secured using industry-standard TLS. TLS effectively establishes a security-enhanced browser to server connection to help ensure data confidentiality and integrity between desktops and datacenters. API access from the customer endpoint to the server is also similarly protected. Currently, TLS 1.2 (or higher) is required for accessing the server endpoints.

All the data stored as part of sales insights are encrypted using Microsoft encryption keys.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
