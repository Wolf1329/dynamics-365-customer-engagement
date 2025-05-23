---
title: "Set grid properties for Unified Interface apps in Dynamics 365 Customer Engagement (on-premises)"
description: "As an app maker working with a Unified Interface app, you can configure the Read Only Grid control and its properties for custom grids and lists."
keywords: 

ms.custom: 
ms.topic: how-to
applies_to: 
  - Dynamics 365 for Customer Engagement (online)
  - powerapps
author: Mattp123
ms.assetid: 3ecea4a7-0d18-4ccd-9609-3a62179e9e1b
ms.author: matp
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 0
topic-status: Drafting
search.audienceType: 
  - customizer

---
# Configure the properties for custom grids and lists in Unified Interface apps

The Unified Interface framework uses responsive design principles to provide an optimal viewing and interaction experience for any screen size or orientation. With custom business apps that use the Unified Interface framework, the grid (view) control is responsive. As the size of the container decreases—for example, on phones and smaller viewports—the grid is transformed into a list. 

The Read Only Grid control specifies how a grid should reflow to different screen sizes. As an app maker, if you’re working with a Unified Interface app, you can configure the Read Only Grid control and its properties for custom grids and lists.
- **Card Form property:** Use a card form for lists instead of the default list template. Card forms provide more information for list items than the default list template.
- **Reflow behavior property:** Use this parameter to specify a grid to reflow in to a list or not.

## Allow grid to reflow into list

Adding the Read Only Grid control to your controls list allows you to  configure the following features: 
- Allow a grid to reflow into a list on small displays such as mobile.
- Specify the rendering mode as grid-only or list-only.  

1. Open solution explorer.
2. In navigation pane expand **Entities**, select the appropriate entity (such as **Account** or **Contact**), and then on the **Controls** tab, select **Add Control**.

    ![Open add control.](media/UnifiedInterface_ReadOnlyGrid_AddControl.png "Open Add Control")

3. Select **Read Only Grid** from the list of controls, and then choose **Add**.

    The control is added to the list of available controls.

    ![Select a control.](media/UnifiedInterface_ReadOnlyGrid_SelectControl.png "Select a Control")

4. Select the devices (**Web**, **Phone**, or **Tablet**) for which you want to make the grid read-only.

    ![Select the device type.](media/UnifiedInterface_ReadOnlyGrid_SelectDevice.png "Select devices")

5. Configure the **Card Form** property.

    You can use the Card Form property to show list items instead of the default list template. Card forms provide more information for list items than the default list template does.    

    a. Choose the pencil icon next to **Card Form**.

    ![Edit card form.](media/UnifiedInterface_ReadOnlyGrid_CardForm.png "Edit card form")

    b.  Select the **Entity** and **Card Form** types.

    ![Card form properties.](media/UnifiedInterface_ReadOnlyGrid_CardFormProperties.png "Card form properties")

    c. Choose **OK**.
6. Configure the **Reflow behavior** property. 

    a. Choose the pencil icon next to **Reflow behavior**.

    ![Edit Reflow behaviour.](media/UnifiedInterface_ReadOnlyGrid_EditReflow.png "Edit Reflow behaviour")

    b. Select the grid flow type from **Bind to static options** drop down.

    |Flow Type|Description|
    |--------------|--------------------|
    |**Reflow**|Allows the grid to render into list mode depending when there is no enough display space.|
    |**Grid Only**|Restricts the grid to reflow into list even when there is no enough display space.|
    |**List Only**|Displays only as a list even when there is enough space to display as grid.|

     ![Reflow behaviour properties.](media/UnifiedInterface_ReadOnlyGrid_ReflowProperties.png "Reflow behaviour properties")

    c. Choose **OK**.


7. Save and publish the changes. 


## Conditional image
You can display a custom icon instead of a value in a list and establish the logic used to select them based on a column’s values by using JavaScript. For more information about conditional images, see [Display custom icons instead of values in list views](display-custom-icons-instead.md).

### See also
[Create or edit a view](create-edit-views.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
