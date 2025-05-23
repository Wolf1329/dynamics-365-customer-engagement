---
title: "Add transformation mappings for import (Developer Guide for Dynamics 365 Customer Engagement) | MicrosoftDocs"
description: "Transformation mapping enables optional modification of source data before importation."
ms.custom: 
ms.reviewer: pehecke

ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
applies_to: 
  - Dynamics 365 Customer Engagement (on-premises)
helpviewer_keywords: 
  - using transformation mapping to modify data before importing
  - transformation mappings, definition
  - adding transformation mappings for importing, list of valid property values
  - "adding transformation mappings for importing, transformations: concatenation; split; substring; replace; assign value; add to date; and others"
  - implementing transformation mapping, by using the transformation mapping entity
  - adding transformation mappings for importing, using the transformation mapping and transformation parameter mapping entities
  - transformation mappings for importing, adding
  - adding transformation mappings for importing, using transformation mapping to modify data before importing
  - adding transformation mappings for importing, available transformations with their descriptions and input parameters
  - transformations for mapping, concatenation; split; substring; replace; assign value; add to date; and others
ms.assetid: c5c6c8ac-0206-4658-8f4b-58310ecd9c29
author: JimDaly
ms.author: jdaly
search.audienceType: 
  - developer

---
# Add transformation mappings for import

Use transformation mapping to modify data before importing it. For example, split a full name that is contained in the source file into a first name and a last name to match the target attributes for an entity.  

 To implement transformation mapping, use the transformation mapping (`TransformationMapping`) entity and transformation parameter mapping (`TransformationParameterMapping`) entity.  

 The transformed data must be compatible with the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] entity attribute types.  

 The transformation type is described by the `TransformationMapping.TransformationTypeName` property. The valid values for this property are listed in the following table:  

|Field|Value|  
|-----------|-----------|  
|AddToCurrentDate|"Microsoft.Crm.Transformations.AddToCurrentDate"|  
|AddToDate|"Microsoft.Crm.Transformations.AddToDate"|  
|AdvancedAddToCurrentDate|"Microsoft.Crm.Transformations.AdvancedAddToCurrentDate"|  
|AssignValue|"Microsoft.Crm.Transformations.AssignValue"|  
|Concatenate|"Microsoft.Crm.Transformations.Concatenate"|  
|Replace|"Microsoft.Crm.Transformations.Replace"|  
|Split|"Microsoft.Crm.Transformations.Split"|  
|Substring|"Microsoft.Crm.Transformations.Substring"|  

 The following sections describe the available transformations.  

<a name="BKMK_Concatenation"></a>   
## Concatenation  
 Concatenates strings and separates them with a delimiter.  

|Input Parameters|Description|  
|----------------------|-----------------|  
|Prefix|String that is used as a prefix in the concatenated string.|  
|Suffix|String that is used as a suffix in the concatenated string.|  
|Delimiter|One character or combination of characters that separate substrings inside the concatenated string. The delimiter is not used between the prefix and the substring or between the suffix and the substring. Do not use the backspace (\b), newline (\n), and return (\r) characters as a delimiter.|  
|\<Variable>|Array of variable length that contains substrings.|  

|Output Parameters|Description|  
|-----------------------|-----------------|  
|String|Concatenated string.|  

<a name="BKMK_Split"></a>   
## Split  
 Separates a string that includes a delimiter into substrings. There can be up to ten substrings.  

|Input Parameters|Description|  
|----------------------|-----------------|  
|Input String|String that contains one or more substrings that is separated with delimiters.|  
|Delimiter|One character or combination of characters that separate substrings inside the string. Do not use the backspace (\b), newline (\n), and return (\r) characters or empty strings as a delimiter.|  

|Output Parameters|Description|  
|-----------------------|-----------------|  
|Variable|Substrings 1 through maximum of 10.|  

 For example, if the input string contains eleven substrings, the output contains ten substrings as shown in the following example:  

 Input string: a;b;c;d;e;f;g;h;i;j;k  

 Output:  

 a  

 b  

 c  

 d  

 e  

 f  

 g  

 h  

 i  

 j;k  

<a name="BKMK_Substring"></a>   
## Substring  
 Returns a substring of a specified length, starting at a specified point in the string.  

|Input Parameters|Description|  
|----------------------|-----------------|  
|Input String|String that contains a substring.|  
|Start Index|Starting position of the substring.|  
|Length|Length of the substring. If the length is **null**, returns a complete string from the start index.|  

|Output Parameters|Description|  
|-----------------------|-----------------|  
|Substring|Returned substring.|  

<a name="BKMK_Replace"></a>   
## Replace  
 Replaces all occurrences of a specified string with another specified string.  

|Input Parameters|Description|  
|----------------------|-----------------|  
|Input String|String that contains a search string.|  
|Search String|Search string. Do not use the backspace (\b), newline (\n), and return (\r) characters as a search string.|  
|Replace String|Replacement string. Use an empty string to remove a search string. Do not use the backspace (\b), newline (\n), and return (\r) characters as a replacement string.|  

|Output Parameters|Description|  
|-----------------------|-----------------|  
|Value|Replacement value (same as assigned value).|  

<a name="BKMK_AssignValue"></a>   
## Assign value  
 Replaces all values with a specified value.  

|Input Parameters|Description|  
|----------------------|-----------------|  
|Value|Value that you want to assign.|  

|Output Parameters|Description|  
|-----------------------|-----------------|  
|Value|Replacement value (same as assigned value).|  

> [!NOTE]
>  Date transformations can only be used for correctly formatted dates. For information about how to format dates, see [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] Help.  

<a name="BKMK_AddToDate"></a>   
## Add to date  
 Adds a specified number of days, months, and years to a date.  

|Input Parameters|Description|  
|----------------------|-----------------|  
|Date|Date string that is to be modified.|  
|Year Offset|Positive or negative value that is added to the year component of an input date.|  
|Month Offset|Positive or negative value that is added to the month component of an input date.|  
|Day Offset|Positive or negative value that is added to the day component of an input date.|  

|Output Parameters|Description|  
|-----------------------|-----------------|  
|New Date|New data string that contains day, month, and year added in this order.|  

<a name="BKMK_AdjustCurrentDate"></a>   
## Adjust current date and set time  
 Adds a specified number of days, months, and years to the current date and sets the specified time. The offsets can only be integer numbers.  

|Input Parameters|Description|  
|----------------------|-----------------|  
|Year Offset|Positive or negative value that is added to the year component of a current date.|  
|Month Offset|Positive or negative value that is added to the month component of a current date.|  
|Day Offset|Positive or negative value that is added to the day component of a current date.|  
|Hours|Value that is used to set the hours component of a current date.|  
|Minutes|Value that is used to set the minutes component of a current date.|  
|Seconds|Value that is used to set the seconds component of a current date.|  
|Day of Week|Day of the week that can be Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, or Sunday. The days of the week are represented by whole numbers, starting with decimal 1 for Monday. The values for days of the week are contained in the `DayOfWeek` enumeration. For more information about this enumeration, see the MSDN topic, [DayOfWeekEnumeration](/dotnet/api/system.dayofweek). <br />If the calculated current date does not fall on the specified day of the week, it is adjusted to the nearest earlier date that falls on the specified day of the week. The current date is always adjusted to a date in the past. <br />For example, if you specify Wednesday as a day of the week, and the newly calculated date falls on Tuesday, March 9, then the date is adjusted to Wednesday, March 3.|  

|Output Parameters|Description|  
|-----------------------|-----------------|  
|New Date|New data string that contains day, month, and year added in this order.|  

<a name="BKMK_AdvancedAdd"></a>   
## Advanced add to current date  
 Adds a specified number of days, months, and years to the current date. You can specify whether offsets are relative to the current date or absolute values. The offsets can only be integer numbers.  

 For example, if you use an absolute value of 3 for a month offset, the newly calculated month is March. If you set a relative to current date month offset to 3, and the current month is April, the newly calculated month is July.  


| Input Parameters  |                                                                                                                                                                                                         Description                                                                                                                                                                                                         |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Year Offset    |                                                                                                                                                             Positive or negative value that is added to the year component of a current date or absolute year.                                                                                                                                                              |
| Year Offset Mode  | Specify whether the offset is relative to the current date or absolute value by using the `TransformationParameterMapping.Data` attribute. If you are using early bound types, you can use the `TransformationOffsetMode` enumeration to specify relative or absolute offset. For a list of the DataTypeCode values, see the picklist values for this entity. [!INCLUDE[metadata_browser](../includes/metadata-browser.md)] |
|   Month Offset    |                                                                                                                                                            Positive or negative value that is added to the month component of a current date or absolute month.                                                                                                                                                             |
| Month Offset Mode |                                Specify whether the offset is relative to the current date or absolute value by using the `TransformationParameterMapping.Data` attribute. If you are using early bound types, you can use the `TransformationOffsetMode` enumeration to specify relative or absolute offset. For a list of the DataTypeCode values, see the picklist values for this entity.                                |
|    Day Offset     |                                                                                                                                                              Positive or negative value that is added to the day component of a current date or absolute day.                                                                                                                                                               |
|  Day Offset Mode  |                                Specify whether the offset is relative to the current date or absolute value by using the `TransformationParameterMapping.Data` attribute. If you are using early bound types, you can use the `TransformationOffsetMode` enumeration to specify relative or absolute offset. For a list of the DataTypeCode values, see the picklist values for this entity.                                |
|       Hours       |                                                                                                                                                                                   Value that sets the hours component of a current date.                                                                                                                                                                                    |
|      Minutes      |                                                                                                                                                                                  Value that sets the minutes component of a current date.                                                                                                                                                                                   |
|      Seconds      |                                                                                                                                                                                  Value that sets the seconds component of a current date.                                                                                                                                                                                   |

|Output Parameters|Description|  
|-----------------------|-----------------|  
|New Date|New data string that contains day, month, and year, added in this order. First, the relative components are added, and then the absolute values are used to form a date.|  

### See also  
 [Import Data in Dynamics 365 Customer Engagement (on-premises)](import-data.md)   
 [Create data maps for import](create-data-maps-for-import.md)   
 [Configure Data Import](configure-data-import.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
