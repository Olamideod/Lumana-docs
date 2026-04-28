# Video walls and shared displays

Use video walls and shared displays to monitor multiple cameras on one screen, combine live cameras with alerts, and share selected views with other viewers. Lumana supports saved walls for ongoing monitoring, quick live view walls for fast temporary layouts, and shared external video walls for secure external access.

## Before you begin

Make sure you can access the cameras and locations you want to display. If you plan to create a shared external video wall, you'll also need access to API keys and camera IDs.

## Choose the right wall type

Choose the wall type based on how long you need the layout and who needs to view it.

* **Saved walls:** Use a saved wall when you need a reusable layout with camera tiles, alert tiles, and alert filtering.
* **Quick live view:** Use **Quick live view** when you need a temporary wall quickly and may want to save it later.
* **Shared external video wall:** Use a shared external video wall when you need a secure URL for viewers outside Lumana.
* **Standard camera and alert tiles:** Use standard camera tiles and alert tiles when you need to combine live monitoring with event visibility in the same wall.
* **Advanced alert tile:** Use the advanced alert tile when you want alerts to stream directly to the video wall without extra clicks.

## View and edit walls

Use the **Walls** page to open existing walls and make changes to saved layouts.

1.  Open **Walls**.

    The wall list shows the walls available in your organization.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/video-walls-list.png" alt="Walls list and quick live view button."></div>

2.  Click a wall to open it.

    A wall can show multiple live camera tiles, alert tiles, or both in the same layout.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/video-wall-example.png" alt="Video wall with camera and alert tiles."></div>

3.  Hover over the wall you want to change and click the pencil icon.

    Editing lets you change the wall layout, update individual tiles, and save the revised wall.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/video-wall-editing-view.png" alt="Wall editing view."></div>

4. Click the pencil icon on a tile to replace that tile with a different camera.
5. Use the upper-right controls to change the layout, adjust alert settings and filters, delete the wall, discard changes, or save changes.

## Create a wall

Create a saved wall when you need a reusable layout for ongoing monitoring.

1. On **Walls**, click **Create wall**.
2. Enter a wall name and choose a layout that fits the number of cameras or alert tiles you want to show.
3.  Open **Cameras & alerts** to add camera tiles and alert tiles.

    Alert tiles help you monitor real-time events without opening a separate view.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/video-wall-cameras-and-alerts-tab.png" alt="Cameras and alerts tab."></div>

4.  Open **Alert view settings** to choose how alerts appear on the wall.

    You can position the alert list, choose display and picture-in-picture options, set the view duration, and enable alert sound.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/video-wall-alert-view-settings.png" alt="Alert view settings."></div>

5.  Configure alert filtering to choose which alerts appear on the wall.

    You can filter by location, camera, and priority so the wall only shows the events that matter to your team.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/video-wall-alert-filtering.png" alt="Alert filtering panel."></div>

6. Click **Done**, then click **Create**.

## Create a quick live view wall

Use **Quick live view** when you need a temporary wall without building a full saved wall first.

1. On **Walls**, click **Quick live view**.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/video-wall-quick-live-view-button.png" alt="Quick live view button."></div>

2.  Select the cameras you want to display, then click **Select**.

    Quick live view is useful when visibility matters immediately and you need to open a wall fast.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/video-wall-select-cameras-dialog.png" alt="Select cameras dialog."></div>

3. Review the temporary wall.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/video-wall-quick-live-view-example.png" alt="Quick live view wall example."></div>

4. Use the upper-right controls to open full-screen mode, adjust the settings, or save the wall.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/video-wall-quick-live-view-toolbar.png" alt="Quick live view toolbar."></div>

5. Save the wall if you want it to appear in your wall list later.

Quick live view walls also use the same live view controls available in [Use live view](live-view.md).

## Create a shared external video wall

Use a shared external video wall when you need a secure, video wall URL for external viewers. No app installation or login is required, and access is controlled through a token in the generated URL.

Create the API token, collect the camera IDs, choose the display options, and then build the shared wall URL.

1. In **Settings**, click **Organization Settings**, and then click **API Keys**.
2. Click **Create API Key**.
3.  Copy the generated token.

    You will use this token in the shared video wall URL.
4. Open **Edit Camera** for each camera you want to include, then copy the camera ID for each selected camera.
5.  Choose the video quality and decide whether to show camera names in the shared wall.

    Use one of the following resolution values:

    * `0` = standard quality (SQ)
    * `1` = medium quality (MQ)
    * `2` = high quality (HQ)

    Higher resolution improves clarity but increases bandwidth usage. To show camera names, add `cameraNames=1` to the URL. This is useful when you share the wall with viewers who are unfamiliar with camera placements.
6.  Build the shared video wall URL with the following format:

    ```
    https://external-walls.lumana.ai/live-view-wall.html?resolution=<0|1|2>&cameraNames=1&cameraIds=<CAMERA_ID1>,<CAMERA_ID2>&token=<YOUR_API_TOKEN>
    ```

    For example:

    ```
    https://external-walls.lumana.ai/live-view-wall.html?resolution=1&cameraNames=1&cameraIds=<CAMERA_ID1>,<CAMERA_ID2>&token=<YOUR_API_TOKEN>
    ```

    Use these parameters:

    * `resolution=...` sets the video quality. For example, `resolution=1` uses medium quality.
    * `cameraNames=1` shows camera names.
    * `cameraIds=...` lists the selected camera IDs, separated by commas.
    * `token=...` uses your API token to secure access.

## Next steps

After you create or share a wall, you can continue with related live monitoring tasks.

* Use [Use live view](live-view.md) to work with player controls and thumbnails.
* Read [Understand live view streaming and quality](understand-live-view-streaming-and-quality.md) to understand how live video delivery and quality selection work.
