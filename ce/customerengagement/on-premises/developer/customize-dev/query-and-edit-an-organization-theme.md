---
title: "Query and edit an organization theme | MicrosoftDocs"
description: "Learn about defining and applying visual themes for an organization. This provides a supported way to apply an organization's logo and color choices to the application. "
ms.custom: 
ms.reviewer: pehecke

ms.suite: 
ms.tgt_pltfrm: 
ms.topic: how-to
applies_to: 
  - Dynamics 365 Customer Engagement (on-premises)
ms.assetid: b9ad59fa-4778-4f79-9b24-94c320a33bde
caps.latest.revision: 20
author: JimDaly
ms.author: jdaly
search.audienceType: 
  - developer

---
# Query and edit an organization theme

You can define and apply visual themes for an organization. This provides a supported way to apply an organization's logo and color choices to the application. You can create a custom theme for your application by making changes to the default colors and visual elements provided in the un-customized [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] system. For example, you can create your personal product branding, add a company logo and provide entity-specific coloring. The theme colors are applied globally throughout the application, with the exception of some legacy areas.  
  
> [!NOTE]
> [!INCLUDE[cc_feature_included_with_2015_update_1_admins](../../includes/cc-feature-included-with-2015-update-1-admins.md)]  
  
 Theme customization is supported in this release only for the web application. The changes made for an organization's theme are not included in solutions exported from the organization. You can define multiple themes, but only one can be set and published as the default theme.  
  
 Video: [Theming in Microsoft Dynamics 365 Customer Engagement](https://go.microsoft.com/fwlink/p/?LinkId=529568)  
  
<a name="BKMK_QueryTheme"></a>

## Query the current theme
 You may need to query the current theme using client-side code if you have a solution with HTML web resources which you want to adapt to theme choices made for an organization. You can use the following query with the Web API to retrieve that information.  

 **Request:** 

```http
GET [Organization URI]/api/data/v9.1/themes?$filter=isdefaulttheme eq true&$select=defaultentitycolor,defaultcustomentitycolor,controlborder,controlshade,selectedlinkeffect,globallinkcolor,processcontrolcolor,headercolor,logotooltip,hoverlinkeffect,navbarshelfcolor,navbarbackgroundcolor
```

 **Response:**

```json
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0

{  
    "@odata.context": "[Organization URI]/api/data/v9.1/$metadata#themes(defaultentitycolor,defaultcustomentitycolor,controlborder,controlshade,selectedlinkeffect,globallinkcolor,processcontrolcolor,headercolor,logotooltip,hoverlinkeffect,navbarshelfcolor,navbarbackgroundcolor)",  
    "value": [  
        {  
            "defaultentitycolor": "#001CA5",  
            "defaultcustomentitycolor": "#006551",  
            "controlborder": "#CCCCCC",  
            "controlshade": "#F3F1F1",  
            "selectedlinkeffect": "#B1D6F0",  
            "globallinkcolor": "#1160B7",  
            "processcontrolcolor": "#D24726",  
            "headercolor": "#1160B7",  
            "logotooltip": "Microsoft CRM",  
            "hoverlinkeffect": "#D7EBF9",  
            "navbarshelfcolor": "#DFE2E8",  
            "navbarbackgroundcolor": "#002050",  
            "themeid": "f499443d-2082-4938-8842-e7ee62de9a23"  
        }  
    ]  
}  
```

 [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Query Data using the Web API](/powerapps/developer/data-platform/webapi/query-data-web-api).
  
<a name="BKMK_EditAndPublish"></a>

## Edit and publish theme data

 A theme is created by using the customization tools in the UI, without requiring a developer to write code. Details about how to apply these customizations can be found in [Change the color scheme or add a logo to match your organization's brand](../../customize/change-color-scheme-add-logo-match-organizations-brand.md).  

 Most theme data is stored within the Theme entity. Customized colors for specific entities is included in the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.EntityColor> property. This data is exported with the entity if the entity is included in a solution.

 The following table describes the `Theme` entity attributes that are valid for update and contain data that is applied by the theme:  

|Schema Name|Type|Value of default theme|Description|  
|-----------------|----------|----------------------------|-----------------| 
|AccentColor|String|#E83D0F|The Unified Interface secondary theme color to be used on the process control.| 
|BackgroundColor|String|#FFFFFF|For internal use only.|
|ControlBorder|String|#BDC3C7|The color that controls will use for borders.|  
|ControlShade|String|#FFFFFF|The color for controls to use to indicate when you hover over items.|  
|DefaultCustomEntityColor|String|#00CCA3|The default custom entity color if no color is assigned.|  
|DefaultEntityColor|String|#666666|The default color for system entities if no color is assigned.|  
|GlobalLinkColor|String|#1160B7|The color for links, such as email addresses or lookups.|  
|HeaderColor|String|#1160B7|The color for header text, such as form tab labels.|  
|HoverLinkEffect|String|#E7EFF7|The color that commands or lists will use when you hover over the items.|  
|ImportSequenceNumber|Integer|null|Sequence number of the import that created this record.|
|IsDefaultTheme|Boolean|True|The default value for a custom theme is false.|
|LogoId|String|null|The name of a web resource to use as a logo. Recommended dimensions are a height of 50 pixels and a maximum width of 400 pixels.|  
|LogoToolTip|String|Microsoft Dynamics 365 Customer Engagement|The text that will be used as the tooltip and alt text for the logo.| 
|MainColor|String|#3B79B7|The Unified Interface primary theme color to be used on main command bar, buttons and tabs.| 
|Name|String|CRM Default Theme|The name of the Theme entity.|  
|NavBarBackgroundColor|String|#002050|The primary navigation bar color.|  
|NavBarShelfColor|String|#DFE2E8|The secondary navigation bar color.|  
|OverriddenCreatedOn|DateTime|null|Date and time that the record was migrated.|  
|PageHeaderBackgroundColor|String|#E0E0E0|The page header background color.|  
|PanelHeaderBackgroundColor|String|#F3F3F3|The panel header background color.|  
|ProcessControlColor|String|#41A053|The primary color for process controls.|  
|SelectedLinkEffect|String|#F8FAFC|The color that commands or lists will use to indicate selected items.| 
|TransactionCurrencyId|Lookup|null|Exchange rate for the currency associated with the Theme with respect to the base currency.| 
 
 After you have applied changes, use the <xref href="Microsoft.Dynamics.CRM.PublishTheme?text=PublishTheme Action" /> or <xref:Microsoft.Crm.Sdk.Messages.PublishThemeRequest> class to make one of the theme records the current theme.  

<a name="BKMK_ExportingAndImportingThemes"></a>

## Exporting and importing themes

 Because themes aren't included as part of a solution, if you want to transfer themes from one organization to another you can use the Configuration Migration tool to generate a schema, export the theme data, and import it into a different organization. For details about how to use this tool, see [Move configuration data using the Configuration Migration Tool](../../admin/manage-configuration-data.md).  

### See also

 [Theme Entity](/power-apps/developer/data-platform/reference/entities/theme)   
 [Create a theme](../../customize/change-color-scheme-add-logo-match-organizations-brand.md)  
 [Developers guide to customization for Microsoft Dynamics 365 Customer Engagement](customize-applications.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
