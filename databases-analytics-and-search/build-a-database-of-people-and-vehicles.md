# Build a database of people and vehicles

Use the organization database to organize detected people, doors, and vehicles into a searchable list your team can manage over time. You can also use Event Tags to attach structured external data to video and import vehicle lists in bulk when you need faster setup.

## Prerequisites

Make sure you can open the organization database and edit the people, doors, or vehicles you want to manage. If you plan to use Event Tags or import vehicles from a CSV file, then confirm you have access to those features in your organization.

## Understand the organization database

The organization database stores detected items that Lumana has already identified in your environment. This gives your team one place to review people, doors, vehicles, and event-related data.

People and vehicles can move from detected items into a maintained database entry with names, groups, and other identifying details. Groups work in a similar way across the directory, so once you understand the group workflow for people, the same pattern applies elsewhere.

## Manage people profiles and groups

Use the people directory to review detected faces, save profiles, and organize people into groups.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/people-directory-profiles.png" alt="Organization database people directory showing unsaved people, saved profiles, and search controls." width="563"></div>

Unsaved people are recognitions waiting to be added as known people. Saved profiles contain the recognitions you have assigned to a person. You can also create a profile by uploading an image of that person's face.

### Create a group

Create groups when you need to organize people into reusable sets for review or workflow purposes.

1. In the people directory, select **Create group**.

   The group creation dialog opens.

   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/people-directory-groups.png" alt="" width="563"></div>

2. Enter a group name.

3. Select the profiles to include.

   The dialog shows the selected people before you finish.

   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/create-group-dialog.png" alt="" width="375"></div>

4. Select **Create**.

   You can later hover over the group to edit or delete it.

   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/people-groups-table-edit-delete.png" alt="" width="375"></div>

## Use doors in the database

Use the doors section to store doors seen on camera so you can work with them later in alerting workflows. Once a door is in the database, you can use it with alerts such as [Door state change](../alerts-and-ai-detection/alert-types/security/door-state-change.md).

## Add vehicles to the database

Use the vehicles directory to review detected vehicles, save known vehicles, and maintain a list your team can reuse in alerts and investigations.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/vehicles-directory-vehicles.png" alt="" width="563"></div>

Vehicles seen on camera appear in the detected list. **Existing vehicles** are the saved records your team maintains over time.

### Add a vehicle with Add manually

Use **Add manually** when you want to type owner and vehicle details (for example after you choose **Add vehicles** on the vehicles page).

1. Select **Add vehicles**, then **Add manually**.

   The **Add manually** dialog opens.

2. Enter **Car owner's name** and **License plate**.

3. Choose **Vehicle make** from the list and select **Vehicle color** (for example a color swatch).

    <div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/vehicle-seen-validation-dialog.png" alt="" width="375"></div>

4. Select **Add**.

   The vehicle is added to your organization's saved vehicle list.

### Add a vehicle from a detection

Add a vehicle from a detection when Lumana has already captured the plate and vehicle details from camera footage, and the product sends you through the save flow from **Vehicles seen on camera** or the unsaved list.

1. Select the vehicle row you want to save.

2. Complete any fields the save dialog shows (owner, plate, make, color), then confirm to add it to **Existing vehicles**.

## Import vehicles from a CSV file

Use CSV import when you need to add many vehicles at once instead of entering them one by one.

1. In the vehicles directory, open **Vehicles**.
2. Select **Add from file** (next to **Add vehicles**).

   The **Add vehicles** dialog opens. You can drag and drop a CSV (accepted types and size limits appear in the dialog), use **Or upload from your computer**, or **Download template** to match the required columns.

   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/vehicle-manual-upload-form.png" alt="" width="375"></div>

3. When you use the template, enter the vehicle data in the CSV locally.

4. Upload the completed CSV in the importer, then select **Done** when the import finishes.

   The import adds vehicles to the organization database in bulk.

{% hint style="info" %}
If you are creating a license plate alert, you can also select **Import from file** in the alert flow to reuse the same CSV pattern while you configure [License plate recognition](../alerts-and-ai-detection/alert-types/identification/license-plate.md).
{% endhint %}

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/license-plate-import-from-file-dialog.png" alt="" width="375"></div>

## Use Event Tags

Use Event Tags when you want to attach structured external data to video, such as access control events, point-of-sale records, or warehouse scan data. This makes those events searchable alongside camera footage and helps your team add more context to investigations.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/event-tag-configuration-fields.png" alt="" width="563"></div>

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/organization-database-event-tags.png" alt="" width="563"></div>

To create and manage Event Tags, read [Add Lumana Event Tags to your video data](enhance-your-video-data-with-lumana-event-tags.md).

## Next steps

After you organize your database, you can continue with related search and alert workflows.

* Use [Search video footage for people or vehicles](search-video-footage-for-people-or-vehicles.md) to review results from saved profiles and vehicles.
* Read [Add Lumana Event Tags to your video data](enhance-your-video-data-with-lumana-event-tags.md) to connect external systems to video.
* Use [License plate recognition](../alerts-and-ai-detection/alert-types/identification/license-plate.md) to create alerts from saved vehicle lists.
