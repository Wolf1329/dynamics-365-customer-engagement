---
title: "Add Relationship intelligence widgets to custom forms"
description: "If you're using custom forms, add the health score and who knows whom widgets manually to the form."
ms.date: 02/14/2025
ms.custom: 
ms.topic: how-to
author: lavanyakr01
ms.author: lavanyakr
ms.reviewer: lavanyakr
---
# Add Relationship intelligence widgets to custom forms

By default, the health score widget and who knows whom widget are available only in the out-of-the-box **Sales Insights** form. If you're using customized forms, you can display these widgets on your custom forms by manually adding them to your form.

## Add widgets to a custom form

To add the health score widget or who knows whom widget to your custom form, follow these steps:

> [!IMPORTANT]
> - Widgets are only supported in Unified Interface apps.
> - You can't use the legacy form designer to add the widgets to a form.

1. Sign in to the [Power Apps](https://make.powerapps.com/) portal.

2. Search for and select your organization's environment.

    :::image type="content" source="media/power-apps-select-org.png" alt-text="Screenshot of selecting your organization in the Power Apps portal.":::

3. In the left pane, select **Tables**.

4. On the **Tables** page, select a table to open it.

1. On the **Data experiences** card, select **Forms**.

1. Select a main form to add the widget to. In this example, the table **Account** is selected and the main form **Account** is selected.

    >[!NOTE]
    >If you're unable to view the table to which you want to add the widget, in the upper-right corner of the page, change the filters settings to **All**.

    :::image type="content" source="media/power-apps-lead-main-form.png" alt-text="Screenshot of selecting the Lead main form on the Forms tab.":::

5. In the form designer, select **Component**, and then from **Layout**, add a column to the form as a placeholder to add the widget.

    :::image type="content" source="media/power-apps-layout-add-column-form.png" alt-text="Screenshot of adding a column to the form in the form designer.":::

7. Depending on the widget you want to add, do one of the following actions:
    - To add the health score widget, select **Display** > **Relationship Health**.
    - To add the who knows whom widget, select **Display** > **Who Knows Whom**.    
        >[!NOTE]
        >Ensure that the added placeholder column is selected. If it isn't, the widget will be added at a random place in the form.   
    In this example, let's select the **Who Knows Whom** widget.
    > [!div class="mx-imgBorder"]  
    > ![Select the who knows whom widget](media/power-select-who-knows-whom-widget.png "Select the who knows whom widget")

8. In the pop-up window, select the components on which you want to display the widget, and select **Done**.

    The widget is added to the form, as shown in the following image.

    :::image type="content" source="media/power-app-who-knows-whom-widget-added.png" alt-text="Screenshot of the Who knows whom widget added to the form.":::

    >[!NOTE]
    >To hide the **New section** label, go to the **Properties** tab of the **New Section** settings pane, and then select **Hide label**.

9. Save and publish the form.
    > [!NOTE]
    > If you'd like roles other than Salesperson and Sales Manager to access the who knows whom widget, [grant access to those roles](grant-access-wkw.md). 


[!INCLUDE[cant-find-option](../includes/cant-find-option.md)]
