---
title: "Resource Requirement (msdyn_resourcerequirement) table/entity reference (Microsoft Dynamics 365 Customer Service)"
description: "Includes schema information and supported messages for the Resource Requirement (msdyn_resourcerequirement) table/entity with Microsoft Dynamics 365 Customer Service."
ms.topic: generated-reference
author: gandhamm
ms.author: mgandham
search.audienceType: 
  - developer
---

# Resource Requirement (msdyn_resourcerequirement) table/entity reference (Microsoft Dynamics 365 Customer Service)



## Messages

The following table lists the messages for the Resource Requirement (msdyn_resourcerequirement) table.
Messages represent operations that can be performed on the table. They may also be events.

| Name <br />Is Event? |Web API Operation |SDK for .NET |
| ---- | ----- |----- |
| `Assign`<br />Event: True |`PATCH` /msdyn_resourcerequirements(*msdyn_resourcerequirementid*)<br />[Update](/powerapps/developer/data-platform/webapi/update-delete-entities-using-web-api#basic-update) the `ownerid` property. |<xref:Microsoft.Crm.Sdk.Messages.AssignRequest>|
| `Associate`<br />Event: True |[Associate records](/power-apps/developer/data-platform/webapi/associate-disassociate-entities-using-web-api) |[Associate records](/power-apps/developer/data-platform/org-service/entity-operations-associate-disassociate#use-the-associate-method-or-associaterequest)|
| `BulkRetain`<br />Event: True |<xref:Microsoft.Dynamics.CRM.BulkRetain?displayProperty=nameWithType /> |[Learn to use messages with the SDK for .NET](/power-apps/developer/data-platform/org-service/use-messages)|
| `Create`<br />Event: True |`POST` /msdyn_resourcerequirements<br />See [Create](/powerapps/developer/data-platform/webapi/create-entity-web-api) |[Create records](/power-apps/developer/data-platform/org-service/entity-operations-create#basic-create)|
| `CreateMultiple`<br />Event: True |<xref:Microsoft.Dynamics.CRM.CreateMultiple?displayProperty=nameWithType /> |<xref:Microsoft.Xrm.Sdk.Messages.CreateMultipleRequest>|
| `Delete`<br />Event: True |`DELETE` /msdyn_resourcerequirements(*msdyn_resourcerequirementid*)<br />See [Delete](/powerapps/developer/data-platform/webapi/update-delete-entities-using-web-api#basic-delete) |[Delete records](/power-apps/developer/data-platform/org-service/entity-operations-update-delete#basic-delete)|
| `Disassociate`<br />Event: True |[Disassociate records](/power-apps/developer/data-platform/webapi/associate-disassociate-entities-using-web-api) |[Disassociate records](/power-apps/developer/data-platform/org-service/entity-operations-associate-disassociate#use-the-disassociate-method-or-disassociaterequest)|
| `GrantAccess`<br />Event: True |<xref:Microsoft.Dynamics.CRM.GrantAccess?displayProperty=nameWithType /> |<xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest>|
| `IsValidStateTransition`<br />Event: False |<xref:Microsoft.Dynamics.CRM.IsValidStateTransition?displayProperty=nameWithType /> |<xref:Microsoft.Crm.Sdk.Messages.IsValidStateTransitionRequest>|
| `ModifyAccess`<br />Event: True |<xref:Microsoft.Dynamics.CRM.ModifyAccess?displayProperty=nameWithType /> |<xref:Microsoft.Crm.Sdk.Messages.ModifyAccessRequest>|
| `msdyn_BookingResourceRequirement`<br />Event: True |**msdyn_BookingResourceRequirement action** |[Learn to use messages with the SDK for .NET](/power-apps/developer/data-platform/org-service/use-messages)|
| `PurgeRetainedContent`<br />Event: True |<xref:Microsoft.Dynamics.CRM.PurgeRetainedContent?displayProperty=nameWithType /> |[Learn to use messages with the SDK for .NET](/power-apps/developer/data-platform/org-service/use-messages)|
| `Restore`<br />Event: True |<xref:Microsoft.Dynamics.CRM.Restore?displayProperty=nameWithType /> |[Learn to use messages with the SDK for .NET](/power-apps/developer/data-platform/org-service/use-messages)|
| `Retain`<br />Event: True |<xref:Microsoft.Dynamics.CRM.Retain?displayProperty=nameWithType /> |[Learn to use messages with the SDK for .NET](/power-apps/developer/data-platform/org-service/use-messages)|
| `Retrieve`<br />Event: True |`GET` /msdyn_resourcerequirements(*msdyn_resourcerequirementid*)<br />See [Retrieve](/powerapps/developer/data-platform/webapi/retrieve-entity-using-web-api) |[Retrieve records](/power-apps/developer/data-platform/org-service/entity-operations-retrieve)|
| `RetrieveMultiple`<br />Event: True |`GET` /msdyn_resourcerequirements<br />See [Query data](/power-apps/developer/data-platform/webapi/query-data-web-api) |[Query data](/power-apps/developer/data-platform/org-service/entity-operations-query-data)|
| `RetrievePrincipalAccess`<br />Event: True |<xref:Microsoft.Dynamics.CRM.RetrievePrincipalAccess?displayProperty=nameWithType /> |<xref:Microsoft.Crm.Sdk.Messages.RetrievePrincipalAccessRequest>|
| `RetrieveSharedPrincipalsAndAccess`<br />Event: True |<xref:Microsoft.Dynamics.CRM.RetrieveSharedPrincipalsAndAccess?displayProperty=nameWithType /> |<xref:Microsoft.Crm.Sdk.Messages.RetrieveSharedPrincipalsAndAccessRequest>|
| `RevokeAccess`<br />Event: True |<xref:Microsoft.Dynamics.CRM.RevokeAccess?displayProperty=nameWithType /> |<xref:Microsoft.Crm.Sdk.Messages.RevokeAccessRequest>|
| `RollbackRetain`<br />Event: True |<xref:Microsoft.Dynamics.CRM.RollbackRetain?displayProperty=nameWithType /> |[Learn to use messages with the SDK for .NET](/power-apps/developer/data-platform/org-service/use-messages)|
| `SetState`<br />Event: True |`PATCH` /msdyn_resourcerequirements(*msdyn_resourcerequirementid*)<br />[Update](/powerapps/developer/data-platform/webapi/update-delete-entities-using-web-api#basic-update) the `statecode` and `statuscode` properties. |<xref:Microsoft.Crm.Sdk.Messages.SetStateRequest>|
| `Update`<br />Event: True |`PATCH` /msdyn_resourcerequirements(*msdyn_resourcerequirementid*)<br />See [Update](/powerapps/developer/data-platform/webapi/update-delete-entities-using-web-api#basic-update) |[Update records](/power-apps/developer/data-platform/org-service/entity-operations-update-delete#basic-update)|
| `UpdateMultiple`<br />Event: True |<xref:Microsoft.Dynamics.CRM.UpdateMultiple?displayProperty=nameWithType /> |<xref:Microsoft.Xrm.Sdk.Messages.UpdateMultipleRequest>|
| `Upsert`<br />Event: False |`PATCH` /msdyn_resourcerequirements(*msdyn_resourcerequirementid*)<br />See [Upsert a table row](/powerapps/developer/data-platform/webapi/update-delete-entities-using-web-api#upsert-a-table-row) |<xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest>|
| `UpsertMultiple`<br />Event: False |<xref:Microsoft.Dynamics.CRM.UpsertMultiple?displayProperty=nameWithType /> |<xref:Microsoft.Xrm.Sdk.Messages.UpsertMultipleRequest>|
| `ValidateRetentionConfig`<br />Event: True |<xref:Microsoft.Dynamics.CRM.ValidateRetentionConfig?displayProperty=nameWithType /> |[Learn to use messages with the SDK for .NET](/power-apps/developer/data-platform/org-service/use-messages)|

## Properties

The following table lists selected properties for the Resource Requirement (msdyn_resourcerequirement) table.

|Property|Value|
| --- | --- |
| **DisplayName** | **Resource Requirement** |
| **DisplayCollectionName** | **Resource Requirements** |
| **SchemaName** | `msdyn_resourcerequirement` |
| **CollectionSchemaName** | `msdyn_resourcerequirements` |
| **EntitySetName** | `msdyn_resourcerequirements`|
| **LogicalName** | `msdyn_resourcerequirement` |
| **LogicalCollectionName** | `msdyn_resourcerequirements` |
| **PrimaryIdAttribute** | `msdyn_resourcerequirementid` |
| **PrimaryNameAttribute** |`msdyn_name` |
| **TableType** | `Standard` |
| **OwnershipType** | `UserOwned` |

## Writable columns/attributes

These columns/attributes return true for either **IsValidForCreate** or **IsValidForUpdate** (usually both). Listed by **SchemaName**.

- [ImportSequenceNumber](#BKMK_ImportSequenceNumber)
- [msdyn_allocationmethod](#BKMK_msdyn_allocationmethod)
- [msdyn_AppointmentRequirementId](#BKMK_msdyn_AppointmentRequirementId)
- [msdyn_BookingSetupMetadataId](#BKMK_msdyn_BookingSetupMetadataId)
- [msdyn_CalendarId](#BKMK_msdyn_CalendarId)
- [msdyn_duration](#BKMK_msdyn_duration)
- [msdyn_effort](#BKMK_msdyn_effort)
- [msdyn_fromdate](#BKMK_msdyn_fromdate)
- [msdyn_FulfilledDuration](#BKMK_msdyn_FulfilledDuration)
- [msdyn_InternalFlags](#BKMK_msdyn_InternalFlags)
- [msdyn_IsPrimary](#BKMK_msdyn_IsPrimary)
- [msdyn_istemplate](#BKMK_msdyn_istemplate)
- [msdyn_Latitude](#BKMK_msdyn_Latitude)
- [msdyn_Longitude](#BKMK_msdyn_Longitude)
- [msdyn_name](#BKMK_msdyn_name)
- [msdyn_percentage](#BKMK_msdyn_percentage)
- [msdyn_PoolType](#BKMK_msdyn_PoolType)
- [msdyn_Priority](#BKMK_msdyn_Priority)
- [msdyn_ProposedDuration](#BKMK_msdyn_ProposedDuration)
- [msdyn_RemainingDuration](#BKMK_msdyn_RemainingDuration)
- [msdyn_requirementgroupcontrolviewid](#BKMK_msdyn_requirementgroupcontrolviewid)
- [msdyn_requirementgroupid](#BKMK_msdyn_requirementgroupid)
- [msdyn_requirementrelationshipid](#BKMK_msdyn_requirementrelationshipid)
- [msdyn_resourcerequirementId](#BKMK_msdyn_resourcerequirementId)
- [msdyn_resourcetype](#BKMK_msdyn_resourcetype)
- [msdyn_serviceappointment](#BKMK_msdyn_serviceappointment)
- [msdyn_sortoptions](#BKMK_msdyn_sortoptions)
- [msdyn_Status](#BKMK_msdyn_Status)
- [msdyn_templaterequirementid](#BKMK_msdyn_templaterequirementid)
- [msdyn_Territory](#BKMK_msdyn_Territory)
- [msdyn_TimeFromPromised](#BKMK_msdyn_TimeFromPromised)
- [msdyn_TimeGroup](#BKMK_msdyn_TimeGroup)
- [msdyn_TimeToPromised](#BKMK_msdyn_TimeToPromised)
- [msdyn_TimeWindowEnd](#BKMK_msdyn_TimeWindowEnd)
- [msdyn_TimeWindowStart](#BKMK_msdyn_TimeWindowStart)
- [msdyn_timezonefortimewindow](#BKMK_msdyn_timezonefortimewindow)
- [msdyn_todate](#BKMK_msdyn_todate)
- [msdyn_TzaFromDate](#BKMK_msdyn_TzaFromDate)
- [msdyn_TzaToDate](#BKMK_msdyn_TzaToDate)
- [msdyn_workhourtemplate](#BKMK_msdyn_workhourtemplate)
- [msdyn_WorkLocation](#BKMK_msdyn_WorkLocation)
- [OverriddenCreatedOn](#BKMK_OverriddenCreatedOn)
- [OwnerId](#BKMK_OwnerId)
- [OwnerIdType](#BKMK_OwnerIdType)
- [statecode](#BKMK_statecode)
- [statuscode](#BKMK_statuscode)
- [TimeZoneRuleVersionNumber](#BKMK_TimeZoneRuleVersionNumber)
- [UTCConversionTimeZoneCode](#BKMK_UTCConversionTimeZoneCode)

### <a name="BKMK_ImportSequenceNumber"></a> ImportSequenceNumber

|Property|Value|
|---|---|
|Description|**Sequence number of the import that created this record.**|
|DisplayName|**Import Sequence Number**|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|`importsequencenumber`|
|RequiredLevel|None|
|Type|Integer|
|MaxValue|2147483647|
|MinValue|-2147483648|

### <a name="BKMK_msdyn_allocationmethod"></a> msdyn_allocationmethod

|Property|Value|
|---|---|
|Description|**Select the allocation method to be used for creating requirement distribution over a time period.**|
|DisplayName|**Allocation Method**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_allocationmethod`|
|RequiredLevel|ApplicationRequired|
|Type|Picklist|
|DefaultFormValue|192350000|
|GlobalChoiceName|`msdyn_resourcerequirement_msdyn_allocationmethod`|

#### msdyn_allocationmethod Choices/Options

|Value|Label|
|---|---|
|192350000|**None**|
|192350001|**Full capacity**|
|192350003|**Distribute evenly**|
|192350004|**Percentage capacity**|
|192350005|**Front load**|

### <a name="BKMK_msdyn_AppointmentRequirementId"></a> msdyn_AppointmentRequirementId

|Property|Value|
|---|---|
|Description|**Unique identifier for Appointment associated with Resource Requirement.**|
|DisplayName|**Appointment Requirement**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_appointmentrequirementid`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|appointment|

### <a name="BKMK_msdyn_BookingSetupMetadataId"></a> msdyn_BookingSetupMetadataId

|Property|Value|
|---|---|
|Description|**A unique identifier for the booking setup metadata that is associated with a resource requirement.**|
|DisplayName|**Booking Setup Metadata**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_bookingsetupmetadataid`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|msdyn_bookingsetupmetadata|

### <a name="BKMK_msdyn_CalendarId"></a> msdyn_CalendarId

|Property|Value|
|---|---|
|Description|**The calendar that will be used for a resource requirement**|
|DisplayName|**Calendar Id**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_calendarid`|
|RequiredLevel|None|
|Type|String|
|Format|Text|
|FormatName|Text|
|ImeMode|Auto|
|IsLocalizable|False|
|MaxLength|100|

### <a name="BKMK_msdyn_duration"></a> msdyn_duration

|Property|Value|
|---|---|
|Description|**Duration of total minutes required**|
|DisplayName|**Duration**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_duration`|
|RequiredLevel|None|
|Type|Integer|
|MaxValue|2147483647|
|MinValue|0|

### <a name="BKMK_msdyn_effort"></a> msdyn_effort

|Property|Value|
|---|---|
|Description|**Effort that's required from resource capacity**|
|DisplayName|**Effort**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_effort`|
|RequiredLevel|None|
|Type|Decimal|
|ImeMode|Auto|
|MaxValue|1000000000|
|MinValue|0.0001|
|Precision|4|
|SourceTypeMask|0|

### <a name="BKMK_msdyn_fromdate"></a> msdyn_fromdate

|Property|Value|
|---|---|
|Description||
|DisplayName|**From Date**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_fromdate`|
|RequiredLevel|Recommended|
|Type|DateTime|
|CanChangeDateTimeBehavior|False|
|DateTimeBehavior|UserLocal|
|Format|DateOnly|
|ImeMode|Auto|
|SourceTypeMask|0|

### <a name="BKMK_msdyn_FulfilledDuration"></a> msdyn_FulfilledDuration

|Property|Value|
|---|---|
|Description|**The fulfilled duration, in minutes.**|
|DisplayName|**Fulfilled Duration**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_fulfilledduration`|
|RequiredLevel|None|
|Type|Integer|
|MaxValue|2147483647|
|MinValue|0|

### <a name="BKMK_msdyn_InternalFlags"></a> msdyn_InternalFlags

|Property|Value|
|---|---|
|Description|**For internal use only.**|
|DisplayName|**Internal Flags**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_internalflags`|
|RequiredLevel|None|
|Type|Memo|
|Format|Text|
|FormatName|Text|
|ImeMode|Auto|
|IsLocalizable|False|
|MaxLength|1048576|

### <a name="BKMK_msdyn_IsPrimary"></a> msdyn_IsPrimary

|Property|Value|
|---|---|
|Description||
|DisplayName|**Is Primary**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_isprimary`|
|RequiredLevel|None|
|Type|Boolean|
|GlobalChoiceName|`msdyn_resourcerequirement_msdyn_isprimary`|
|DefaultValue|False|
|True Label|Yes|
|False Label|No|

### <a name="BKMK_msdyn_istemplate"></a> msdyn_istemplate

|Property|Value|
|---|---|
|Description|**Is template requirement**|
|DisplayName|**Is Template**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_istemplate`|
|RequiredLevel|None|
|Type|Boolean|
|GlobalChoiceName|`msdyn_resourcerequirement_msdyn_istemplate`|
|DefaultValue|False|
|True Label|Yes|
|False Label|No|

### <a name="BKMK_msdyn_Latitude"></a> msdyn_Latitude

|Property|Value|
|---|---|
|Description|**The latitude to use for the location of a requirement.**|
|DisplayName|**Latitude**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_latitude`|
|RequiredLevel|None|
|Type|Double|
|ImeMode|Auto|
|MaxValue|90|
|MinValue|-90|
|Precision|5|

### <a name="BKMK_msdyn_Longitude"></a> msdyn_Longitude

|Property|Value|
|---|---|
|Description|**The longitude to use for the location of a requirement.**|
|DisplayName|**Longitude**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_longitude`|
|RequiredLevel|None|
|Type|Double|
|ImeMode|Auto|
|MaxValue|180|
|MinValue|-180|
|Precision|5|

### <a name="BKMK_msdyn_name"></a> msdyn_name

|Property|Value|
|---|---|
|Description|**The name of the custom entity.**|
|DisplayName|**Name**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_name`|
|RequiredLevel|Recommended|
|Type|String|
|Format|Text|
|FormatName|Text|
|ImeMode|Auto|
|IsLocalizable|False|
|MaxLength|100|

### <a name="BKMK_msdyn_percentage"></a> msdyn_percentage

|Property|Value|
|---|---|
|Description|**Enter the percentage of the calendar capacity required.**|
|DisplayName|**Percentage**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_percentage`|
|RequiredLevel|None|
|Type|Decimal|
|ImeMode|Auto|
|MaxValue|100000000000|
|MinValue|-100000000000|
|Precision|2|
|SourceTypeMask|0|

### <a name="BKMK_msdyn_PoolType"></a> msdyn_PoolType

|Property|Value|
|---|---|
|Description||
|DisplayName|**Pool Type**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_pooltype`|
|RequiredLevel|None|
|Type|MultiSelectPicklist|
|DefaultFormValue||
|GlobalChoiceName|`msdyn_pooltype`|

#### msdyn_PoolType Choices/Options

|Value|Label|
|---|---|
|192350000|**Account**|
|192350001|**Contact**|
|192350002|**User**|
|192350003|**Equipment**|
|192350004|**Facility**|

### <a name="BKMK_msdyn_Priority"></a> msdyn_Priority

|Property|Value|
|---|---|
|Description|**Priority of the requirement. To be taken into consideration while scheduling resources**|
|DisplayName|**Priority**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_priority`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|msdyn_priority|

### <a name="BKMK_msdyn_ProposedDuration"></a> msdyn_ProposedDuration

|Property|Value|
|---|---|
|Description||
|DisplayName|**Proposed Duration**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_proposedduration`|
|RequiredLevel|None|
|Type|Integer|
|MaxValue|2147483647|
|MinValue|0|

### <a name="BKMK_msdyn_RemainingDuration"></a> msdyn_RemainingDuration

|Property|Value|
|---|---|
|Description||
|DisplayName|**Remaining Duration**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_remainingduration`|
|RequiredLevel|None|
|Type|Integer|
|MaxValue|2147483647|
|MinValue|0|

### <a name="BKMK_msdyn_requirementgroupcontrolviewid"></a> msdyn_requirementgroupcontrolviewid

|Property|Value|
|---|---|
|Description|**The requirement group control view id of the resource requirement entity. This field will has value only when the entity is inside the requirement group control.**|
|DisplayName|**Requirement Group Control View Id**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_requirementgroupcontrolviewid`|
|RequiredLevel|None|
|Type|String|
|Format|Text|
|FormatName|Text|
|ImeMode|Auto|
|IsLocalizable|False|
|MaxLength|1000|

### <a name="BKMK_msdyn_requirementgroupid"></a> msdyn_requirementgroupid

|Property|Value|
|---|---|
|Description|**Requirement Group**|
|DisplayName|**Requirement Group**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_requirementgroupid`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|msdyn_requirementgroup|

### <a name="BKMK_msdyn_requirementrelationshipid"></a> msdyn_requirementrelationshipid

|Property|Value|
|---|---|
|Description|**Requirement Relationship**|
|DisplayName|**Requirement Relationship**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_requirementrelationshipid`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|msdyn_requirementrelationship|

### <a name="BKMK_msdyn_resourcerequirementId"></a> msdyn_resourcerequirementId

|Property|Value|
|---|---|
|Description|**Unique identifier for entity instances**|
|DisplayName|**Resource Requirement**|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|`msdyn_resourcerequirementid`|
|RequiredLevel|SystemRequired|
|Type|Uniqueidentifier|

### <a name="BKMK_msdyn_resourcetype"></a> msdyn_resourcetype

|Property|Value|
|---|---|
|Description||
|DisplayName|**Resource Type**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_resourcetype`|
|RequiredLevel|None|
|Type|MultiSelectPicklist|
|DefaultFormValue||
|GlobalChoiceName|`msdyn_bookableresourcetype`|

#### msdyn_resourcetype Choices/Options

|Value|Label|
|---|---|
|1|**Generic**|
|2|**Contact**|
|3|**User**|
|4|**Equipment**|
|5|**Account**|
|6|**Crew**|
|7|**Facility**|
|8|**Pool**|

### <a name="BKMK_msdyn_serviceappointment"></a> msdyn_serviceappointment

|Property|Value|
|---|---|
|Description|**Unique identifier for Service Appointment associated with Resource Requirement.**|
|DisplayName|**Service Activity**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_serviceappointment`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|serviceappointment|

### <a name="BKMK_msdyn_sortoptions"></a> msdyn_sortoptions

|Property|Value|
|---|---|
|Description|**Sort option string field of resource requirement**|
|DisplayName|**Sort Options**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_sortoptions`|
|RequiredLevel|None|
|Type|String|
|Format|Text|
|FormatName|Text|
|ImeMode|Auto|
|IsLocalizable|False|
|MaxLength|1000|

### <a name="BKMK_msdyn_Status"></a> msdyn_Status

|Property|Value|
|---|---|
|Description|**Requirement Status**|
|DisplayName|**Status**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_status`|
|RequiredLevel|ApplicationRequired|
|Type|Lookup|
|Targets|msdyn_requirementstatus|

### <a name="BKMK_msdyn_templaterequirementid"></a> msdyn_templaterequirementid

|Property|Value|
|---|---|
|Description|**template requirement id if requirement is created from template**|
|DisplayName|**Template Requirement Id**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_templaterequirementid`|
|RequiredLevel|None|
|Type|String|
|Format|Text|
|FormatName|Text|
|ImeMode|Auto|
|IsLocalizable|False|
|MaxLength|100|

### <a name="BKMK_msdyn_Territory"></a> msdyn_Territory

|Property|Value|
|---|---|
|Description||
|DisplayName|**Territory**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_territory`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|territory|

### <a name="BKMK_msdyn_TimeFromPromised"></a> msdyn_TimeFromPromised

|Property|Value|
|---|---|
|Description|**Enter the starting range of the time promised to the account that incidents will be resolved.**|
|DisplayName|**Time From Promised**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_timefrompromised`|
|RequiredLevel|None|
|Type|DateTime|
|CanChangeDateTimeBehavior|False|
|DateTimeBehavior|UserLocal|
|Format|DateAndTime|
|ImeMode|Inactive|
|SourceTypeMask|0|

### <a name="BKMK_msdyn_TimeGroup"></a> msdyn_TimeGroup

|Property|Value|
|---|---|
|Description||
|DisplayName|**Fulfillment Preference**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_timegroup`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|msdyn_timegroup|

### <a name="BKMK_msdyn_TimeToPromised"></a> msdyn_TimeToPromised

|Property|Value|
|---|---|
|Description|**Enter the ending range of the time promised to the account that incidents will be resolved.**|
|DisplayName|**Time To Promised**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_timetopromised`|
|RequiredLevel|None|
|Type|DateTime|
|CanChangeDateTimeBehavior|False|
|DateTimeBehavior|UserLocal|
|Format|DateAndTime|
|ImeMode|Inactive|
|SourceTypeMask|0|

### <a name="BKMK_msdyn_TimeWindowEnd"></a> msdyn_TimeWindowEnd

|Property|Value|
|---|---|
|Description|**The time by which the Booking needs to be completed.**|
|DisplayName|**Time Window End**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_timewindowend`|
|RequiredLevel|None|
|Type|DateTime|
|CanChangeDateTimeBehavior|False|
|DateTimeBehavior|UserLocal|
|Format|DateAndTime|
|ImeMode|Inactive|
|SourceTypeMask|0|

### <a name="BKMK_msdyn_TimeWindowStart"></a> msdyn_TimeWindowStart

|Property|Value|
|---|---|
|Description|**The time by which the Booking needs to be started.**|
|DisplayName|**Time Window Start**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_timewindowstart`|
|RequiredLevel|None|
|Type|DateTime|
|CanChangeDateTimeBehavior|False|
|DateTimeBehavior|UserLocal|
|Format|DateAndTime|
|ImeMode|Inactive|
|SourceTypeMask|0|

### <a name="BKMK_msdyn_timezonefortimewindow"></a> msdyn_timezonefortimewindow

|Property|Value|
|---|---|
|Description|**The Timezone in which the Time windows are defined by the User**|
|DisplayName|**Timezone for time window**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_timezonefortimewindow`|
|RequiredLevel|None|
|Type|Integer|
|MaxValue|2147483647|
|MinValue|-2147483648|

### <a name="BKMK_msdyn_todate"></a> msdyn_todate

|Property|Value|
|---|---|
|Description|**End date of requirement period**|
|DisplayName|**To Date**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_todate`|
|RequiredLevel|Recommended|
|Type|DateTime|
|CanChangeDateTimeBehavior|False|
|DateTimeBehavior|UserLocal|
|Format|DateOnly|
|ImeMode|Auto|
|SourceTypeMask|0|

### <a name="BKMK_msdyn_TzaFromDate"></a> msdyn_TzaFromDate

|Property|Value|
|---|---|
|Description|**From date of the resource requirement in time zone independent format**|
|DisplayName|**From Date Time Zone Independent**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_tzafromdate`|
|RequiredLevel|None|
|Type|DateTime|
|CanChangeDateTimeBehavior|False|
|DateTimeBehavior|TimeZoneIndependent|
|Format|DateOnly|
|ImeMode|Inactive|
|SourceTypeMask|0|

### <a name="BKMK_msdyn_TzaToDate"></a> msdyn_TzaToDate

|Property|Value|
|---|---|
|Description|**To date of the resource requirement in time zone independent format**|
|DisplayName|**To Date Time Zone Independent**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_tzatodate`|
|RequiredLevel|None|
|Type|DateTime|
|CanChangeDateTimeBehavior|False|
|DateTimeBehavior|TimeZoneIndependent|
|Format|DateOnly|
|ImeMode|Inactive|
|SourceTypeMask|0|

### <a name="BKMK_msdyn_workhourtemplate"></a> msdyn_workhourtemplate

|Property|Value|
|---|---|
|Description|**The working hours for a requirement.**|
|DisplayName|**Work Hour Template**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_workhourtemplate`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|msdyn_workhourtemplate|

### <a name="BKMK_msdyn_WorkLocation"></a> msdyn_WorkLocation

|Property|Value|
|---|---|
|Description||
|DisplayName|**Work Location**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_worklocation`|
|RequiredLevel|None|
|Type|Picklist|
|DefaultFormValue|690970000|
|GlobalChoiceName|`msdyn_worklocation`|

#### msdyn_WorkLocation Choices/Options

|Value|Label|
|---|---|
|690970000|**Onsite**|
|690970001|**Facility**|
|690970002|**Location Agnostic**|

### <a name="BKMK_OverriddenCreatedOn"></a> OverriddenCreatedOn

|Property|Value|
|---|---|
|Description|**Date and time that the record was migrated.**|
|DisplayName|**Record Created On**|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|`overriddencreatedon`|
|RequiredLevel|None|
|Type|DateTime|
|CanChangeDateTimeBehavior|False|
|DateTimeBehavior|UserLocal|
|Format|DateOnly|
|ImeMode|Inactive|
|SourceTypeMask|0|

### <a name="BKMK_OwnerId"></a> OwnerId

|Property|Value|
|---|---|
|Description|**Owner Id**|
|DisplayName|**Owner**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`ownerid`|
|RequiredLevel|SystemRequired|
|Type|Owner|
|Targets|systemuser, team|

### <a name="BKMK_OwnerIdType"></a> OwnerIdType

|Property|Value|
|---|---|
|Description|**Owner Id Type**|
|DisplayName||
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|`owneridtype`|
|RequiredLevel|SystemRequired|
|Type|EntityName|

### <a name="BKMK_statecode"></a> statecode

|Property|Value|
|---|---|
|Description|**Status of the Resource Requirement**|
|DisplayName|**Status**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`statecode`|
|RequiredLevel|SystemRequired|
|Type|State|
|DefaultFormValue||
|GlobalChoiceName|`msdyn_resourcerequirement_statecode`|

#### statecode Choices/Options

|Value|Details|
|---|---|
|0|Label: **Active**<br />DefaultStatus: 1<br />InvariantName: `Active`|
|1|Label: **Inactive**<br />DefaultStatus: 2<br />InvariantName: `Inactive`|

### <a name="BKMK_statuscode"></a> statuscode

|Property|Value|
|---|---|
|Description|**Reason for the status of the Resource Requirement**|
|DisplayName|**Status Reason**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`statuscode`|
|RequiredLevel|None|
|Type|Status|
|DefaultFormValue||
|GlobalChoiceName|`msdyn_resourcerequirement_statuscode`|

#### statuscode Choices/Options

|Value|Details|
|---|---|
|1|Label: **Active**<br />State:0<br />TransitionData: None|
|2|Label: **Inactive**<br />State:1<br />TransitionData: None|

### <a name="BKMK_TimeZoneRuleVersionNumber"></a> TimeZoneRuleVersionNumber

|Property|Value|
|---|---|
|Description|**For internal use only.**|
|DisplayName|**Time Zone Rule Version Number**|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|`timezoneruleversionnumber`|
|RequiredLevel|None|
|Type|Integer|
|MaxValue|2147483647|
|MinValue|-1|

### <a name="BKMK_UTCConversionTimeZoneCode"></a> UTCConversionTimeZoneCode

|Property|Value|
|---|---|
|Description|**Time zone code that was in use when the record was created.**|
|DisplayName|**UTC Conversion Time Zone Code**|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|`utcconversiontimezonecode`|
|RequiredLevel|None|
|Type|Integer|
|MaxValue|2147483647|
|MinValue|-1|


## Read-only columns/attributes

These columns/attributes return false for both **IsValidForCreate** and **IsValidForUpdate**. Listed by **SchemaName**.

- [CreatedBy](#BKMK_CreatedBy)
- [CreatedOn](#BKMK_CreatedOn)
- [CreatedOnBehalfBy](#BKMK_CreatedOnBehalfBy)
- [ModifiedBy](#BKMK_ModifiedBy)
- [ModifiedOn](#BKMK_ModifiedOn)
- [ModifiedOnBehalfBy](#BKMK_ModifiedOnBehalfBy)
- [OwnerIdName](#BKMK_OwnerIdName)
- [OwnerIdYomiName](#BKMK_OwnerIdYomiName)
- [OwningBusinessUnit](#BKMK_OwningBusinessUnit)
- [OwningTeam](#BKMK_OwningTeam)
- [OwningUser](#BKMK_OwningUser)
- [VersionNumber](#BKMK_VersionNumber)

### <a name="BKMK_CreatedBy"></a> CreatedBy

|Property|Value|
|---|---|
|Description|**Unique identifier of the user who created the record.**|
|DisplayName|**Created By**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`createdby`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|systemuser|

### <a name="BKMK_CreatedOn"></a> CreatedOn

|Property|Value|
|---|---|
|Description|**Date and time when the record was created.**|
|DisplayName|**Created On**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`createdon`|
|RequiredLevel|None|
|Type|DateTime|
|CanChangeDateTimeBehavior|False|
|DateTimeBehavior|UserLocal|
|Format|DateAndTime|
|ImeMode|Inactive|
|SourceTypeMask|0|

### <a name="BKMK_CreatedOnBehalfBy"></a> CreatedOnBehalfBy

|Property|Value|
|---|---|
|Description|**Unique identifier of the delegate user who created the record.**|
|DisplayName|**Created By (Delegate)**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`createdonbehalfby`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|systemuser|

### <a name="BKMK_ModifiedBy"></a> ModifiedBy

|Property|Value|
|---|---|
|Description|**Unique identifier of the user who modified the record.**|
|DisplayName|**Modified By**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`modifiedby`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|systemuser|

### <a name="BKMK_ModifiedOn"></a> ModifiedOn

|Property|Value|
|---|---|
|Description|**Date and time when the record was modified.**|
|DisplayName|**Modified On**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`modifiedon`|
|RequiredLevel|None|
|Type|DateTime|
|CanChangeDateTimeBehavior|False|
|DateTimeBehavior|UserLocal|
|Format|DateAndTime|
|ImeMode|Inactive|
|SourceTypeMask|0|

### <a name="BKMK_ModifiedOnBehalfBy"></a> ModifiedOnBehalfBy

|Property|Value|
|---|---|
|Description|**Unique identifier of the delegate user who modified the record.**|
|DisplayName|**Modified By (Delegate)**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`modifiedonbehalfby`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|systemuser|

### <a name="BKMK_OwnerIdName"></a> OwnerIdName

|Property|Value|
|---|---|
|Description|**Name of the owner**|
|DisplayName||
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|`owneridname`|
|RequiredLevel|SystemRequired|
|Type|String|
|Format|Text|
|FormatName|Text|
|ImeMode|Auto|
|IsLocalizable|False|
|MaxLength|100|

### <a name="BKMK_OwnerIdYomiName"></a> OwnerIdYomiName

|Property|Value|
|---|---|
|Description|**Yomi name of the owner**|
|DisplayName||
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|`owneridyominame`|
|RequiredLevel|SystemRequired|
|Type|String|
|Format|Text|
|FormatName|Text|
|ImeMode|Auto|
|IsLocalizable|False|
|MaxLength|100|

### <a name="BKMK_OwningBusinessUnit"></a> OwningBusinessUnit

|Property|Value|
|---|---|
|Description|**Unique identifier for the business unit that owns the record**|
|DisplayName|**Owning Business Unit**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`owningbusinessunit`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|businessunit|

### <a name="BKMK_OwningTeam"></a> OwningTeam

|Property|Value|
|---|---|
|Description|**Unique identifier for the team that owns the record.**|
|DisplayName|**Owning Team**|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|`owningteam`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|team|

### <a name="BKMK_OwningUser"></a> OwningUser

|Property|Value|
|---|---|
|Description|**Unique identifier for the user that owns the record.**|
|DisplayName|**Owning User**|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|`owninguser`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|systemuser|

### <a name="BKMK_VersionNumber"></a> VersionNumber

|Property|Value|
|---|---|
|Description|**Version Number**|
|DisplayName|**Version Number**|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|`versionnumber`|
|RequiredLevel|None|
|Type|BigInt|
|MaxValue|9223372036854775807|
|MinValue|-9223372036854775808|

## Many-to-One relationships

These relationships are many-to-one. Listed by **SchemaName**.

- [business_unit_msdyn_resourcerequirement](#BKMK_business_unit_msdyn_resourcerequirement)
- [lk_msdyn_resourcerequirement_createdby](#BKMK_lk_msdyn_resourcerequirement_createdby)
- [lk_msdyn_resourcerequirement_createdonbehalfby](#BKMK_lk_msdyn_resourcerequirement_createdonbehalfby)
- [lk_msdyn_resourcerequirement_modifiedby](#BKMK_lk_msdyn_resourcerequirement_modifiedby)
- [lk_msdyn_resourcerequirement_modifiedonbehalfby](#BKMK_lk_msdyn_resourcerequirement_modifiedonbehalfby)
- [msdyn_appointment_msdyn_resourcerequirement](#BKMK_msdyn_appointment_msdyn_resourcerequirement)
- [msdyn_msdyn_bookingsetupmetadata_msdyn_resourcerequirement](#BKMK_msdyn_msdyn_bookingsetupmetadata_msdyn_resourcerequirement)
- [msdyn_msdyn_priority_msdyn_resourcerequirement_Priority](#BKMK_msdyn_msdyn_priority_msdyn_resourcerequirement_Priority)
- [msdyn_msdyn_timegroup_msdyn_resourcerequirement_TimeGroup](#BKMK_msdyn_msdyn_timegroup_msdyn_resourcerequirement_TimeGroup)
- [msdyn_requirementgroup_resourcerequirement_requirementgroupid](#BKMK_msdyn_requirementgroup_resourcerequirement_requirementgroupid)
- [msdyn_requirementrelationship_resourcerequirement_requirementrelationshipid](#BKMK_msdyn_requirementrelationship_resourcerequirement_requirementrelationshipid)
- [msdyn_requirementstatus_resourcerequirement_status](#BKMK_msdyn_requirementstatus_resourcerequirement_status)
- [msdyn_serviceappointment_msdyn_resourcerequirement_serviceappointment](#BKMK_msdyn_serviceappointment_msdyn_resourcerequirement_serviceappointment)
- [msdyn_territory_msdyn_resourcerequirement_Territory](#BKMK_msdyn_territory_msdyn_resourcerequirement_Territory)
- [msdyn_workhourtemplate_msdyn_resourcerequirement_workhourtemplate](#BKMK_msdyn_workhourtemplate_msdyn_resourcerequirement_workhourtemplate)
- [owner_msdyn_resourcerequirement](#BKMK_owner_msdyn_resourcerequirement)
- [team_msdyn_resourcerequirement](#BKMK_team_msdyn_resourcerequirement)
- [user_msdyn_resourcerequirement](#BKMK_user_msdyn_resourcerequirement)

### <a name="BKMK_business_unit_msdyn_resourcerequirement"></a> business_unit_msdyn_resourcerequirement

One-To-Many Relationship: [businessunit business_unit_msdyn_resourcerequirement](businessunit.md#BKMK_business_unit_msdyn_resourcerequirement)

|Property|Value|
|---|---|
|ReferencedEntity|`businessunit`|
|ReferencedAttribute|`businessunitid`|
|ReferencingAttribute|`owningbusinessunit`|
|ReferencingEntityNavigationPropertyName|`owningbusinessunit`|
|IsHierarchical||
|CascadeConfiguration|Archive: `Restrict`<br />Assign: `NoCascade`<br />Delete: `Restrict`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_lk_msdyn_resourcerequirement_createdby"></a> lk_msdyn_resourcerequirement_createdby

One-To-Many Relationship: [systemuser lk_msdyn_resourcerequirement_createdby](systemuser.md#BKMK_lk_msdyn_resourcerequirement_createdby)

|Property|Value|
|---|---|
|ReferencedEntity|`systemuser`|
|ReferencedAttribute|`systemuserid`|
|ReferencingAttribute|`createdby`|
|ReferencingEntityNavigationPropertyName|`createdby`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `NoCascade`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_lk_msdyn_resourcerequirement_createdonbehalfby"></a> lk_msdyn_resourcerequirement_createdonbehalfby

One-To-Many Relationship: [systemuser lk_msdyn_resourcerequirement_createdonbehalfby](systemuser.md#BKMK_lk_msdyn_resourcerequirement_createdonbehalfby)

|Property|Value|
|---|---|
|ReferencedEntity|`systemuser`|
|ReferencedAttribute|`systemuserid`|
|ReferencingAttribute|`createdonbehalfby`|
|ReferencingEntityNavigationPropertyName|`createdonbehalfby`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `NoCascade`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_lk_msdyn_resourcerequirement_modifiedby"></a> lk_msdyn_resourcerequirement_modifiedby

One-To-Many Relationship: [systemuser lk_msdyn_resourcerequirement_modifiedby](systemuser.md#BKMK_lk_msdyn_resourcerequirement_modifiedby)

|Property|Value|
|---|---|
|ReferencedEntity|`systemuser`|
|ReferencedAttribute|`systemuserid`|
|ReferencingAttribute|`modifiedby`|
|ReferencingEntityNavigationPropertyName|`modifiedby`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `NoCascade`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_lk_msdyn_resourcerequirement_modifiedonbehalfby"></a> lk_msdyn_resourcerequirement_modifiedonbehalfby

One-To-Many Relationship: [systemuser lk_msdyn_resourcerequirement_modifiedonbehalfby](systemuser.md#BKMK_lk_msdyn_resourcerequirement_modifiedonbehalfby)

|Property|Value|
|---|---|
|ReferencedEntity|`systemuser`|
|ReferencedAttribute|`systemuserid`|
|ReferencingAttribute|`modifiedonbehalfby`|
|ReferencingEntityNavigationPropertyName|`modifiedonbehalfby`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `NoCascade`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_msdyn_appointment_msdyn_resourcerequirement"></a> msdyn_appointment_msdyn_resourcerequirement

One-To-Many Relationship: [appointment msdyn_appointment_msdyn_resourcerequirement](appointment.md#BKMK_msdyn_appointment_msdyn_resourcerequirement)

|Property|Value|
|---|---|
|ReferencedEntity|`appointment`|
|ReferencedAttribute|`activityid`|
|ReferencingAttribute|`msdyn_appointmentrequirementid`|
|ReferencingEntityNavigationPropertyName|`msdyn_AppointmentRequirementId`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `RemoveLink`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_msdyn_msdyn_bookingsetupmetadata_msdyn_resourcerequirement"></a> msdyn_msdyn_bookingsetupmetadata_msdyn_resourcerequirement

One-To-Many Relationship: [msdyn_bookingsetupmetadata msdyn_msdyn_bookingsetupmetadata_msdyn_resourcerequirement](msdyn_bookingsetupmetadata.md#BKMK_msdyn_msdyn_bookingsetupmetadata_msdyn_resourcerequirement)

|Property|Value|
|---|---|
|ReferencedEntity|`msdyn_bookingsetupmetadata`|
|ReferencedAttribute|`msdyn_bookingsetupmetadataid`|
|ReferencingAttribute|`msdyn_bookingsetupmetadataid`|
|ReferencingEntityNavigationPropertyName|`msdyn_BookingSetupMetadataId`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `RemoveLink`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_msdyn_msdyn_priority_msdyn_resourcerequirement_Priority"></a> msdyn_msdyn_priority_msdyn_resourcerequirement_Priority

One-To-Many Relationship: [msdyn_priority msdyn_msdyn_priority_msdyn_resourcerequirement_Priority](msdyn_priority.md#BKMK_msdyn_msdyn_priority_msdyn_resourcerequirement_Priority)

|Property|Value|
|---|---|
|ReferencedEntity|`msdyn_priority`|
|ReferencedAttribute|`msdyn_priorityid`|
|ReferencingAttribute|`msdyn_priority`|
|ReferencingEntityNavigationPropertyName|`msdyn_Priority`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `RemoveLink`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_msdyn_msdyn_timegroup_msdyn_resourcerequirement_TimeGroup"></a> msdyn_msdyn_timegroup_msdyn_resourcerequirement_TimeGroup

One-To-Many Relationship: [msdyn_timegroup msdyn_msdyn_timegroup_msdyn_resourcerequirement_TimeGroup](msdyn_timegroup.md#BKMK_msdyn_msdyn_timegroup_msdyn_resourcerequirement_TimeGroup)

|Property|Value|
|---|---|
|ReferencedEntity|`msdyn_timegroup`|
|ReferencedAttribute|`msdyn_timegroupid`|
|ReferencingAttribute|`msdyn_timegroup`|
|ReferencingEntityNavigationPropertyName|`msdyn_TimeGroup`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `RemoveLink`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_msdyn_requirementgroup_resourcerequirement_requirementgroupid"></a> msdyn_requirementgroup_resourcerequirement_requirementgroupid

One-To-Many Relationship: [msdyn_requirementgroup msdyn_requirementgroup_resourcerequirement_requirementgroupid](msdyn_requirementgroup.md#BKMK_msdyn_requirementgroup_resourcerequirement_requirementgroupid)

|Property|Value|
|---|---|
|ReferencedEntity|`msdyn_requirementgroup`|
|ReferencedAttribute|`msdyn_requirementgroupid`|
|ReferencingAttribute|`msdyn_requirementgroupid`|
|ReferencingEntityNavigationPropertyName|`msdyn_requirementgroupid`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `RemoveLink`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_msdyn_requirementrelationship_resourcerequirement_requirementrelationshipid"></a> msdyn_requirementrelationship_resourcerequirement_requirementrelationshipid

One-To-Many Relationship: [msdyn_requirementrelationship msdyn_requirementrelationship_resourcerequirement_requirementrelationshipid](msdyn_requirementrelationship.md#BKMK_msdyn_requirementrelationship_resourcerequirement_requirementrelationshipid)

|Property|Value|
|---|---|
|ReferencedEntity|`msdyn_requirementrelationship`|
|ReferencedAttribute|`msdyn_requirementrelationshipid`|
|ReferencingAttribute|`msdyn_requirementrelationshipid`|
|ReferencingEntityNavigationPropertyName|`msdyn_requirementrelationshipid`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `Cascade`<br />Delete: `Cascade`<br />Merge: `NoCascade`<br />Reparent: `Cascade`<br />RollupView: `NoCascade`<br />Share: `Cascade`<br />Unshare: `Cascade`|

### <a name="BKMK_msdyn_requirementstatus_resourcerequirement_status"></a> msdyn_requirementstatus_resourcerequirement_status

One-To-Many Relationship: [msdyn_requirementstatus msdyn_requirementstatus_resourcerequirement_status](msdyn_requirementstatus.md#BKMK_msdyn_requirementstatus_resourcerequirement_status)

|Property|Value|
|---|---|
|ReferencedEntity|`msdyn_requirementstatus`|
|ReferencedAttribute|`msdyn_requirementstatusid`|
|ReferencingAttribute|`msdyn_status`|
|ReferencingEntityNavigationPropertyName|`msdyn_Status`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `RemoveLink`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_msdyn_serviceappointment_msdyn_resourcerequirement_serviceappointment"></a> msdyn_serviceappointment_msdyn_resourcerequirement_serviceappointment

One-To-Many Relationship: [serviceappointment msdyn_serviceappointment_msdyn_resourcerequirement_serviceappointment](serviceappointment.md#BKMK_msdyn_serviceappointment_msdyn_resourcerequirement_serviceappointment)

|Property|Value|
|---|---|
|ReferencedEntity|`serviceappointment`|
|ReferencedAttribute|`activityid`|
|ReferencingAttribute|`msdyn_serviceappointment`|
|ReferencingEntityNavigationPropertyName|`msdyn_serviceappointment`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `RemoveLink`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_msdyn_territory_msdyn_resourcerequirement_Territory"></a> msdyn_territory_msdyn_resourcerequirement_Territory

One-To-Many Relationship: [territory msdyn_territory_msdyn_resourcerequirement_Territory](territory.md#BKMK_msdyn_territory_msdyn_resourcerequirement_Territory)

|Property|Value|
|---|---|
|ReferencedEntity|`territory`|
|ReferencedAttribute|`territoryid`|
|ReferencingAttribute|`msdyn_territory`|
|ReferencingEntityNavigationPropertyName|`msdyn_Territory`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `RemoveLink`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_msdyn_workhourtemplate_msdyn_resourcerequirement_workhourtemplate"></a> msdyn_workhourtemplate_msdyn_resourcerequirement_workhourtemplate

One-To-Many Relationship: [msdyn_workhourtemplate msdyn_workhourtemplate_msdyn_resourcerequirement_workhourtemplate](msdyn_workhourtemplate.md#BKMK_msdyn_workhourtemplate_msdyn_resourcerequirement_workhourtemplate)

|Property|Value|
|---|---|
|ReferencedEntity|`msdyn_workhourtemplate`|
|ReferencedAttribute|`msdyn_workhourtemplateid`|
|ReferencingAttribute|`msdyn_workhourtemplate`|
|ReferencingEntityNavigationPropertyName|`msdyn_workhourtemplate`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `RemoveLink`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_owner_msdyn_resourcerequirement"></a> owner_msdyn_resourcerequirement

One-To-Many Relationship: [owner owner_msdyn_resourcerequirement](owner.md#BKMK_owner_msdyn_resourcerequirement)

|Property|Value|
|---|---|
|ReferencedEntity|`owner`|
|ReferencedAttribute|`ownerid`|
|ReferencingAttribute|`ownerid`|
|ReferencingEntityNavigationPropertyName|`ownerid`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `NoCascade`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_team_msdyn_resourcerequirement"></a> team_msdyn_resourcerequirement

One-To-Many Relationship: [team team_msdyn_resourcerequirement](team.md#BKMK_team_msdyn_resourcerequirement)

|Property|Value|
|---|---|
|ReferencedEntity|`team`|
|ReferencedAttribute|`teamid`|
|ReferencingAttribute|`owningteam`|
|ReferencingEntityNavigationPropertyName|`owningteam`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `NoCascade`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_user_msdyn_resourcerequirement"></a> user_msdyn_resourcerequirement

One-To-Many Relationship: [systemuser user_msdyn_resourcerequirement](systemuser.md#BKMK_user_msdyn_resourcerequirement)

|Property|Value|
|---|---|
|ReferencedEntity|`systemuser`|
|ReferencedAttribute|`systemuserid`|
|ReferencingAttribute|`owninguser`|
|ReferencingEntityNavigationPropertyName|`owninguser`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `NoCascade`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|


## One-to-Many relationships

These relationships are one-to-many. Listed by **SchemaName**.

- [msdyn_resourcerequirement_Annotations](#BKMK_msdyn_resourcerequirement_Annotations)
- [msdyn_resourcerequirement_AsyncOperations](#BKMK_msdyn_resourcerequirement_AsyncOperations)
- [msdyn_resourcerequirement_bookableresourcebooking_ResourceRequirement](#BKMK_msdyn_resourcerequirement_bookableresourcebooking_ResourceRequirement)
- [msdyn_resourcerequirement_bookableresourcebookingheader_ResourceRequirement](#BKMK_msdyn_resourcerequirement_bookableresourcebookingheader_ResourceRequirement)
- [msdyn_resourcerequirement_BulkDeleteFailures](#BKMK_msdyn_resourcerequirement_BulkDeleteFailures)
- [msdyn_resourcerequirement_details](#BKMK_msdyn_resourcerequirement_details)
- [msdyn_resourcerequirement_DuplicateBaseRecord](#BKMK_msdyn_resourcerequirement_DuplicateBaseRecord)
- [msdyn_resourcerequirement_DuplicateMatchingRecord](#BKMK_msdyn_resourcerequirement_DuplicateMatchingRecord)
- [msdyn_resourcerequirement_MailboxTrackingFolders](#BKMK_msdyn_resourcerequirement_MailboxTrackingFolders)
- [msdyn_resourcerequirement_PrincipalObjectAttributeAccesses](#BKMK_msdyn_resourcerequirement_PrincipalObjectAttributeAccesses)
- [msdyn_resourcerequirement_ProcessSession](#BKMK_msdyn_resourcerequirement_ProcessSession)
- [msdyn_resourcerequirement_requirementcharacteristic_resourcerequirement](#BKMK_msdyn_resourcerequirement_requirementcharacteristic_resourcerequirement)
- [msdyn_resourcerequirement_requirementdependency_dependentrequirement](#BKMK_msdyn_resourcerequirement_requirementdependency_dependentrequirement)
- [msdyn_resourcerequirement_requirementdependency_resourcerequirement](#BKMK_msdyn_resourcerequirement_requirementdependency_resourcerequirement)
- [msdyn_resourcerequirement_requirementorganizationunit_ResourceRequirement](#BKMK_msdyn_resourcerequirement_requirementorganizationunit_ResourceRequirement)
- [msdyn_resourcerequirement_requirementresourcecategory_resourcerequirement](#BKMK_msdyn_resourcerequirement_requirementresourcecategory_resourcerequirement)
- [msdyn_resourcerequirement_requirementresourcepreference_ResourceRequirement](#BKMK_msdyn_resourcerequirement_requirementresourcepreference_ResourceRequirement)
- [msdyn_resourcerequirement_SyncErrors](#BKMK_msdyn_resourcerequirement_SyncErrors)

### <a name="BKMK_msdyn_resourcerequirement_Annotations"></a> msdyn_resourcerequirement_Annotations

Many-To-One Relationship: [annotation msdyn_resourcerequirement_Annotations](annotation.md#BKMK_msdyn_resourcerequirement_Annotations)

|Property|Value|
|---|---|
|ReferencingEntity|`annotation`|
|ReferencingAttribute|`objectid`|
|ReferencedEntityNavigationPropertyName|`msdyn_resourcerequirement_Annotations`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `DoNotDisplay`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: <br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_resourcerequirement_AsyncOperations"></a> msdyn_resourcerequirement_AsyncOperations

Many-To-One Relationship: [asyncoperation msdyn_resourcerequirement_AsyncOperations](asyncoperation.md#BKMK_msdyn_resourcerequirement_AsyncOperations)

|Property|Value|
|---|---|
|ReferencingEntity|`asyncoperation`|
|ReferencingAttribute|`regardingobjectid`|
|ReferencedEntityNavigationPropertyName|`msdyn_resourcerequirement_AsyncOperations`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `DoNotDisplay`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: <br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_resourcerequirement_bookableresourcebooking_ResourceRequirement"></a> msdyn_resourcerequirement_bookableresourcebooking_ResourceRequirement

Many-To-One Relationship: [bookableresourcebooking msdyn_resourcerequirement_bookableresourcebooking_ResourceRequirement](bookableresourcebooking.md#BKMK_msdyn_resourcerequirement_bookableresourcebooking_ResourceRequirement)

|Property|Value|
|---|---|
|ReferencingEntity|`bookableresourcebooking`|
|ReferencingAttribute|`msdyn_resourcerequirement`|
|ReferencedEntityNavigationPropertyName|`msdyn_resourcerequirement_bookableresourcebooking_ResourceRequirement`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `UseCollectionName`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: 10000<br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_resourcerequirement_bookableresourcebookingheader_ResourceRequirement"></a> msdyn_resourcerequirement_bookableresourcebookingheader_ResourceRequirement

Many-To-One Relationship: [bookableresourcebookingheader msdyn_resourcerequirement_bookableresourcebookingheader_ResourceRequirement](bookableresourcebookingheader.md#BKMK_msdyn_resourcerequirement_bookableresourcebookingheader_ResourceRequirement)

|Property|Value|
|---|---|
|ReferencingEntity|`bookableresourcebookingheader`|
|ReferencingAttribute|`msdyn_resourcerequirement`|
|ReferencedEntityNavigationPropertyName|`msdyn_resourcerequirement_bookableresourcebookingheader_ResourceRequirement`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `UseCollectionName`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: 10000<br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_resourcerequirement_BulkDeleteFailures"></a> msdyn_resourcerequirement_BulkDeleteFailures

Many-To-One Relationship: [bulkdeletefailure msdyn_resourcerequirement_BulkDeleteFailures](bulkdeletefailure.md#BKMK_msdyn_resourcerequirement_BulkDeleteFailures)

|Property|Value|
|---|---|
|ReferencingEntity|`bulkdeletefailure`|
|ReferencingAttribute|`regardingobjectid`|
|ReferencedEntityNavigationPropertyName|`msdyn_resourcerequirement_BulkDeleteFailures`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `DoNotDisplay`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: <br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_resourcerequirement_details"></a> msdyn_resourcerequirement_details

Many-To-One Relationship: [msdyn_resourcerequirementdetail msdyn_resourcerequirement_details](msdyn_resourcerequirementdetail.md#BKMK_msdyn_resourcerequirement_details)

|Property|Value|
|---|---|
|ReferencingEntity|`msdyn_resourcerequirementdetail`|
|ReferencingAttribute|`msdyn_resourcerequirementid`|
|ReferencedEntityNavigationPropertyName|`msdyn_resourcerequirement_details`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `UseLabel`<br />Group: `Details`<br />Label: Requirement Details<br />MenuId: null<br />Order: 10000<br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_resourcerequirement_DuplicateBaseRecord"></a> msdyn_resourcerequirement_DuplicateBaseRecord

Many-To-One Relationship: [duplicaterecord msdyn_resourcerequirement_DuplicateBaseRecord](duplicaterecord.md#BKMK_msdyn_resourcerequirement_DuplicateBaseRecord)

|Property|Value|
|---|---|
|ReferencingEntity|`duplicaterecord`|
|ReferencingAttribute|`baserecordid`|
|ReferencedEntityNavigationPropertyName|`msdyn_resourcerequirement_DuplicateBaseRecord`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `DoNotDisplay`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: <br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_resourcerequirement_DuplicateMatchingRecord"></a> msdyn_resourcerequirement_DuplicateMatchingRecord

Many-To-One Relationship: [duplicaterecord msdyn_resourcerequirement_DuplicateMatchingRecord](duplicaterecord.md#BKMK_msdyn_resourcerequirement_DuplicateMatchingRecord)

|Property|Value|
|---|---|
|ReferencingEntity|`duplicaterecord`|
|ReferencingAttribute|`duplicaterecordid`|
|ReferencedEntityNavigationPropertyName|`msdyn_resourcerequirement_DuplicateMatchingRecord`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `DoNotDisplay`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: <br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_resourcerequirement_MailboxTrackingFolders"></a> msdyn_resourcerequirement_MailboxTrackingFolders

Many-To-One Relationship: [mailboxtrackingfolder msdyn_resourcerequirement_MailboxTrackingFolders](mailboxtrackingfolder.md#BKMK_msdyn_resourcerequirement_MailboxTrackingFolders)

|Property|Value|
|---|---|
|ReferencingEntity|`mailboxtrackingfolder`|
|ReferencingAttribute|`regardingobjectid`|
|ReferencedEntityNavigationPropertyName|`msdyn_resourcerequirement_MailboxTrackingFolders`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `DoNotDisplay`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: <br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_resourcerequirement_PrincipalObjectAttributeAccesses"></a> msdyn_resourcerequirement_PrincipalObjectAttributeAccesses

Many-To-One Relationship: [principalobjectattributeaccess msdyn_resourcerequirement_PrincipalObjectAttributeAccesses](principalobjectattributeaccess.md#BKMK_msdyn_resourcerequirement_PrincipalObjectAttributeAccesses)

|Property|Value|
|---|---|
|ReferencingEntity|`principalobjectattributeaccess`|
|ReferencingAttribute|`objectid`|
|ReferencedEntityNavigationPropertyName|`msdyn_resourcerequirement_PrincipalObjectAttributeAccesses`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `DoNotDisplay`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: <br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_resourcerequirement_ProcessSession"></a> msdyn_resourcerequirement_ProcessSession

Many-To-One Relationship: [processsession msdyn_resourcerequirement_ProcessSession](processsession.md#BKMK_msdyn_resourcerequirement_ProcessSession)

|Property|Value|
|---|---|
|ReferencingEntity|`processsession`|
|ReferencingAttribute|`regardingobjectid`|
|ReferencedEntityNavigationPropertyName|`msdyn_resourcerequirement_ProcessSession`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `DoNotDisplay`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: <br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_resourcerequirement_requirementcharacteristic_resourcerequirement"></a> msdyn_resourcerequirement_requirementcharacteristic_resourcerequirement

Many-To-One Relationship: [msdyn_requirementcharacteristic msdyn_resourcerequirement_requirementcharacteristic_resourcerequirement](msdyn_requirementcharacteristic.md#BKMK_msdyn_resourcerequirement_requirementcharacteristic_resourcerequirement)

|Property|Value|
|---|---|
|ReferencingEntity|`msdyn_requirementcharacteristic`|
|ReferencingAttribute|`msdyn_resourcerequirement`|
|ReferencedEntityNavigationPropertyName|`msdyn_resourcerequirement_requirementcharacteristic_resourcerequirement`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `UseLabel`<br />Group: `Details`<br />Label: Characteristics<br />MenuId: null<br />Order: 10000<br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_resourcerequirement_requirementdependency_dependentrequirement"></a> msdyn_resourcerequirement_requirementdependency_dependentrequirement

Many-To-One Relationship: [msdyn_requirementdependency msdyn_resourcerequirement_requirementdependency_dependentrequirement](msdyn_requirementdependency.md#BKMK_msdyn_resourcerequirement_requirementdependency_dependentrequirement)

|Property|Value|
|---|---|
|ReferencingEntity|`msdyn_requirementdependency`|
|ReferencingAttribute|`msdyn_dependentrequirement`|
|ReferencedEntityNavigationPropertyName|`msdyn_resourcerequirement_requirementdependency_dependentrequirement`|
|IsCustomizable|`False`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `UseCollectionName`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: 10000<br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_resourcerequirement_requirementdependency_resourcerequirement"></a> msdyn_resourcerequirement_requirementdependency_resourcerequirement

Many-To-One Relationship: [msdyn_requirementdependency msdyn_resourcerequirement_requirementdependency_resourcerequirement](msdyn_requirementdependency.md#BKMK_msdyn_resourcerequirement_requirementdependency_resourcerequirement)

|Property|Value|
|---|---|
|ReferencingEntity|`msdyn_requirementdependency`|
|ReferencingAttribute|`msdyn_requirement`|
|ReferencedEntityNavigationPropertyName|`msdyn_resourcerequirement_requirementdependency_resourcerequirement`|
|IsCustomizable|`False`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `UseCollectionName`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: 10000<br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_resourcerequirement_requirementorganizationunit_ResourceRequirement"></a> msdyn_resourcerequirement_requirementorganizationunit_ResourceRequirement

Many-To-One Relationship: [msdyn_requirementorganizationunit msdyn_resourcerequirement_requirementorganizationunit_ResourceRequirement](msdyn_requirementorganizationunit.md#BKMK_msdyn_resourcerequirement_requirementorganizationunit_ResourceRequirement)

|Property|Value|
|---|---|
|ReferencingEntity|`msdyn_requirementorganizationunit`|
|ReferencingAttribute|`msdyn_resourcerequirement`|
|ReferencedEntityNavigationPropertyName|`msdyn_resourcerequirement_requirementorganizationunit_ResourceRequirement`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `UseLabel`<br />Group: `Details`<br />Label: Organizational Units<br />MenuId: null<br />Order: 10000<br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_resourcerequirement_requirementresourcecategory_resourcerequirement"></a> msdyn_resourcerequirement_requirementresourcecategory_resourcerequirement

Many-To-One Relationship: [msdyn_requirementresourcecategory msdyn_resourcerequirement_requirementresourcecategory_resourcerequirement](msdyn_requirementresourcecategory.md#BKMK_msdyn_resourcerequirement_requirementresourcecategory_resourcerequirement)

|Property|Value|
|---|---|
|ReferencingEntity|`msdyn_requirementresourcecategory`|
|ReferencingAttribute|`msdyn_resourcerequirement`|
|ReferencedEntityNavigationPropertyName|`msdyn_resourcerequirement_requirementresourcecategory_resourcerequirement`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `UseLabel`<br />Group: `Details`<br />Label: Resource Categories<br />MenuId: null<br />Order: 10000<br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_resourcerequirement_requirementresourcepreference_ResourceRequirement"></a> msdyn_resourcerequirement_requirementresourcepreference_ResourceRequirement

Many-To-One Relationship: [msdyn_requirementresourcepreference msdyn_resourcerequirement_requirementresourcepreference_ResourceRequirement](msdyn_requirementresourcepreference.md#BKMK_msdyn_resourcerequirement_requirementresourcepreference_ResourceRequirement)

|Property|Value|
|---|---|
|ReferencingEntity|`msdyn_requirementresourcepreference`|
|ReferencingAttribute|`msdyn_resourcerequirement`|
|ReferencedEntityNavigationPropertyName|`msdyn_resourcerequirement_requirementresourcepreference_ResourceRequirement`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `UseLabel`<br />Group: `Details`<br />Label: Resource Preferences<br />MenuId: null<br />Order: 10000<br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_resourcerequirement_SyncErrors"></a> msdyn_resourcerequirement_SyncErrors

Many-To-One Relationship: [syncerror msdyn_resourcerequirement_SyncErrors](syncerror.md#BKMK_msdyn_resourcerequirement_SyncErrors)

|Property|Value|
|---|---|
|ReferencingEntity|`syncerror`|
|ReferencingAttribute|`regardingobjectid`|
|ReferencedEntityNavigationPropertyName|`msdyn_resourcerequirement_SyncErrors`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `DoNotDisplay`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: <br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|



### See also

[Dataverse table/entity reference](/power-apps/developer/data-platform/reference/about-entity-reference)  
[Dataverse Web API Reference](/power-apps/developer/data-platform/webapi/reference/about)   

