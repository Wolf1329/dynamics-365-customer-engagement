---
title: Sales literature entities (Dynamics 365 Sales)
description: Create and manage sales literature items to associate attachments and articles to enrich an organization's sales information.
ms.date: 01/30/2024
ms.topic: concept-article
author: udaykirang
ms.author: udag
ms.reviewer: udag
search.audienceType: 
  - developer

---
# Sales literature entities in Dynamics 365 Sales

A *sales literature* item is the basic unit of the marketing encyclopedia in Dynamics 365 Sales. For example, a business unit might decide to create an article about a specific product. The article can contain multiple sales literature items (sales attachments) such as a brochure, detailed specifications, and a CAD file, together with appropriate search terms, for example, "bolt" or "stainless steel." Any PC-compatible file format can be uploaded and attached to an article in the marketing encyclopedia. Specific search terms can be specified for each item.  
  
 You can use the sales literature management entities to create a central repository for your organization's sales information (in the form of  sales literature items (sales attachments)) that provides an easy way to distribute information to users, both online and offline. Sales literature can be organized into categories and types to provide easier management and searching. Dynamics 365 Sales also supports a subject manager and knowledge base.  
  
 A sales literature record can have one or more sales literature items (sales attachments) attached to it in various formats, such as .doc, .pub, and .pdf. An item can't be shared between sales literature records.  
  
 Sales literature records can also be attached to competitors and products (both yours and your competitors').  
  
 The following operations are supported in the marketing encyclopedia:  
  
- Create a sales literature item  
- View a sales literature item  
- Edit a sales literature item  
- Delete a sales literature item  
- Search for a sales literature item  
- Upload an attachment and attach it to a sales literature item  
  
  You can create a searchable marketing encyclopedia for storing various sales and marketing literature. As an example, a sales literature library might include the following:  
  
- Product information  
- Presentations and brochures  
- Policies and procedures  
- Sales literature  
- White papers  
- Competitive information  
- Price lists  
- Annual reports  
- Manuals  
  
## In This Section  

 [Sales Literature (SalesLiterature) table](../../developer/reference/entities/salesliterature.md)  
  
 [Sales Attachment (SalesLiteratureItem) table](../../developer/reference/entities/salesliteratureitem.md)  
  
## Related Sections  

 [Model your business data with Dataverse](/power-apps/maker/data-platform/data-platform-intro))  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
