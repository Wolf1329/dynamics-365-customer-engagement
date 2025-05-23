---
title: "Understand charts: Underlying data and chart representation (Developer Guide for Dynamics 365 Customer Engagement) | MicrosoftDocs"
description: "Charts display data visually by mapping textual values on two axes: horizontal (x) and vertical (y). In Dynamics 365 Customer Engagement, the x axis is called the category axis and the y axis is called the series axis."
ms.custom: 
ms.reviewer: pehecke

ms.suite: 
ms.tgt_pltfrm: 
ms.topic: concept-article
applies_to: 
  - Dynamics 365 Customer Engagement (on-premises)
helpviewer_keywords: 
  - charts, understand
ms.assetid: 05ada555-b535-4371-8029-176c454ada26
caps.latest.revision: 41
author: JimDaly
ms.author: jdaly
search.audienceType: 
  - developer

---
# Understand charts: Underlying data and chart representation

Charts display data visually by mapping textual values on two axes: horizontal (x) and vertical (y). In [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)], the x axis is called the *category* axis and the y axis is called the *series* axis. The category axis can display numeric as well as non-numeric values whereas the series axis only displays numeric values.  
  
 Charts in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] can be further classified into the following:  
  
- **Single-series charts**: Charts that display data with a series (y) value mapped to a category (x) value.  
  
- **Multi-series charts**:  Charts that display data with multiple series values mapped to a single category value. Multi-series charts include stacked column charts, which vertically display the contribution of each series to a total across categories, and 100% stacked column charts, which compare the percentage that each series contributes to a total across categories. You can combine different compatible chart types in multi-series charts, for example, column and line, bar and line, and so on.  
  
> [!NOTE]
>  Multi-category charts can be created through the web application or by modifying the XML strings described here.  
  
 While authoring a chart in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] using the SDK, you need to consider the following two important aspects:  
  
- **Underlying data for the chart**: Specified using the *data description* XML string.  
  
- **Data representation (appearance)**: Specified using the *presentation description* XML string.  
  
> [!NOTE]
> [!INCLUDE[pn_ms_chart_controls_short](../../includes/pn-ms-chart-controls-short.md)] lets you create various types of charts such as column, bar, area, line, pie, funnel, bubble, and radar. The chart designer in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] lets you create only certain types of charts. However, using the SDK, you can create most of the chart types that are supported by [!INCLUDE[pn_ms_chart_controls_short](../../includes/pn-ms-chart-controls-short.md)].  
  
## Use the data description XML string to specify chart data  
 The data description XML string defines the data that will displayed on the chart. The contents of the XML string are validated against the visualization data description schema. For more information about the schema, see [Visualization Data Description Schema](visualization-data-description-schema.md).  
  
 You can specify the data description XML string while you are creating a chart using the `SavedQueryVisualization.DataDescription` or the `UserQueryVisualization.DataDescription` attribute for the organization-owned or user-owned chart respectively.  
  
 The data description XML string contains the following two elements: `<FetchCollection>` and `<CategoryCollection>`.  
  
### The \<FetchCollection> element  
 The `<FetchCollection>` element uses FetchXML to retrieve data for the chart. The FetchXML query specifies information about the entity attributes, aggregate functions, and the group by clauses for the data to be displayed in a chart. All the FetchXML aggregate functions are supported for charts. For more information about the FetchXML aggregate functions, see [Using FetchXML Aggregration](/powerapps/developer/data-platform/use-fetchxml-aggregation).  
  
 The FetchXML query enables you to filter your data. Also, filters are applied on charts through views. Therefore, if a filter condition is already specified in the FetchXML query in the `<FetchCollection>` element, and additionally a filter is applied through a view, the chart will display data that is returned after it applies all the filters. For more information about how to use the FetchXML query to filter data, see [Building Queries with FetchXML](/powerapps/developer/data-platform/use-fetchxml-construct-query).  
  
> [!NOTE]
>  Although the data description XML string is validated again the visualization data description schema, the FetchXML query inside the `<FetchCollection>` element is not. The FetchXML query is validated against the FetchXML schema. For more information, see [Fetch XML Schema](/powerapps/developer/data-platform/fetchxml-schema).  
  
 If the chart is a comparison chart, the `<FetchCollection>` element will contain two *group by* clauses.  
  
### The \<CategoryCollection> element  
 The `<CategoryCollection>` element contains information about the category (horizontal) and the series (vertical) axes in a chart.  
  
-   Each `<Category>` sub-element has a child element called `<MeasureCollection>` that maps to the `<Series>` element in the presentation description XML. A single series chart has a single `<MeasureCollection>` child element whereas a multi-series chart will have multiple `<MeasureCollection>` child elements, each mapped to the respective `<Series>` element in the presentation description XML.  
  
-   Each `<MeasureCollection>` child element has an element called `<Measure>` that corresponds to the series (vertical) axis value, corresponding to each value on the category (horizontal) axis.  
  
### Example  
 The following is a sample data description XML string:  
  
```xml  
<datadefinition>  
  <fetchcollection>  
    <fetch mapping="logical" count="10">  
      <entity name="opportunity">  
        <attribute name="estimatedvalue" />  
        <order attribute="estimatedvalue" descending="true" />  
      </entity>  
    </fetch>  
  </fetchcollection>  
  <categorycollection>  
    <category>  
      <measurecollection>  
        <measure alias="estimatedvalue" />  
      </measurecollection>  
    </category>  
  </categorycollection></datadefinition>  
```  
  
 For more sample data description XML strings, see [Sample Charts](sample-charts.md).  
  
## Use the presentation description XML string to specify data representation  
 The presentation description XML string contains information about the appearance of the chart such as chart title, chart color, and chart type (bar, column, line, and so on). There is no schema definition for this XML string. However, the XML is a serialization of the [Chart](/dotnet/api/system.web.ui.datavisualization.charting.chart) class in [!INCLUDE[pn_ms_chart_controls_short](../../includes/pn-ms-chart-controls-short.md)]. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Chart Controls](https://go.microsoft.com/fwlink/p/?LinkId=128301)  
  
 You can specify the presentation description XML string while you are creating a chart using the `SavedQueryVisualization.PresentationDescription` or `UserQueryVisualization.PresentationDescription` attribute for the organization-owned or user-owned chart, respectively.  
  
### Example  
 The following is a sample presentation description XML string:  
  
```xml  
<Chart Palette="BrightPastel">  
  <Series>  
    <Series _Template_="All" Color="153, 204, 255" BorderColor="164, 164, 164" BorderDashStyle="Solid" BorderWidth="1" ShadowColor="128, 128, 128, 128" ShadowOffset="1" IsValueShownAsLabel="true" Font="{0}, 6.75pt" BackGradientStyle="TopBottom" BackSecondaryColor="0, 102, 153" LabelForeColor="100, 100, 100" ChartType="Column">  
      <SmartLabelStyle Enabled="True" />  
      <Points />  
    </Series>  
  </Series>  
  <ChartAreas>  
    <ChartArea _Template_="All" BackColor="White" BorderColor="26, 59, 105" BorderWidth="0" BorderDashStyle="Solid">      <AxisY LineColor="204, 204, 204" TitleFont="{0}, 8pt, GdiCharSet=0" TitleForeColor="100, 100, 100" LabelAutoFitMaxFontSize="7" LabelAutoFitMinFontSize="7">  
        <MajorTickMark LineColor="Gray" />  
        <MajorGrid Enabled="false" />  
        <LabelStyle Font="{0}, 6.75pt, GdiCharSet=0" ForeColor="100, 100, 100" />  
      </AxisY>  
      <AxisX LineColor="204, 204, 204" TitleFont="{0}, 8pt, GdiCharSet=0" TitleForeColor="100, 100, 100" LabelAutoFitMaxFontSize="7" LabelAutoFitMinFontSize="7">        <MajorTickMark LineColor="Gray" />        <MajorGrid Enabled="false" />  
        <LabelStyle Font="{0}, 6.75pt, GdiCharSet=0" ForeColor="100, 100, 100" />  
      </AxisX>  
    </ChartArea>  
  </ChartAreas>  
  <Titles>  
    <Title _Template_="All" Font="{0}, 9pt, style=Bold, GdiCharSet=0" ForeColor="100, 100, 100"></Title>  
  </Titles>  
  <BorderSkin PageColor="Control" BackColor="CornflowerBlue" BackSecondaryColor="CornflowerBlue" />  
</Chart>  
```  
  
 For more sample presentation description XML strings, see [Sample Charts](sample-charts.md).  
  
### See also  
 [Visualizations (Charts)](view-data-with-visualizations-charts.md)   
 [Actions on Visualizations (Charts)](actions-visualizations-charts.md)   
 [Create a Chart](create-visualization-chart.md)   
 [Building Queries with FetchXML](/powerapps/developer/data-platform/use-fetchxml-construct-query)   
 [Fetch XML Schema](/powerapps/developer/data-platform/fetchxml-schema)   
 [Visualization Data Description Schema](visualization-data-description-schema.md)   
 [Sample Charts](sample-charts.md)   
 [Chart Class (Microsoft Chart Controls)](/dotnet/api/system.web.ui.datavisualization.charting.chart)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
