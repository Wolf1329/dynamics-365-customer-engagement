You can have multiple schedule board tabs configured for your business needs. As the owner of a schedule board tab, you can share the tab.

## Share a schedule board tab

By default, a new schedule board tab is visible only to the user who creates it and users with higher access levels such as org administrators. Use the schedule board tab settings to share a tab.

1. On the schedule board, select the vertical ellipsis &vellip; next to a schedule board tab name and select **Board settings**.

   :::image type="content" source="../../field-service/media/schedule-board-tab-settings.png" alt-text="Screenshot of the vertical ellipsis and the settings option.":::

1. Under **Shared With** select one of the sharing options.

   - **Everyone** exposes the tab to all users who can access the schedule board.
   - **Just Me** restricts the tab to you only.
   - **Specific People** [shares the tab with other users that you choose](#choose-users-to-share-the-schedule-board-tab).

   > [!NOTE]
   > Every user with the Schedule Board Setting read privilege set to User can see tabs shared with them. Admins can create custom security roles. Users with higher privileges to Schedule Board Setting records can access schedule board tabs even if they aren't shared with them directly. Managing schedule board access for teams by creating custom security roles and editing permissions isn't supported. Instead, choose users to share the schedule board tab.

## Choose users to share the schedule board tab

The schedule board saves tabs as records in the *Schedule Board Settings* table. To share a tab with specific people, use the [Schedule board settings management control](/dynamics365/guidance/resources/fs-schedule-board-settings-management-control).

> [!TIP]
> Alternatively, you can also directly access a schedule board settings record by finding the relevant ID with this URL: `[OrgUrl]/api/data/v9.2/msdyn_scheduleboardsettings`.
> Using the ID, construct URL with the following format and share the schedule board settings as above: `[OrgUrl]//main.aspx?pagetype=entityrecord&etn=msdyn_scheduleboardsetting&id=[yourSettingId]`
