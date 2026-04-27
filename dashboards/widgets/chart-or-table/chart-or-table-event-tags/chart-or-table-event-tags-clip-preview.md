# Event tag clip preview

When you select a data point in an Event tags chart, Lumana opens the Event tag records view for that period. Selecting a clip from that view opens the clip preview window, so you can review the video footage, navigate between events, and manage archives.

This page covers everything available in the clip preview window. To get here, follow the steps in [Event tags](/broken/pages/Dsi4oiK829G9U1zTaJuJ) first.

## Review the clip

The clip preview window opens with three tabs: **Images**, **Video**, and **Objects**. Each tab shows the same clip from a different angle.

<div align="center" data-with-frame="true"><img src="../../../../.gitbook/assets/widget-event-tags-clip-preview-images-tab.png" alt="" width="563"></div>

* **Images**: Shows still frames captured during the event. Use **Previous captured image** and **Next captured image** to step through each frame.
* **Video**: Shows continuous video for the event segment. Includes a playback speed control so you can watch at a faster or slower rate.
* **Objects**: Shows detected objects associated with the clip.

<div align="center" data-with-frame="true"><img src="../../../../.gitbook/assets/widget-event-tags-clip-preview-video-tab.png" alt="" width="563"></div>

The preview updates as you move the timeline on either the Images or Video tab.

## Navigate between events

A shared control bar sits below the viewer on all three tabs.

<div align="center" data-with-frame="true"><img src="../../../../.gitbook/assets/widget-event-tags-clip-playback-controls.png" alt="" width="222"></div>

* **Previous alert** and **Next alert**: Move to the previous or next event in the records list.
* **Play**: Starts video playback. If you're on the Images tab, then selecting Play switches to the Video tab and begins playing. While playing, the same control acts as Pause.
* **Previous captured image** and **Next captured image**: Step backward or forward through the still frames captured for the current event.

## Adjust the view

A floating toolbar appears over the feed with controls for adjusting the view.

<div align="center" data-with-frame="true"><img src="../../../../.gitbook/assets/widget-event-tags-clip-overlay-zoom-snapshot-fullscreen.png" alt="" width="317"></div>

* **Zoom out**, **Reset zoom**, **Zoom in**: Adjust how close you are to the picture. Reset zoom returns to the default framing.
* **Snapshot**: Saves the current frame to your device as a PNG file.
* **Fullscreen**: Expands the viewer to fill the screen.

## Save an archive, add cameras, and change the layout

The toolbar on the right side of the tab row gives you three additional controls.

<div align="center" data-with-frame="true"><img src="../../../../.gitbook/assets/widget-event-tags-clip-preview-images-icons.png" alt="" width="563"></div>

* **Create archive**: Opens the Create archive dialog.

<div align="center" data-with-frame="true"><img src="../../../../.gitbook/assets/widget-event-tags-clip-create-archive.png" alt="" width="563"></div>

Fill in the dialog:

* **Name**: Enter a name for the archive.
* **From** and **To**: Set the time range for the segment. The fields pre-populate based on the clip. Select either field to open the date and time picker. Choose a date from the calendar, then set the hour, minute, and second using the scrollers. Select **Done** to apply.

<div align="center" data-with-frame="true"><img src="../../../../.gitbook/assets/widget-event-tags-clip-archive-date-picker.png" alt="" width="563"></div>

**Duration**: The length of time between the **From** and **To** values. \
**Add to case**: Link the archive to a case. Search for an existing case by name, select \*\*+ Create\*\* to create a new case, or select **Manage** to open the Cases page in Lumana.

Selecting **+ Create** opens the Create case dialog.

<div align="center" data-with-frame="true"><img src="../../../../.gitbook/assets/widget-event-tags-clip-create-case.png" alt="" width="563"></div>

Fill in the required fields (marked with \*):

* **Case Name**: The name of the case, for example "Warehouse break-in" or "PPE violation north entrance."
* **Description**: A summary of what the case covers, for example "Unauthorized access detected at the north entrance on March 31 at 3:47 PM."
* **Case start time**: The date and time the incident began, for example "2026-03-31 15:47 WAT."
* **Case end time**: The date and time the incident ended, for example "2026-03-31 16:00 WAT."
* **Address**: The location where the incident occurred, for example "123 Main Street, Warehouse A."
* **Category**: The category that determines the retention period for the case and all its data.

{% hint style="warning" %}
The retention period is set when the case is created and cannot be changed afterward. When the retention period ends, the case and all related data are permanently deleted.
{% endhint %}

The following fields are optional:

* **Record number**: An internal reference number for the case, for example "INC-2026-0341."
* **External incident number**: A reference number from an external system, for example "POL-4821."
* **Tags**: Labels you can attach to the case for filtering, for example "ppe-violation" or "unauthorized-access."
* **Protected from deletion**: Select this checkbox to prevent the case from being deleted.

Select **Save** to create the case. Lumana returns you to the Create archive dialog with the new case selected. Select **Create** to save the archive.

* **Choose cameras**: Opens the Choose cameras dialog. Search by name or location, select individual cameras or **All cameras**, then select **Select** to add feeds to the preview.

<div align="center" data-with-frame="true"><img src="../../../../.gitbook/assets/widget-event-tags-clip-choose-cameras.png" alt="" width="563"></div>

* **Change layout**: Opens the layout picker with options for 1, 2, 3, 4, 6, or 9 tiles. Select a layout to show one camera full screen or view multiple feeds in a grid. Empty tiles show **Select camera** until you assign a feed to them.

<div align="center" data-with-frame="true"><img src="../../../../.gitbook/assets/widget-event-tags-clip-change-layout.png" alt="" width="563"></div>

## View multiple cameras

After adding cameras and selecting a multi-tile layout, you can view several feeds at the same time. Each tile shows a different camera, and all tiles share the same timeline and playback controls.

<div align="center" data-with-frame="true"><img src="../../../../.gitbook/assets/widget-event-tags-clip-multi-camera-view.png" alt="" width="563"></div>

## Resume a paused video

If a video feed has been idle for a while, then Lumana shows a short countdown before pausing to reduce bandwidth use. Select **Keep playing** to continue or **Pause video** to stop. After playback stops, a **Resume video** button appears on the tile. Select it to restart the feed.

|                              **Countdown before pause**                              |                                 **Resume playback**                                 |
| :----------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------: |
| ![](../../../../.gitbook/assets/widget-event-tags-clip-video-inactivity-warning.png) | ![](../../../../.gitbook/assets/widget-event-tags-clip-video-inactivity-paused.png) |
