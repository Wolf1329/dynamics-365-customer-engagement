---
title: "Profile Album (msdyn_PostAlbum) table/entity reference (Microsoft Dynamics 365 Customer Service)"
description: "Includes schema information and supported messages for the Profile Album (msdyn_PostAlbum) table/entity with Microsoft Dynamics 365 Customer Service."
ms.topic: generated-reference
author: gandhamm
ms.author: mgandham
search.audienceType: 
  - developer
---

# Profile Album (msdyn_PostAlbum) table/entity reference (Microsoft Dynamics 365 Customer Service)

Contains user profile images that are stored as attachments and displayed in posts.

> [!NOTE]
> The Microsoft Dynamics 365 Customer Service Profile Album (msdyn_PostAlbum) table extends the [Microsoft Dynamics 365 Profile Album (msdyn_PostAlbum) table](/dynamics365/developer/reference/entities/msdyn_postalbum).




## One-to-Many relationships

These relationships are one-to-many. Listed by **SchemaName**.

- [msdyn_postalbum_msdyn_bookingalerts](#BKMK_msdyn_postalbum_msdyn_bookingalerts)
- [msdyn_postalbum_msdyn_ocoutboundmessages](#BKMK_msdyn_postalbum_msdyn_ocoutboundmessages)

### <a name="BKMK_msdyn_postalbum_msdyn_bookingalerts"></a> msdyn_postalbum_msdyn_bookingalerts

Many-To-One Relationship: [msdyn_bookingalert msdyn_postalbum_msdyn_bookingalerts](msdyn_bookingalert.md#BKMK_msdyn_postalbum_msdyn_bookingalerts)

|Property|Value|
|---|---|
|ReferencingEntity|`msdyn_bookingalert`|
|ReferencingAttribute|`regardingobjectid`|
|ReferencedEntityNavigationPropertyName|`msdyn_postalbum_msdyn_bookingalerts`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `DoNotDisplay`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: <br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_postalbum_msdyn_ocoutboundmessages"></a> msdyn_postalbum_msdyn_ocoutboundmessages

Many-To-One Relationship: [msdyn_ocoutboundmessage msdyn_postalbum_msdyn_ocoutboundmessages](msdyn_ocoutboundmessage.md#BKMK_msdyn_postalbum_msdyn_ocoutboundmessages)

|Property|Value|
|---|---|
|ReferencingEntity|`msdyn_ocoutboundmessage`|
|ReferencingAttribute|`regardingobjectid`|
|ReferencedEntityNavigationPropertyName|`msdyn_postalbum_msdyn_ocoutboundmessages`|
|IsCustomizable|`False`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `DoNotDisplay`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: <br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|



### See also

[Dataverse table/entity reference](/power-apps/developer/data-platform/reference/about-entity-reference)  
[Dataverse Web API Reference](/power-apps/developer/data-platform/webapi/reference/about)   

