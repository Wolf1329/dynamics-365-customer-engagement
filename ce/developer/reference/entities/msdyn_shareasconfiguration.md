---
title: "ShareAs Configuration (msdyn_shareasconfiguration) table/entity reference (Microsoft Dynamics 365)"
description: "Includes schema information and supported messages for the ShareAs Configuration (msdyn_shareasconfiguration) table/entity with Microsoft Dynamics 365."
ms.topic: generated-reference
author: JimDaly
ms.author: jdaly
search.audienceType: 
  - developer
---

# ShareAs Configuration (msdyn_shareasconfiguration) table/entity reference (Microsoft Dynamics 365)

ShareAs Configuration

## Messages

The following table lists the messages for the ShareAs Configuration (msdyn_shareasconfiguration) table.
Messages represent operations that can be performed on the table. They may also be events.

| Name <br />Is Event? |Web API Operation |SDK for .NET |
| ---- | ----- |----- |
| `Associate`<br />Event: True |[Associate records](/power-apps/developer/data-platform/webapi/associate-disassociate-entities-using-web-api) |[Associate records](/power-apps/developer/data-platform/org-service/entity-operations-associate-disassociate#use-the-associate-method-or-associaterequest)|
| `BulkRetain`<br />Event: True |<xref:Microsoft.Dynamics.CRM.BulkRetain?displayProperty=nameWithType /> |[Learn to use messages with the SDK for .NET](/power-apps/developer/data-platform/org-service/use-messages)|
| `Create`<br />Event: True |`POST` /msdyn_shareasconfigurations<br />See [Create](/powerapps/developer/data-platform/webapi/create-entity-web-api) |[Create records](/power-apps/developer/data-platform/org-service/entity-operations-create#basic-create)|
| `CreateMultiple`<br />Event: True |<xref:Microsoft.Dynamics.CRM.CreateMultiple?displayProperty=nameWithType /> |<xref:Microsoft.Xrm.Sdk.Messages.CreateMultipleRequest>|
| `Delete`<br />Event: True |`DELETE` /msdyn_shareasconfigurations(*msdyn_shareasconfigurationid*)<br />See [Delete](/powerapps/developer/data-platform/webapi/update-delete-entities-using-web-api#basic-delete) |[Delete records](/power-apps/developer/data-platform/org-service/entity-operations-update-delete#basic-delete)|
| `Disassociate`<br />Event: True |[Disassociate records](/power-apps/developer/data-platform/webapi/associate-disassociate-entities-using-web-api) |[Disassociate records](/power-apps/developer/data-platform/org-service/entity-operations-associate-disassociate#use-the-disassociate-method-or-disassociaterequest)|
| `IsValidStateTransition`<br />Event: False |<xref:Microsoft.Dynamics.CRM.IsValidStateTransition?displayProperty=nameWithType /> |<xref:Microsoft.Crm.Sdk.Messages.IsValidStateTransitionRequest>|
| `PurgeRetainedContent`<br />Event: True |<xref:Microsoft.Dynamics.CRM.PurgeRetainedContent?displayProperty=nameWithType /> |[Learn to use messages with the SDK for .NET](/power-apps/developer/data-platform/org-service/use-messages)|
| `Restore`<br />Event: True |<xref:Microsoft.Dynamics.CRM.Restore?displayProperty=nameWithType /> |[Learn to use messages with the SDK for .NET](/power-apps/developer/data-platform/org-service/use-messages)|
| `Retain`<br />Event: True |<xref:Microsoft.Dynamics.CRM.Retain?displayProperty=nameWithType /> |[Learn to use messages with the SDK for .NET](/power-apps/developer/data-platform/org-service/use-messages)|
| `Retrieve`<br />Event: True |`GET` /msdyn_shareasconfigurations(*msdyn_shareasconfigurationid*)<br />See [Retrieve](/powerapps/developer/data-platform/webapi/retrieve-entity-using-web-api) |[Retrieve records](/power-apps/developer/data-platform/org-service/entity-operations-retrieve)|
| `RetrieveMultiple`<br />Event: True |`GET` /msdyn_shareasconfigurations<br />See [Query data](/power-apps/developer/data-platform/webapi/query-data-web-api) |[Query data](/power-apps/developer/data-platform/org-service/entity-operations-query-data)|
| `RollbackRetain`<br />Event: True |<xref:Microsoft.Dynamics.CRM.RollbackRetain?displayProperty=nameWithType /> |[Learn to use messages with the SDK for .NET](/power-apps/developer/data-platform/org-service/use-messages)|
| `SetState`<br />Event: True |`PATCH` /msdyn_shareasconfigurations(*msdyn_shareasconfigurationid*)<br />[Update](/powerapps/developer/data-platform/webapi/update-delete-entities-using-web-api#basic-update) the `statecode` and `statuscode` properties. |<xref:Microsoft.Crm.Sdk.Messages.SetStateRequest>|
| `Update`<br />Event: True |`PATCH` /msdyn_shareasconfigurations(*msdyn_shareasconfigurationid*)<br />See [Update](/powerapps/developer/data-platform/webapi/update-delete-entities-using-web-api#basic-update) |[Update records](/power-apps/developer/data-platform/org-service/entity-operations-update-delete#basic-update)|
| `UpdateMultiple`<br />Event: True |<xref:Microsoft.Dynamics.CRM.UpdateMultiple?displayProperty=nameWithType /> |<xref:Microsoft.Xrm.Sdk.Messages.UpdateMultipleRequest>|
| `Upsert`<br />Event: False |`PATCH` /msdyn_shareasconfigurations(*msdyn_shareasconfigurationid*)<br />See [Upsert a table row](/powerapps/developer/data-platform/webapi/update-delete-entities-using-web-api#upsert-a-table-row) |<xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest>|
| `UpsertMultiple`<br />Event: False |<xref:Microsoft.Dynamics.CRM.UpsertMultiple?displayProperty=nameWithType /> |<xref:Microsoft.Xrm.Sdk.Messages.UpsertMultipleRequest>|
| `ValidateRetentionConfig`<br />Event: True |<xref:Microsoft.Dynamics.CRM.ValidateRetentionConfig?displayProperty=nameWithType /> |[Learn to use messages with the SDK for .NET](/power-apps/developer/data-platform/org-service/use-messages)|

## Properties

The following table lists selected properties for the ShareAs Configuration (msdyn_shareasconfiguration) table.

|Property|Value|
| --- | --- |
| **DisplayName** | **ShareAs Configuration** |
| **DisplayCollectionName** | **ShareAs Configuration** |
| **SchemaName** | `msdyn_shareasconfiguration` |
| **CollectionSchemaName** | `msdyn_shareasconfigurations` |
| **EntitySetName** | `msdyn_shareasconfigurations`|
| **LogicalName** | `msdyn_shareasconfiguration` |
| **LogicalCollectionName** | `msdyn_shareasconfigurations` |
| **PrimaryIdAttribute** | `msdyn_shareasconfigurationid` |
| **PrimaryNameAttribute** |`msdyn_shareashashid` |
| **TableType** | `Standard` |
| **OwnershipType** | `OrganizationOwned` |

## Writable columns/attributes

These columns/attributes return true for either **IsValidForCreate** or **IsValidForUpdate** (usually both). Listed by **SchemaName**.

- [ImportSequenceNumber](#BKMK_ImportSequenceNumber)
- [msdyn_forecastconfigurationid](#BKMK_msdyn_forecastconfigurationid)
- [msdyn_hierarchyrecordid](#BKMK_msdyn_hierarchyrecordid)
- [msdyn_shareasconfigurationId](#BKMK_msdyn_shareasconfigurationId)
- [msdyn_shareashashid](#BKMK_msdyn_shareashashid)
- [msdyn_sharedbyuserid](#BKMK_msdyn_sharedbyuserid)
- [msdyn_sharedon](#BKMK_msdyn_sharedon)
- [msdyn_sharedwithuserid](#BKMK_msdyn_sharedwithuserid)
- [msdyn_sharelevel](#BKMK_msdyn_sharelevel)
- [OverriddenCreatedOn](#BKMK_OverriddenCreatedOn)
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

### <a name="BKMK_msdyn_forecastconfigurationid"></a> msdyn_forecastconfigurationid

|Property|Value|
|---|---|
|Description||
|DisplayName|**msdyn\_forecastconfigurationid**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_forecastconfigurationid`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|msdyn_forecastconfiguration|

### <a name="BKMK_msdyn_hierarchyrecordid"></a> msdyn_hierarchyrecordid

|Property|Value|
|---|---|
|Description|**Hierarchy Record Id**|
|DisplayName|**Hierarchy Record Id**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_hierarchyrecordid`|
|RequiredLevel|None|
|Type|String|
|Format|Text|
|FormatName|Text|
|ImeMode|Auto|
|IsLocalizable|False|
|MaxLength|36|

### <a name="BKMK_msdyn_shareasconfigurationId"></a> msdyn_shareasconfigurationId

|Property|Value|
|---|---|
|Description|**Unique identifier for entity instances**|
|DisplayName|**ShareAs Configuration**|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|`msdyn_shareasconfigurationid`|
|RequiredLevel|SystemRequired|
|Type|Uniqueidentifier|

### <a name="BKMK_msdyn_shareashashid"></a> msdyn_shareashashid

|Property|Value|
|---|---|
|Description|**Share As Hash Id**|
|DisplayName|**Share As Hash Id**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_shareashashid`|
|RequiredLevel|None|
|Type|String|
|Format|Text|
|FormatName|Text|
|ImeMode|Auto|
|IsLocalizable|False|
|MaxLength|36|

### <a name="BKMK_msdyn_sharedbyuserid"></a> msdyn_sharedbyuserid

|Property|Value|
|---|---|
|Description|**Shared By User Id**|
|DisplayName|**Shared By User Id**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_sharedbyuserid`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|systemuser|

### <a name="BKMK_msdyn_sharedon"></a> msdyn_sharedon

|Property|Value|
|---|---|
|Description|**Date and time when the fc was shared**|
|DisplayName|**Shared On**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_sharedon`|
|RequiredLevel|None|
|Type|DateTime|
|CanChangeDateTimeBehavior|True|
|DateTimeBehavior|TimeZoneIndependent|
|Format|DateAndTime|
|ImeMode|Inactive|
|SourceTypeMask|0|

### <a name="BKMK_msdyn_sharedwithuserid"></a> msdyn_sharedwithuserid

|Property|Value|
|---|---|
|Description|**Shared With User Id**|
|DisplayName|**Shared With User Id**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_sharedwithuserid`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|systemuser|

### <a name="BKMK_msdyn_sharelevel"></a> msdyn_sharelevel

|Property|Value|
|---|---|
|Description|**Share Level**|
|DisplayName|**Share Level**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`msdyn_sharelevel`|
|RequiredLevel|None|
|Type|Picklist|
|DefaultFormValue|0|
|GlobalChoiceName|`msdyn_shareasconfiguration_sharelevel`|

#### msdyn_sharelevel Choices/Options

|Value|Label|
|---|---|
|0|**None**|
|1|**ReadOnly**|
|2|**ReadWrite**|

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

### <a name="BKMK_statecode"></a> statecode

|Property|Value|
|---|---|
|Description|**Status of the ShareAs Configuration**|
|DisplayName|**Status**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`statecode`|
|RequiredLevel|SystemRequired|
|Type|State|
|DefaultFormValue||
|GlobalChoiceName|`msdyn_shareasconfiguration_statecode`|

#### statecode Choices/Options

|Value|Details|
|---|---|
|0|Label: **Active**<br />DefaultStatus: 1<br />InvariantName: `Active`|
|1|Label: **Inactive**<br />DefaultStatus: 2<br />InvariantName: `Inactive`|

### <a name="BKMK_statuscode"></a> statuscode

|Property|Value|
|---|---|
|Description|**Reason for the status of the ShareAs Configuration**|
|DisplayName|**Status Reason**|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|`statuscode`|
|RequiredLevel|None|
|Type|Status|
|DefaultFormValue||
|GlobalChoiceName|`msdyn_shareasconfiguration_statuscode`|

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
- [OrganizationId](#BKMK_OrganizationId)
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

### <a name="BKMK_OrganizationId"></a> OrganizationId

|Property|Value|
|---|---|
|Description|**Unique identifier for the organization**|
|DisplayName|**Organization Id**|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|`organizationid`|
|RequiredLevel|None|
|Type|Lookup|
|Targets|organization|

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

- [lk_msdyn_shareasconfiguration_createdby](#BKMK_lk_msdyn_shareasconfiguration_createdby)
- [lk_msdyn_shareasconfiguration_createdonbehalfby](#BKMK_lk_msdyn_shareasconfiguration_createdonbehalfby)
- [lk_msdyn_shareasconfiguration_modifiedby](#BKMK_lk_msdyn_shareasconfiguration_modifiedby)
- [lk_msdyn_shareasconfiguration_modifiedonbehalfby](#BKMK_lk_msdyn_shareasconfiguration_modifiedonbehalfby)
- [msdyn_msdyn_forecastconfiguration_msdyn_shareasconfiguration_forecastconfigurationid](#BKMK_msdyn_msdyn_forecastconfiguration_msdyn_shareasconfiguration_forecastconfigurationid)
- [msdyn_msdyn_shareasconfiguration_sharedbyuserid](#BKMK_msdyn_msdyn_shareasconfiguration_sharedbyuserid)
- [msdyn_msdyn_shareasconfiguration_sharedwithuserid](#BKMK_msdyn_msdyn_shareasconfiguration_sharedwithuserid)
- [organization_msdyn_shareasconfiguration](#BKMK_organization_msdyn_shareasconfiguration)

### <a name="BKMK_lk_msdyn_shareasconfiguration_createdby"></a> lk_msdyn_shareasconfiguration_createdby

One-To-Many Relationship: [systemuser lk_msdyn_shareasconfiguration_createdby](systemuser.md#BKMK_lk_msdyn_shareasconfiguration_createdby)

|Property|Value|
|---|---|
|ReferencedEntity|`systemuser`|
|ReferencedAttribute|`systemuserid`|
|ReferencingAttribute|`createdby`|
|ReferencingEntityNavigationPropertyName|`createdby`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `NoCascade`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_lk_msdyn_shareasconfiguration_createdonbehalfby"></a> lk_msdyn_shareasconfiguration_createdonbehalfby

One-To-Many Relationship: [systemuser lk_msdyn_shareasconfiguration_createdonbehalfby](systemuser.md#BKMK_lk_msdyn_shareasconfiguration_createdonbehalfby)

|Property|Value|
|---|---|
|ReferencedEntity|`systemuser`|
|ReferencedAttribute|`systemuserid`|
|ReferencingAttribute|`createdonbehalfby`|
|ReferencingEntityNavigationPropertyName|`createdonbehalfby`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `NoCascade`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_lk_msdyn_shareasconfiguration_modifiedby"></a> lk_msdyn_shareasconfiguration_modifiedby

One-To-Many Relationship: [systemuser lk_msdyn_shareasconfiguration_modifiedby](systemuser.md#BKMK_lk_msdyn_shareasconfiguration_modifiedby)

|Property|Value|
|---|---|
|ReferencedEntity|`systemuser`|
|ReferencedAttribute|`systemuserid`|
|ReferencingAttribute|`modifiedby`|
|ReferencingEntityNavigationPropertyName|`modifiedby`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `NoCascade`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_lk_msdyn_shareasconfiguration_modifiedonbehalfby"></a> lk_msdyn_shareasconfiguration_modifiedonbehalfby

One-To-Many Relationship: [systemuser lk_msdyn_shareasconfiguration_modifiedonbehalfby](systemuser.md#BKMK_lk_msdyn_shareasconfiguration_modifiedonbehalfby)

|Property|Value|
|---|---|
|ReferencedEntity|`systemuser`|
|ReferencedAttribute|`systemuserid`|
|ReferencingAttribute|`modifiedonbehalfby`|
|ReferencingEntityNavigationPropertyName|`modifiedonbehalfby`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `NoCascade`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_msdyn_msdyn_forecastconfiguration_msdyn_shareasconfiguration_forecastconfigurationid"></a> msdyn_msdyn_forecastconfiguration_msdyn_shareasconfiguration_forecastconfigurationid

One-To-Many Relationship: [msdyn_forecastconfiguration msdyn_msdyn_forecastconfiguration_msdyn_shareasconfiguration_forecastconfigurationid](msdyn_forecastconfiguration.md#BKMK_msdyn_msdyn_forecastconfiguration_msdyn_shareasconfiguration_forecastconfigurationid)

|Property|Value|
|---|---|
|ReferencedEntity|`msdyn_forecastconfiguration`|
|ReferencedAttribute|`msdyn_forecastconfigurationid`|
|ReferencingAttribute|`msdyn_forecastconfigurationid`|
|ReferencingEntityNavigationPropertyName|`msdyn_forecastconfigurationid`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `Cascade`<br />Delete: `Cascade`<br />Merge: `NoCascade`<br />Reparent: `Cascade`<br />RollupView: `NoCascade`<br />Share: `Cascade`<br />Unshare: `Cascade`|

### <a name="BKMK_msdyn_msdyn_shareasconfiguration_sharedbyuserid"></a> msdyn_msdyn_shareasconfiguration_sharedbyuserid

One-To-Many Relationship: [systemuser msdyn_msdyn_shareasconfiguration_sharedbyuserid](systemuser.md#BKMK_msdyn_msdyn_shareasconfiguration_sharedbyuserid)

|Property|Value|
|---|---|
|ReferencedEntity|`systemuser`|
|ReferencedAttribute|`systemuserid`|
|ReferencingAttribute|`msdyn_sharedbyuserid`|
|ReferencingEntityNavigationPropertyName|`msdyn_sharedbyuserid`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `RemoveLink`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_msdyn_msdyn_shareasconfiguration_sharedwithuserid"></a> msdyn_msdyn_shareasconfiguration_sharedwithuserid

One-To-Many Relationship: [systemuser msdyn_msdyn_shareasconfiguration_sharedwithuserid](systemuser.md#BKMK_msdyn_msdyn_shareasconfiguration_sharedwithuserid)

|Property|Value|
|---|---|
|ReferencedEntity|`systemuser`|
|ReferencedAttribute|`systemuserid`|
|ReferencingAttribute|`msdyn_sharedwithuserid`|
|ReferencingEntityNavigationPropertyName|`msdyn_sharedwithuserid`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `RemoveLink`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|

### <a name="BKMK_organization_msdyn_shareasconfiguration"></a> organization_msdyn_shareasconfiguration

One-To-Many Relationship: [organization organization_msdyn_shareasconfiguration](organization.md#BKMK_organization_msdyn_shareasconfiguration)

|Property|Value|
|---|---|
|ReferencedEntity|`organization`|
|ReferencedAttribute|`organizationid`|
|ReferencingAttribute|`organizationid`|
|ReferencingEntityNavigationPropertyName|`organizationid`|
|IsHierarchical||
|CascadeConfiguration|Archive: `NoCascade`<br />Assign: `NoCascade`<br />Delete: `NoCascade`<br />Merge: `NoCascade`<br />Reparent: `NoCascade`<br />RollupView: `NoCascade`<br />Share: `NoCascade`<br />Unshare: `NoCascade`|


## One-to-Many relationships

These relationships are one-to-many. Listed by **SchemaName**.

- [msdyn_shareasconfiguration_AsyncOperations](#BKMK_msdyn_shareasconfiguration_AsyncOperations)
- [msdyn_shareasconfiguration_BulkDeleteFailures](#BKMK_msdyn_shareasconfiguration_BulkDeleteFailures)
- [msdyn_shareasconfiguration_MailboxTrackingFolders](#BKMK_msdyn_shareasconfiguration_MailboxTrackingFolders)
- [msdyn_shareasconfiguration_PrincipalObjectAttributeAccesses](#BKMK_msdyn_shareasconfiguration_PrincipalObjectAttributeAccesses)
- [msdyn_shareasconfiguration_ProcessSession](#BKMK_msdyn_shareasconfiguration_ProcessSession)
- [msdyn_shareasconfiguration_SyncErrors](#BKMK_msdyn_shareasconfiguration_SyncErrors)

### <a name="BKMK_msdyn_shareasconfiguration_AsyncOperations"></a> msdyn_shareasconfiguration_AsyncOperations

Many-To-One Relationship: [asyncoperation msdyn_shareasconfiguration_AsyncOperations](asyncoperation.md#BKMK_msdyn_shareasconfiguration_AsyncOperations)

|Property|Value|
|---|---|
|ReferencingEntity|`asyncoperation`|
|ReferencingAttribute|`regardingobjectid`|
|ReferencedEntityNavigationPropertyName|`msdyn_shareasconfiguration_AsyncOperations`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `DoNotDisplay`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: <br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_shareasconfiguration_BulkDeleteFailures"></a> msdyn_shareasconfiguration_BulkDeleteFailures

Many-To-One Relationship: [bulkdeletefailure msdyn_shareasconfiguration_BulkDeleteFailures](bulkdeletefailure.md#BKMK_msdyn_shareasconfiguration_BulkDeleteFailures)

|Property|Value|
|---|---|
|ReferencingEntity|`bulkdeletefailure`|
|ReferencingAttribute|`regardingobjectid`|
|ReferencedEntityNavigationPropertyName|`msdyn_shareasconfiguration_BulkDeleteFailures`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `DoNotDisplay`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: <br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_shareasconfiguration_MailboxTrackingFolders"></a> msdyn_shareasconfiguration_MailboxTrackingFolders

Many-To-One Relationship: [mailboxtrackingfolder msdyn_shareasconfiguration_MailboxTrackingFolders](mailboxtrackingfolder.md#BKMK_msdyn_shareasconfiguration_MailboxTrackingFolders)

|Property|Value|
|---|---|
|ReferencingEntity|`mailboxtrackingfolder`|
|ReferencingAttribute|`regardingobjectid`|
|ReferencedEntityNavigationPropertyName|`msdyn_shareasconfiguration_MailboxTrackingFolders`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `DoNotDisplay`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: <br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_shareasconfiguration_PrincipalObjectAttributeAccesses"></a> msdyn_shareasconfiguration_PrincipalObjectAttributeAccesses

Many-To-One Relationship: [principalobjectattributeaccess msdyn_shareasconfiguration_PrincipalObjectAttributeAccesses](principalobjectattributeaccess.md#BKMK_msdyn_shareasconfiguration_PrincipalObjectAttributeAccesses)

|Property|Value|
|---|---|
|ReferencingEntity|`principalobjectattributeaccess`|
|ReferencingAttribute|`objectid`|
|ReferencedEntityNavigationPropertyName|`msdyn_shareasconfiguration_PrincipalObjectAttributeAccesses`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `DoNotDisplay`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: <br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_shareasconfiguration_ProcessSession"></a> msdyn_shareasconfiguration_ProcessSession

Many-To-One Relationship: [processsession msdyn_shareasconfiguration_ProcessSession](processsession.md#BKMK_msdyn_shareasconfiguration_ProcessSession)

|Property|Value|
|---|---|
|ReferencingEntity|`processsession`|
|ReferencingAttribute|`regardingobjectid`|
|ReferencedEntityNavigationPropertyName|`msdyn_shareasconfiguration_ProcessSession`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `DoNotDisplay`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: <br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|

### <a name="BKMK_msdyn_shareasconfiguration_SyncErrors"></a> msdyn_shareasconfiguration_SyncErrors

Many-To-One Relationship: [syncerror msdyn_shareasconfiguration_SyncErrors](syncerror.md#BKMK_msdyn_shareasconfiguration_SyncErrors)

|Property|Value|
|---|---|
|ReferencingEntity|`syncerror`|
|ReferencingAttribute|`regardingobjectid`|
|ReferencedEntityNavigationPropertyName|`msdyn_shareasconfiguration_SyncErrors`|
|IsCustomizable|`True`|
|AssociatedMenuConfiguration|AvailableOffline: True<br />Behavior: `DoNotDisplay`<br />Group: `Details`<br />Label: <br />MenuId: null<br />Order: <br />QueryApi: null<br />ViewId: `00000000-0000-0000-0000-000000000000`|



### See also

[Dataverse table/entity reference](/power-apps/developer/data-platform/reference/about-entity-reference)  
[Dataverse Web API Reference](/power-apps/developer/data-platform/webapi/reference/about)   

