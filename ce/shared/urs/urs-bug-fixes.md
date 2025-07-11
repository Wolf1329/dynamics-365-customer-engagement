## Release schedule

When a new version of Universal Resource Scheduling releases, it becomes available in different geographic regions at different times. The table shows estimates for when the next release will become available in the region of your environment.

For information about other updates to Universal Resource Scheduling, visit the Field Service section of the [Dynamics 365 release plans](/dynamics365/release-plans/).
For information about older versions, see [Version history archive](../../field-service/version-history-archive.md#universal-resource-scheduling).

| Station | Region | Current version | Next version | Scheduled date |
| ------- | ------ | --------------  | -----------  | -------------  |
|**Station 1** |  *First Release*| [3.12.151.455](/dynamics365/field-service/field-service-version-history-resource-scheduling#312151455) | TBD | 07/04/2025 |
|**Station 2** |  *South America, Canada, India, France, South Africa, Germany, Switzerland, Norway, Korea* | [3.12.151.455](/dynamics365/field-service/field-service-version-history-resource-scheduling#312151455) |  TBD | 07/11/2025 |
|**Station 3** | *United Arab Emirates, Japan, Asia Pacific, United Kingdom, Oceania, Singapore* | [3.12.150.423](/dynamics365/field-service/field-service-version-history-resource-scheduling#31250423) |  [3.12.151.455](/dynamics365/field-service/field-service-version-history-resource-scheduling#312151455) | 06/13/2025 |
| | *USG* | [3.12.151.455](/dynamics365/field-service/field-service-version-history-resource-scheduling#312151455) |  TBD | 07/18/2025 |
|**Station 4** |*Europe* |  [3.12.150.423](/dynamics365/field-service/field-service-version-history-resource-scheduling#31250423) |  [3.12.151.455](/dynamics365/field-service/field-service-version-history-resource-scheduling#312151455) | 06/20/2025 |
|**Station 5** |  *North America*| [3.12.150.423](/dynamics365/field-service/field-service-version-history-resource-scheduling#31250423)  |  [3.12.151.455](/dynamics365/field-service/field-service-version-history-resource-scheduling#312151455) | 06/27/2025 |
|**Station 6** | *Government Community Cloud, DoD, China*  | [3.12.150.423](/dynamics365/field-service/field-service-version-history-resource-scheduling#31250423) | [3.12.151.455](/dynamics365/field-service/field-service-version-history-resource-scheduling#312151455) | 06/25/2025 |
|**Station 6** | *Dedicated Scale Groups* |  [3.12.150.423](/dynamics365/field-service/field-service-version-history-resource-scheduling#31250423)  | [3.12.151.455](/dynamics365/field-service/field-service-version-history-resource-scheduling#312151455) | 07/04/2025 |
>[!NOTE]
>
> - Dates in all regions except Government Community Cloud (GCC), USG, and China are estimates of the next automatic update. Dates in GCC, USG, and China indicate version availability; at this time, there is no automatic update for the GCC, USG, and China regions.
> - For all other regions, while most updates should be complete on the scheduled night, updates requiring more time may be completed during dark hours over the weekend indicated in the **Scheduled date** column.

## 3.12.151.455

**Resource Scheduling Controls:** 1.2.90.251391

**Dataverse:** 4.0.141.455

- Schedule assistant now supports time zone agnostic bookings.
- Fixed a bug that was sometimes causing the schedule board to crash when using the context menu with multiple bookings at a time.
- Find availability is now also displayed when the default requirement tab is hidden.
- Time zone agnostic bookings are now compatible with schedule assistant when they fall on non-working days.
- Fixed a bug that was delaying newly scheduled bookings from appearing on multiday views.
- Fixed a bug that was impacting bookings and schedule board drag and drop in daily view.
- Fixed a bug that was causing requirement details to respect the user's device's time zone instead of the schedule board's time zone. 
- Fixed a bug that was causing the schedule board to not respect the selected sort order in list view. 
- Manually typing dates is now possible in all available date formats.
- Fixed a bug that was allowing users to resize imported appointments.
- Fixed a bug that was causing booking rules not to execute when making a booking from the booking panel. 
- Fixed a bug that was causing SOA to display all routes on the first day in the map view.

## 3.12.150.423 (Hotfix2)

**Resource Scheduling Controls:** 1.2.89.251331

**Dataverse:** 4.0.140.423

- Fixed a bug where booking templates were not working for None type entities
- Fixed a bug where requirement groups were reverting to UTC when using the Book button
- Fixed a bug that was causing the schedule board to crash when quickly right-clicking on new bookings for some users
  
## 3.12.150.423 (Hotfix1)

**Resource Scheduling Controls:** 1.2.89.251132

**Dataverse:** 4.0.140.423

- Fixed a bug that was causing "Move To" to not function for some users on the schedule board. 
- Various security enhancements.
  
## 3.12.150.416

**Resource Scheduling Controls:** 1.2.89.250863

**Dataverse:** 4.0.140.416

- Users can now change the resource view while the crew allocation tool is loading.
- Fixed a bug that was causing the booking card tooltip to refresh when loaded.
- Fixed a bug that was causing the schedule board to scroll when a booking was dragged off the schedule grid.
- Fixed a bug that was causing schedule assistant to respect the user time zone instead of the requirement's time zone when launched from  the requirement form.
- Fixed a bug that was inverting booking start/end times in booking rule parameters.
- Fixed a bug that was causing the wrong duration to be shown in the create booking panel after saving.
- Horizontal scroll location is now maintained on the schedule board when switching views. 
- Fixed a bug that was impacting the display of working days on the schedule board.
- Improved Scheduling Operations Agent error messaging when the start of an optimization range is in the middle of a break.
- Various visual improvements for Scheduling Operations Agent.
- Various security enhancements.

## 3.12.149.15

**Resource Scheduling Controls:** 1.2.88.250442

**Dataverse:** 4.0.139.15

- Released [**Scheduling Operations Agent**, an agent in Dynamics 365 Field Service ](../../field-service/soa-overview.md)that helps dispatchers improve the schedule of a single technician quickly and efficiently. This new feature is enabled across stations on a separate schedule: 
    - Station 2: March 28, 2025
    - Station 3 - March 31, 2025
    - Europe - April 1, 2025
    - North America - April 2, 2025
- Fixed a bug impacting requirement tooltips on the schedule board map. 
- Booking statuses in the booking panel are now sorted alphabetically.
- Fixed a bug that was improperly calculating remaining and fulfilled durations when deleting a booking spanning multiple days or when deleting multiple bookings. 
- The lookup records panel's advanced lookup feature now defaults to the view the requirements panel is currently using on the schedule board. 
- Fixed a bug that was causing schedule assistant to crash for some users when opened in a small window and then expanded.
- Fixed an issue impacting crews when incrementing the date range on a schedule board tab with many resources.
- The schedule board now scrolls when a requirement or map pin is dragged to the side.
- Fixed a bug that was impacting switching requirement panel tabs when "show default requirement panels" setting is disabled.
- Users can now switch the selected resources view in the Crew Allocation tool while resources are still loading. 
- Users can now minimize the requirement details panel in schedule assistant when no resources are displayed.
- Various accessibility enhancements.


## 3.12.148.12

**Resource Scheduling Controls:** 1.2.87.243542

**Dataverse:** 4.0.138.12

- Improved error messaging on the schedule board.
- Fixed a bug that was causing schedule assistant to open with the incorrect requirement view for some users.
- Fixed a bug that was preventing users from using the search box on schedule assistant when no resources are displayed.
- Improved crew availability logic when dealing with variable crew membership.


## 3.12.146.16

**Resource Scheduling Controls:** 1.2.85.243202

**Dataverse:** 4.0.136.16

- Fixed various time zone related bugs in schedule assistant.
- Fixed a bug causing duplicate months to appear for some users in monthly view of the schedule board.
- Fixed a bug causing incorrect dates in requirement details for some users.
- Fixed a bug causing incorrect dates to be selected when dragging the cursor in multiday views on the schedule board.
- Fixed a bug causing an error message to be displayed when double clicking on an appointment on the schedule board. 


## 3.12.145.25

**Resource Scheduling Controls:** 1.2.84.243184

**Dataverse:** 4.0.135.25

- Fixed a bug that was breaking links in appointment tooltip headers.
- Fixed a bug that was causing non-working hours visibility issues when viewing a group resource's membership on the schedule board.
- Various bug fixes surrounding the visibility of the Find Availability button.
- Updated durations in the Schedule Assistant filter pane are now respected when creating a booking. 
- Improved selection behavior of choosing slots on the schedule board. 
- Requirement pane no longer crashes when no tabs are set up.
- Fixed a bug that was impacting the booking methods presented on the booking pane.
- Improved warning logic when moving an appointment on the schedule board.
- Fixed time zones issues on the new requirement panel in Specify Pattern.


## 3.12.144.84

**Resource Scheduling Controls:** 1.2.83.243052

**Dataverse:** 4.0.134.84

> [!IMPORTANT]
> We've encountered issues with the updated schedule board that we recently released. As a result, we are temporarily disabling the updated board to address these issues before reenabling. We are fully committed to delivering this update and will communicate our plans to roll it out once the issues have been resolved.
> In the meantime, the board will revert back to its prior functionality. If you have manually installed Universal Resource Scheduling solution version 3.12.144.84, we will remotely disable the update with no further action required on your end. If you are on any other prior version of the Universal Resource Scheduling solution, there will be no change to your schedule board.

- Fixed a bug that was causing some field options to be improperly populated when using schedule assistant's booking panel.
- The Find Availability button is no longer visible when a requirement is deselected and is visible when a requirement group is selected.
- Fixed a bug where the requirement panel's active tab was not always being cached.
- Improved schedule assistant's handling of custom entities.
- Fixed bugs impacting filtering and pagination on the requirement panel of the schedule board.
- Fixed a bug that was causing some users to be unable to set a booking status on a work order in schedule assistant. 
- Fixed a bug where Specify Pattern was changing the date of some requirement details when editing a time window start.


## 3.12.143.46

**Resource Scheduling Controls:** 1.2.82.242904

**Dataverse:** 4.0.133.47

- Fixed bug that was redirecting some users to the wrong version of the schedule board.

## 3.12.143.36

**Resource Scheduling Controls:** 1.2.82.242904

**Dataverse:** 4.0.133.37

- Fixed a bug that was causing booking previews in schedule assistant to render on top of the settings panel and legend.
- We now show an error when users try to derive capacity from group members on resources that are not pools.
- Fixed a bug that was causing estimated arrival times to be set even when there were no changes.
- Fixed a bug that was sometimes causing the wrong requirement to be booked when using schedule assistant on work orders with multiple requirements.

## 3.12.142.5

**Resource Scheduling Controls:** 1.2.81.242685

**Dataverse:** 4.0.132.5

- Fixed bug that was misdirecting some users to the wrong version of the schedule board.
  
## 3.12.142.1

**Resource Scheduling Controls:** 1.2.81.242685

**Dataverse:** 4.0.132.1

- This release includes all updates from the 2024 release wave 2 early access updates.
- The relevant account for underlying bookings can now be seen on the schedule board aggregate booking by turning on a new feature. 
- Keywords in requirement search box on the schedule board are now cached when switching between tabs.
- Turning on focus mode no longer maximizes the browser.
- Fixed a bug that was causing the schedule Assistant to ignore fulfillment preferences on the initial load.
- Fixed a bug that was impacting time labels on Specify Pattern when changing time zones.
- Schedule Assistant is now using the updated schedule board. The framework underlying the schedule board has been updated, which reduces load times significantly and introduces usability improvements such a day line or tab reordering. For more information, see [The next chapter for the Schedule Board: Enhanced Usability and Performance](https://www.microsoft.com/en-us/dynamics-365/blog/it-professional/2024/10/31/the-next-chapter-for-the-schedule-board-enhanced-usability-and-performance/).
  Unsupported customizations to the schedule board, such as DOM manipulations, may be impacted or stop working. Additionally, the updated schedule board is not available in the Resource Scheduling Optimization add-in due to underlying limitations.  


## 3.12.140.11

**Resource Scheduling Controls:** 1.2.79.242513

**Dataverse:** 4.0.130.11

- Organizational Units are now displayed in alphabetical order in the schedule board filter panel.
- Improved handling of mismatched distance units in Schedule Assistant.
- Fixed a bug that was causing the Crew Allocation Tool to crash when Derive Capacity from group members was checked.
- Fixed a bug that was preventing some additional capacity rows to not expand on the Schedule Board.
  
## 3.12.139.62

**Resource Scheduling Controls:** 1.2.78.242404

**Dataverse:** 4.0.129.62

- Fixed a bug that was causing an error when deselecting resources in the booking panel.
- Fixed a bug that was causing Schedule Board zoom setting not to cache when set to 0.
- Sorting by rating value is now cached and included in saved default filters on Schedule Board tabs.

## 3.12.141.6 - 2024 Wave 2 Early Access update 2

**Resource Scheduling Controls:** 1.2.80.242331

**Dataverse:** 4.0.131.6

- No updates were made to Universal Resource Scheduling in this release.

## 3.12.138.39

**Resource Scheduling Controls:** 1.2.77.242277

**Dataverse:** 4.0.128.39

- Fixed a bug that was displaying an empty preview section on the scheduling parameter form.
- Fixed a bug that was impacting custom field mapping when bookings are created through the schedule assistant.
- Fixed a bug that was causing some input values to persist after selecting *Reset to Default* in the board settings. 
- Fixed a bug that was causing a *No results* message in the schedule assistant list view while results are still populating.
- Fixed a bug that was causing issues with validating *Time Promised* windows on the schedule board when the entity and browser time zones are different.
- Fixed a bug where the number of available hours in a day for resources were not being displayed in the Gantt view of the schedule assistant.
- Working day selections are now honored even when the date range begins on a non-working day and when switching between daily and hourly views.

## 3.12.137.22

**Resource Scheduling Controls:** 1.2.76.242082

**Dataverse:** 4.0.127.22

- Removed toggle for a feature that is not yet active.
- Various security enhancements.

## 3.12.141.2 - 2024 Wave 2 Early Access

**Resource Scheduling Controls:** 1.2.80.242082

**Dataverse:** 4.0.131.2

- Custom URLs that accessed the old schedule board are now redirected to the new schedule board preserving any relevant parameters.
  
## 3.12.137.15

**Resource Scheduling Controls:** 1.2.76.242082

**Dataverse:**  4.0.127.15

- Fixed a bug in the schedule assistant that disabled the **Book** and **Book and Exit** buttons in the create booking panel when working with resources with multiple units of capacity or set to allow overlapping bookings.
- When a resource is selected, map view on the schedule board now shows the resource's latest geolocation.
- Fixed a bug that was causing schedule assistant to ignore the **Allow Overlapping** selection.
- Fixed a bug that was causing notifications from schedule assistant to appear in the wrong location based on certain window configurations.
- Improved managed identity handling when using the msdyn_SearchResourceAvailabilityForRequirementGroup API.
- Improved requirement groups' handling of resources with multiple units of capacity.
- Fixed bug that was impacting the actual booked time slot when allow overlapping bookings is selected.


## 3.12.136.61

**Resource Scheduling Controls:** 1.2.75.241931

**Dataverse:**  4.0.126.59

- Removed toggle for a feature that is not yet active.
- Various security enhancements.
  
## 3.12.136.53

**Resource Scheduling Controls:** 1.2.75.241931

**Dataverse:**  4.0.126.51

- Fixed a bug that caused the schedule assistant to not consider additional resource capacity.
- Fixed a bug that wcaused multi-day bookings created with the schedule assistant to add an additional booking detail when booked outside the search range and an evenly distribute hours booking method. 
- Custom web resources no longer get covered when extending the map panel.
- Booking rules only run in the hourly view.
- Added a tooltip to see long values in fields.
- Improved schedule board rendering performance. 
- Improved translationa and localization.


## 3.12.135.25

**Resource Scheduling Controls:** 1.2.74.241731

**Dataverse:**  4.0.125.34

- Improved messaging when there are no schedule assistant results due to retrieval limits.
- Added "Today" label to the related icon on the schedule board.
- Users can now enter text continuously in the Crew Allocation tool's resource search bar.
- Fixed a bug where requirement groups were not being created by the system user.
- Fixed a bug that was opening the details panel when selecting a resource from the Create booking panel.
- The "Learn more" link when no results found on schedule assistant has been redirected to the appropriate documentation.
- Fixed a bug that was causing "Switch views" to not appear in the right click menu on the schedule board.
- Improved crew membership masking on the schedule board.
- Fixed a bug that was causing selected ties from schedule assistant to not be honored for requirement group bookings.
- Improved legend display on schedule board.

## 3.12.134.25

**Resource Scheduling Controls:** 1.2.73.241652

**Dataverse:** 4.0.124.25

- Fixed a problem that was causing some Schedule Board list view users to see resources erroneously marked as unavailable or available. 
- Business Closure Start Time and End Time fields have been retitled Start and End respectively.
- Resource filter panel now resets to page 1 when search for resources.
- Users are now notified when one of their booking rules is ignored because it is invalid, broken, or corrupted.
- New crew member bookings are now reflected on the SB without a manual refresh.
- Improvements to handling of capacity for requirement groups and facility resources.
- Fixed a problem where Schedule Asisstant was not returning results when one of the Time From/To Promised fields is empty. 
- Fixed a problem that was causing the Create Booking and Details panels to open in each other's place.
- Improved full-screen experience.
- Localization improvements.
- Various security enhancements.

## 3.12.132.9

**Resource Scheduling Controls:** 1.2.71.241432

**Dataverse:** 4.0.122.8

- Improved rendering for non-working hours on the schedule board.
- Fixed a bug that was causing some users to experience crashes when working hours did not start at 12 am.
- Users can now use 24-hour format to enter a time for the End Time field on the booking pane.
- Added a button to jump to today's date on the schedule board.
- Fixed a bug that was displaying incorrect travel times for some requirement group bookings.
- Various security enhancements.
- **Introduced a new tool to efficiently make single day membership changes for crews.**
- Fixed a bug that was causing the Schedule Assistant Booking Panel to malfunction when working with requirement groups.
- Fixed a bug that was causing list view in schedule board to not show availability in some circumstances.
-	Various security enhancements.



## 3.12.131.1

**Resource Scheduling Controls:** 1.2.70.241042

**Dataverse:** 4.0.121.1

- Horizontal scroll location is now maintained when switching views on the schedule board.
- List view on the schedule assistant now sorts all results instead of just the current page.
- Various tooltips have been improved.
- Fixed a bug that was cancelling all related bookings when a Project Operations user canceled a project requirement in an interday view. 
- Fixed a bug that was causing the requirement panel to crash when reordering tabs with active filters applied. 
- Fixed a bug that was mislabeling or and duplicating certain entities in the Related tab of a bookable resource form. 


## 3.12.130.10

**Resource Scheduling Controls:** 1.2.69.240991

**Dataverse:** 4.0.120.10

- Inactive organizational units are no longer displayed on the map
- Custom color setting for working/non-working hours are now used in aggregated views and the hourly view.
- Fixed a bug that prevented the selection of new some new tabs on the requirement pane. 
- Fixed a bug with syncing changes to a booking in the schedule assistant grid.
- Fixed a bug that was causing schedule board to crash when maximizing it from a very small window.
- Fixed a bug that was causing the details panel to not respect customized requirements detail view for resource type.


## 3.12.129.28

**Resource Scheduling Controls:** 1.2.68.240862

**Dataverse:** 4.0.119.28

- Fixed a bug that was preventing some users from rearranging schedule board tabs.
- Unchecked working days are no longer shown in the schedule board's list view.
- Various bug fixes to working days selection.
- Fixed a bug that was casing discrepancies between values on bookings made using the Create panel and how they were displayed in Map view.
- Requirement details are now shown properly in the Edit Booking panel. 
- Users can now change booking status in the Create Booking panel.

## 3.12.125.30

**Resource Scheduling Controls:** 1.2.64.240721

**Dataverse:** 4.0.115.30

- Fixed a bug that was disabling saved filters after a hard refresh for some users.
- Fixed a bug that was disabling the Delete button in a booking context menu in multiday views.
- Travel times of existing bookings are now updated when previous bookings are deleted.
- Booking statuses can now be updated while in multiday views in both List and Gantt modes.

## 3.12.127.12 - 2024 Wave 1 Early Access update 1

**Resource Scheduling Controls:** 1.2.66.240663

**Dataverse:** 4.0.117.12

- Users can now select which days of the week are visible on the schedule board.
- Added a vertical line to indicate current day while in aggregated views.
- Fixed bug where Move Bookings was not functioning properly in some time zones.
- Removed entry point to Schedule Board Settings from Booking Setup Metadata ribbon button.

## 3.12.124.11

**Resource Scheduling Controls:** 1.2.63.240662

**Dataverse:**  4.0.114.11

- Fixed a bug where edited search ranges were defaulting back to requirement start/end dates in Schedule Assistant.
- Improved Service Territory search box in the Select Resources panel.
- Requirement proposed and fulfilled durations now update automatically when bookings are made in Schedule Assistant.
- Fixed a bug that was impacting the Move Bookings feature for some users.
- Various security enhancements.
- Fixed a bug where double clicking on a booking was not opening the record while in the schedule board's hourly view.

**Resource Scheduling Controls:** 1.2.63.240662

## 3.12.123.34

**Resource Scheduling Controls:** 1.2.62.240661

**Dataverse:**  4.0.113.34

- Travel time calculates correctly for facility resources.
- All relevant fields now link to their respective entities in the requirements pane on the schedule board.
- The time zone setting in the schedule board settings is now reflected when moving a booking.
- Performance improvements when switching between schedule board tabs.
- Various security enhancements.
- Fixed a bug where double clicking on a booking was not opening the record while in the schedule board's hourly view.

**Resource Scheduling Controls:** 1.2.62.240661

## 3.12.126.1 - 2024 Wave 1 Early Access

**Resource Scheduling Controls:** 1.2.65.240241

**Dataverse:** 4.0.116.1

- Booking templates now feature updated colors and color picking tools.
- Fixed a bug that was impacting requirement grid column filters for some users.


## 3.12.122.50

**Resource Scheduling Controls:** 1.2.61.240223

**Dataverse:** 4.0.112.50

- Minor user experience bug fixes for requirement groups, map pins, and service territories.

## 3.12.121.18

**Resource Scheduling Controls:** 1.2.60.240112

**Dataverse:** 4.0.111.21

- Released new **Specify Pattern** version to break down long-duration or complex requirements.
- Bookings made in the Booking pane can now be set to any time granularity. 
- Fixed a bug where resources marked to not show on the schedule board were listed in the *Move to* dropdown.
- The number of child resources for pools and crews now show on the schedule board.
- Extra capacity of a resource now shows on the schedule board when available. 
- Booking rules now support HTML tags.
- The *Service territory* field on the *Select resource* filter now supports free text.

## 3.12.120.16

**Resource Scheduling Controls:** 1.2.59.233402

**Dataverse:** 4.0.110.19

- Introduced new version of the **Specify Pattern** control to break down multi-day requirements.
- Fixed a bug where users without delete permissions were shown a delete button on bookings.  
- Enabled free text in the service territory filter field.  
- Booking rules now support HTML tags on the new schedule board.
- When closing schedule assistant on the schedule board, users see their last open requirement tab.  
- The schedule board supports Internet Explorer mode of the Microsoft Edge browser. 
- Fixed a bug that caused an incorrect number of child resources to show on the schedule board for Crew and Pool resources.  
- The move option on the schedule board now respects the resource selection of the schedule board.
- Users can set specific times in the booking panel beyond the existing 15-minute granularity.

## 3.12.119.27

**Resource Scheduling Controls:** 1.2.58.232961

**Dataverse:** 4.0.109.27

- Performance improvements for API calls.
- Performance improvements when using the schedule assistant with lots of bookable resources.  
- Fixed a bug where bookings made with the schedule assistant are longer than resource's availability when search availability is manually set.  
- Fixed a bug that was causing an error message when opening the specify pattern control.
- Fixed bugs with apostrophes in requirement names and booking templates.
- PowerApps improvements with the specify pattern control.

## 3.12.118.19

**Resource Scheduling Controls:** 1.2.57.232831

**Dataverse:** 4.0.108.19

- In the map view on the schedule board, there are now visual indicators to show which record is selected. 
- Fixed a bug that was preventing some tooltips to not properly function while in list view. 
- Improved the schedule board resolution slider to honor the configured working time. 
- Fixed a bug that was displaying an error when booking certain full capacity requirements with a “Full Requirement” booking method. 
- Fixed bugs that were causing errors to be displayed when editing booking lengths in multi-day views.  

**Resource Scheduling Controls:** 1.2.57.232963

- Fixed a bug where apostrophes were shown as undefined when part of a book template name
- Fixed a bug where the Schedule Board requirements grid wasn't showing data. 

## 3.12.117.31

**Resource Scheduling Controls:** 1.2.56.232691

**Dataverse:** 4.0.107.30

- **Proportional booking visualization on aggregated schedule board views:** On daily, weekly, and monthly schedule board views, bookings are displayed as a proportion of their duration to the time block instead of filling the whole period.  
- When schedule assistant fails to create a booking, an error message now shows more information. 
- Fixed an issue that was causing the schedule board to load the wrong date when operating in specific time zones. 
- Fixed an issue that was causing selected resources to be displayed as undefined when using client extensions.  

**Resource Scheduling Controls:** 1.2.56.232963

- Fixed a bug where apostrophes were shown as undefined when part of a book template name
- Fixed a bug where the Schedule Board requirements grid wasn't showing data.  

## 3.12.112.5

**Resource Scheduling Controls:** 1.2.52.232511

**Dataverse:** 4.0.102.5

- **Capacity for resource search**: Resource search is now supported for organizations with more than 5,000 resources. 
- **Accessibility**: Implemented various accessibility improvements including increased support for screen readers, new visual labels, and more ARIA attributes. 
- Fixed an issue in the API where calling *msdyn_SearchResourceAvailability* consistently returned empty *AvailabilityIntervals* and *Characteristics*.
- Fixed an issue that led to the schedule assistant returning no available slots when a user entered information in the *Time from promised* field.  
- Fixed an issue where service territory filters were being reset when navigating through pages of a resource selection search.  

**Resource Scheduling Controls:** 1.2.52.232844
 - Various security enhancements  

## 3.12.116.5 - 2023 Wave 2 Early Access update2

**Resource Scheduling Controls:** 1.2.55.232482

**Dataverse:** 4.0.106.5

- **Retirement of the legacy schedule board:** The new schedule board is faster, more user-friendly, and accessible. It lays the foundation for new capabilities such as multiday scheduling and intelligent interactions.
- **Proportional bookings on multiday views:** Quickly determine a resource’s availability and utilization.
- **Multiple recurrences in work hours calendar:** Greater flexibility in resource scheduling, helping you meet business demands while adjusting to your workforce’s needs.
- Fixed an issue where rebooking and substituting on a requirement that got deleted was failing.
- Fixed an issue where the schedule board color wasn't being applied when saving the board setting with a new color.
- Fixed an issue where "Find Availability" in the new schedule board wasn't considering custom fields.

## 3.12.111.36

**Resource Scheduling Controls:** 1.2.51.232411

**Dataverse:** 4.0.101.36

- Fixed an issue where filtering resources by name didn't handle accented characters correctly.
- Fixed an issue where the “Time From/To Promised” fields weren't displayed during drag and drop operations on the schedule board if custom booking templates were enabled.
- Fixed an issue where the resource search bar on the schedule board was limited to the client-side records and couldn't search for all records when there were more than 5,000 resources.
- Fixed an issue where the schedule board didn't load completely after creating a new tab and switching back to the “Initial public view” tab. 
- Fixed an issue where the calendar icons on the “From” and “To” fields in the requirement group form didn't open the calendar picker. 
- Fixed several accessibility issues in the “Edit Booking Alerts Template” dialog, button labels, ARIA attributes, and screen reader compatibility.

## 3.12.110.18

**Resource Scheduling Controls:** 1.2.50.232152

**Dataverse:** 4.0.100.18

- Fixed a bug where the schedule board color wasn't applied when saving the board setting with a new color.
- Fixed a bug where the “Find Availability” feature in the new schedule board didn't consider custom fields.
- Improved accessibility for the “New Filter Layout” dialog, the “New Schedule Board Tab” button in portrait mode, and the “New Schedule Board” navigation panel.
- Fixed a bug where the schedule assistant requirement view wasn't picked up when the schedule assistant was launched from the book button.
- Fixed a bug where an incorrect “End Time” was populated on the booking custom entity when the “Default Booking Duration” had a Null value.
- Fixed a bug where an incorrect “End Time” was populated in the “Create Booking Panel” in Schedule Assistant when creating a booking for a requirement for the second time.
- Fixed a bug where the schedule board crashed when cold loading or creating a new tab in a small width window.
- Fixed a bug where the “Book & Exit” button reappeared after booking a requirement group, and it canceled the bookings.

## 3.12.114.1 - 2023 Wave 2 Early Access update1

**Resource Scheduling Controls:** 1.2.54.232001

**Dataverse:** 4.0.101.1

**Work hours calendar supports multiple recurrences**: Previously, you could only have one work hour recurrence per resource. With the added capability of multiple recurrences, you can now unlock greater flexibility in your resource scheduling to meet business demands further while adjusting to the needs of your workforce for employee retention and job satisfaction.

