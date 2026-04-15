# Build a database of people and vehicles

# Directory

Introducing your organization’s directory in Lumana. Here you have a collection of the Faces, doors and vehicles that have been detected at your organization. You can organize this collection of detected objects by applying data - making it your database! Additionally, you will find Event Tags here. Event Tags enables you to enrich video footage with useful data to assist your team with critical operations. More on Event Tags here [link]



## People Directory 
Your people directory contains Faces that have been detected at your organization. You can assign a profile facial recognition, upload an image to create a profile and designate groups for people at your location(s).

### Profiles

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/people-directory-profiles.png" alt="Organization database, People directory Profiles: people seen on cameras, search, and existing profile cards."></div>

**Unsaved people**
Under unsaved people are the recognitions waiting to be added as a known person. You can find them under the People seen on camera section.

**Saved profiles within your database**

Profiles contain the collection of recognitions you have assigned to a person. Note you can also add a person by uploading an image of their face. See [Working with Lumana Faces](https://support.lumana.ai/hc/en-us/articles/13972302272658) for more information on how to manage Faces.

 

### Groups
Under groups, Luman enables your team to organize the individuals at your organization further by adding profiles to unique groups.

*Notice: Groups works similarly for all items in your Directory*.

### Create a new group
Step 1: Select create group

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/people-directory-groups.png" alt="People directory Groups: search, Create group, and group list with member counts."></div>

Step 2: Give your group a name & select the relevant profiles to be added

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/create-group-dialog.png" alt="Create a group dialog with group name field, search people list, and Create button."></div>

Step 3: Hover over your group to Edit or Delete

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/people-groups-table-edit-delete.png" alt="Groups table with group names, member counts, and edit and delete actions on a row."></div>

## Doors Directory

### Doors
Any doors seen on camera can be added to your organization's database and used to configure door detection alerts. In this case, your team can activate an alert to trigger when a door is left open for a certain period of time. First, you add the door to the database. Then configure a Door Detection alert.




## Vehicles Directory

### Vehicles
Lumana’s Vehicle directory takes license plate recognition to the next level!

All vehicles detected by license plate on cameras at your organization will be collected here. Similar to people, you can create a database of specific vehicles.

 

**Vehicles seen on camera**
All images collected of any vehicle seen on camera will be collected here.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/vehicles-directory-vehicles.png" alt="Vehicles directory: vehicles seen on cameras, search, Add manually, and existing vehicles table."></div>

**List of existing vehicles**
By choosing a vehicle that has been detected on screen, you can add a useful identifying data to create a list of existing vehicles within your organization. 

 

Add vehicle to existing directory
Step 1: Click on the vehicle icon in your ‘Vehicles seen on cameras’ list

Step 2: Provide the name of owner and verify all data

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/vehicle-seen-validation-dialog.png" alt="Seen dialog to complete vehicle validation with owner name, license plate, make, color, and Add."></div>

Step 3: Click ‘Add’

Step 4: You can also add a vehicle manually by uploading an image and filling in the relevant details.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/vehicle-manual-upload-form.png" alt="Manual add vehicle: drag-and-drop image upload, accepted file types, and Vehicle name field."></div>

You’re all set! You’ve added a vehicle to your organization’s database.

 

## Event Tags
Event Tags enables users to integrate and utilize data from various external systems, on-premise or from the cloud. This feature empowers your team with advanced context based video search.

Here is where you create Event Tags for your organization in a few easy steps:

1. Generate your Public API Key Token
2. Setup Event Tag

   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/event-tag-configuration-fields.png" alt="Event tag setup: name, video length, custom fields with types, and Save event tag."></div>

3. POST Event data

   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/organization-database-event-tags.png" alt="Organization database Event tags: Create event tag, tag count, and table with name and Event type ID."></div>

For the full article on creating and managing Event Tags see [Enhance Your Video Data with Lumana Event Tag](https://support.lumana.ai/hc/en-us/articles/15928683380114).

A new feature is now available, allowing users to upload a CSV file containing a list of vehicles to the database. By clicking "Add File," users can download a template, input vehicle data, and upload the completed list back to Lumana’s database. This functionality is also accessible during alert creation.

This feature enables customers to efficiently upload multiple vehicles in bulk, either to trigger alerts or exclude them from alerting when entering the property.

 

## Alert creation upload 
When creating a license plate alert, click on the list and select "Import from File" to upload a CSV file.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/license-plate-import-from-file-dialog.png" alt="License plate dialog with Vehicle name and License plate columns, Add, Import from file, and Done."></div>

### DataBase Update 
Under **Organisation** → **Database** → **Vehicles Directory** → **Vehicles**, click the <img src="../.gitbook/assets/databases-analytics-and-search/add-from-file-button.png" alt="Add from file" style="display:inline-block;vertical-align:middle;max-height:1.85em;width:auto;"> button to upload your CSV file.