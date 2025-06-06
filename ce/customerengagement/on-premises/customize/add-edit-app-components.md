---
title: "Add app components with Dynamics 365 Customer Engagement (on-premises)"
description: "Learn how to use the app designer to easily add components such as entities, dashboards, business process flows, forms, charts, and views."
keywords: 

ms.custom: 
ms.topic: how-to
applies_to: 
  - Dynamics 365 for Customer Engagement (online)
author: Mattp123
ms.assetid: be93b9d7-f1c2-4ee7-8d7c-0f5c34dfa5f7
ms.author: matp
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 17
topic-status: Drafting
search.audienceType: 
  - customizer

---

# Add or edit app components using the app designer

[!INCLUDE [applies-to-on-premises](../includes/applies-to-on-premises.md)] [Add or edit model-driven app components in the Power Apps app designer](/powerapps/maker/model-driven-apps/add-edit-app-components)

An app is composed of various components. You can add two types of components to an app: artifacts and entity assets. In the context of the app designer, entities, dashboard, and business process flows are all artifacts of an app. Entity assets consist of forms, views, charts, and dashboards.  
  
The app designer refers to existing metadata in the default solution. You can use it to create components like forms, views, charts, and dashboards.  
  
## App designer layout  
 The app designer has two main areas. On the left side is the canvas where you add app components.  
  
 ![App designer canvas.](../customize/media/app-designer-canvas-pane.png "App designer canvas")  
  
 On the right side are tabs that you'll use to select components and set component properties.  
  
 ![App designer components.](../customize/media/app-designer-canvas-components-tab.png "App designer components")  
  
 On the canvas, you'll see areas for the site map, business process flow, dashboard, and entities. When you select a dashboard or business process flow, or configure a site map, the app designer automatically adds the entities that are used in these components to the canvas. After the entities are in place, all you need to do is select each entity and add required entity assets such as forms, views, and charts to it.
 
 You can also use **Search Canvas** to search for components on the canvas. When you select **Search Canvas**, a new search tab opens to the right of the tabs in the rightmost pane.   
  
 ![Canvas search option.](media/app-designer-search-tab.png "Canvas search")

## Add an artifact (entity, dashboard, or business process flow)  
 When you add a dashboard or business process flow to an app, the entities they use are automatically added to the app. When you add an entity, the tiles for its assets are automatically added. There are two ways you can add artifacts to the designer canvas: by using the **Add** button ![Add button on the designer.](../customize/media/dynamics365-designer-addbutton.PNG "Add button on the designer") on the command bar or by using the tiles on the **Components** tab.  

> [!NOTE]
> Unlike business process flows, you don't add task flows to an app.  For more information about task flows, see [Create a mobile task flow](create-mobile-task-flow.md). Also, task flows are not app aware. When you activate task flows, they become available across all model driven apps.
  
 Here are the steps for adding a dashboard to the app. Use the same steps to add a business process flow or entity.  
  
1. On the app designer canvas, select the **Dashboards** tile.  
  
    On the app designer canvas, the rightmost pane shows you dashboards that are available in the default solution.  
  
   > [!TIP]
   >  Alternatively, you can also do one of the following:  
   >   
   > - Select **Add**![Add button on the designer.](../customize/media/dynamics365-designer-addbutton.PNG "Add button on the designer"), and then select **Dashboards**.  
   > - On the **Components** tab, under **Artifacts**, select **Dashboards**.  
  
2. In the **search** box, type a few keywords for the dashboard name you're looking for.  
  
    The dashboard list will be filtered to show results that match your keywords.  
  
3. If you want your users to use only selected dashboards, select the check box for the dashboards you want to add. You can select from the following types of dashboards:
   - **Classic Dashboards** appear on both the web app and the Unified Interface app.
   - **Interactive Dashboards** appear only on the Unified Interface app. If you have selected the client type for the app as web app, the **Interactive Dashboards** option will not be displayed.

     Those dashboards will be added to the **Dashboard** tile on the app designer canvas. The **Dashboard** tile also shows a count of the number of dashboards you added to the app. If you don't select a dashboard, **All** will appear instead of the dashboard count, and all dashboards will be available to users when they use the app.  
  
     All entities the dashboard uses are also added to the **Entity View** area. For example, if you add the Customer Service Manager dashboard, the Case, Entitlement, and Queue Item entities are added to the Entity View area. For each entity, tiles for its assets are also added. You can use these tiles to add forms, views, and charts. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Add entity assets (forms, views, or charts)](../customize/add-edit-app-components.md#bkmk_AddEntityAssets)  
  
   ![Add entity to the app designer canvas.](../customize/media/add-entity-app-designer-canvas.png "Add an entity to the app designer canvas")  
  
4. If the dashboard you want doesn't exist in the default solution, create a dashboard by selecting **Create New** on the **Components** tab to the right of the canvas.  
  
    ![Create New link on the Components tab of app designer.](../customize/media/app-designer-components-tab-create-new.png "Create New link on the Components tab of the app designer")  
  
    The dashboard designer opens. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Create and edit dashboards](../customize/create-edit-dashboards.md)  
  
   > [!NOTE]
   > - When you're adding a business process flow or entity, the **Create New** option opens the corresponding designer. To learn more about creating business process flows or entities, see [Create a business process flow](../customize/create-business-process-flow.md) and [Create and edit entities](../customize/create-edit-entities.md).  
      
  
5. When you're done adding artifacts, on the command bar, select **Save**.  
  
<a name="bkmk_AddEntityAssets"></a>   
## Add entity assets (forms, views, charts, or dashboards)  
 With the artifacts in place, you can start adding entity assets like forms, views, charts, and dashboards to the app.
 Additionally, if you're using the Unified Interface client, you can also add entity dashboard assets to the app.  
  
 This section describes the steps for adding a form to the app. Use the same steps to add a view or chart to the app.  
  
1. On the app designer canvas, select the **Forms** tile for the entity you want to add a form to.  
  
    On the app designer canvas, the entire row for the entity is selected. On the right side, you'll see all existing forms for the selected entity.  
  
   > [!NOTE]
   >  Alternatively, you can also do one of the following:  
   >   
   > - Select **Add**![Add button on the designer.](../customize/media/dynamics365-designer-addbutton.PNG "Add button on the designer"), and then select **Forms**.  
   > - On the **Components** tab, under **Entity Assets**, select **Forms**.  
  
   > [!TIP]
   >  For all entities selected for the app, a **More Options** button (**...**) appears in the **Select Entities** list on the **Components** tab. To add all assets for the selected entity, select **More Options** (**...**), and then select **Add All Assets**.  
  
2. If you want your app users to use only selected forms, select the check boxes for the forms you want to add. The forms define how users will see and interact with data in the app. 
 
    The form tile of the selected entity will display the number of forms added.  
  
    ![Form tile for case entity.](../customize/media/add-forms-entity.png "Form tile for case entity")  
  
    For example, if you don't select any form for an entity, all the forms for that entity will be displayed to end users while they use the app. This behavior is similar for views and charts also, if no view or chart is selected. This helps to create apps quickly when you need to work with all available components; there's no need to select each component during app design.  

    If no dashboards or business process flows are selected, all the dashboards and business process flows will be available for users while they use the app.
  
   > [!NOTE]
   > For the app to run, each entity that you add must have at least one active form. If you've selected multiple forms, the first active form that appears in the default solution will be used when users run the app.  
  
3. If you want to add a new form that's not available in the list, select **Create New**.  
  
    In the drop-down list, select the type of form you want to create.  
  
   > [!NOTE]
   >  The drop-down list is available only when you're adding forms. It isn't available for views and charts.  
  
    The form designer opens. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Create and design forms](../customize/create-design-forms.md)  
  
    When you're adding a view or a chart, the **Create New** option opens the corresponding designer. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Create and edit views](../customize/create-edit-views.md) and [Create or edit a system chart](../customize/create-edit-system-chart.md)  
  
   > [!NOTE]
   >  When you're adding a view, you can reference only public views that are listed under the **Views** node in the solution explorer.  
  
4. Select the down arrow ![Drop down icon.](../customize/media/drop-down-icon.png "down arrow") to expand the tile and see a list of forms that have been added.  
  
     ![Form tile expanded in app designer.](../customize/media/app-designer-expanded-form-tile.png "Form tile expanded in the app designer")  
  
5. Repeat these steps to add entity views and charts to the app.  
  
6. Select **Save**.  
  
## Edit or remove artifacts  
  
- To edit a dashboard or a business process flow, select the down arrow ![Drop down icon.](../customize/media/drop-down-icon.png "down arrow") to expand the tile, and then select the site map designer button ![Open Site Map Designer button.](../customize/media/dynamics365-open-designer.PNG "Open Site Map Designer button") corresponding to the dashboard or business process flow that you want to edit.  
  
     The designer for the selected artifact opens.  
  
- To remove a dashboard or a business process flow, select the down arrow ![Drop down icon.](../customize/media/drop-down-icon.png "down arrow") to expand the tile, and then select the dashboard or business process flow that you want to remove. On the command bar, select **Remove**.  

    Another way to remove a dashboard or business process flow is by clearing the corresponding check box on the **Components** tab.
  
- To edit or remove an entity, select the entity tile, and then on the command bar, select **Edit** or **Remove**. When you edit an entity, the solution explorer opens, where you can make changes to the entity.  
  
     Another way to remove a component is to select the dashboard, business process flow, or entity tile. On the **Components** tab, clear the check boxes for the artifacts you want to remove from the designer.  
  
    > [!NOTE]
    >  When you make any changes to an entity&mdash;like changing an entity display name or description&mdash;the changes don't appear in the app designer unless the changes are published in the solution explorer.  
  
## Edit or remove entity assets  

### Edit entity assets
  
1. Select the down arrow ![Drop down icon.](../customize/media/drop-down-icon.png "down arrow") to expand the tile for forms, views, charts, or dashboards.  
  
2. Select the form, view, chart, or dashboard that you want to edit.  
  
3. On the command bar, select **Edit**.

   or

   Select the site map designer button ![Open Site Map Designer button](../customize/media/dynamics365-open-designer.PNG "Open Site Map Designer button") corresponding to the form, view, chart, or dashboard.  

### Remove entity assets  

1. Select the down arrow ![Drop down icon](../customize/media/drop-down-icon.png "down arrow") to expand the tile for forms, views, charts, or dashboards.  
  
2. Select the form, view, chart, or dashboard that you want to edit.

3. On the command bar, select **Remove**. 

Alternatively, you can select the forms, views, charts, or dashboards tile, and then on the **Components** tab, clear the check boxes for the assets you want to remove from the designer.  
  
### See also  
 [Create a site map for an app](../customize/create-site-map-app.md)   
 [Publish an app](../customize/publish-an-app.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
