# Create a Missing object alert

The **Missing object** alert notifies you when a marked object is no longer visible in the camera view you monitor. That helps you catch removals or theft sooner and reduces the need for constant manual checks of the same scene.

## Why this alert helps

- **Faster response:** You get a notification when the object disappears instead of scrubbing footage later.
- **Less manual watching:** The system watches the marked region for you.
- **Security and loss prevention:** You can detect unauthorized removal of equipment or inventory.
- **Operational checks:** You can confirm that critical items stay in frame during business hours or after hours.

## Before you begin

Make sure you can open **Alerts** and create alert rules. You need a camera that shows the object clearly enough to mark it in the frame, and permission to choose notification actions under **Then do this**.

## Configure the alert

1. In the left sidebar, click **Alerts** <img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-alert-icon.png" alt="Alerts bell icon in the sidebar." height="18">.

2. Click **Add alert**.

   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-alerts-monitoring-add-alert.png" alt="Alerts Monitoring with Alerts in the sidebar and Add alert in the toolbar." width="900"></div>

3. Under **Identification**, find the **Missing object** template and click **Use template**.

   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-missing-object-template.png" alt="Configure alerts with Identification selected and Missing object Use template highlighted." width="900"></div>

4. Set when the rule runs, for example **All times**, so object detection follows the schedule you need.

5. Click **Then do this** and choose what happens when the alert fires, for example notify someone.

   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-missing-object-alert-config.png" alt="Missing object alert form with rule text, Then do this, and camera fields." width="720"></div>

6. Click **Cameras** and select the camera (or cameras) that should watch the object.

   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-choose-cameras-edit.png" alt="Choose cameras dialog with camera list and pencil icon to mark the object." width="900"></div>

7. Click the pencil icon <img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-edit-pencil-icon.png" alt="Pencil icon to edit object region." height="18"> next to the camera so you can mark the object the alert should track.

   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-mark-object-dialog.png" alt="Mark object dialog with polygon on the object and Select button." width="720"></div>

8. In the **Mark object** dialog, outline the object, then click **Select**.

9. When the rest of the rule is complete, click **Create alert** <img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-create-alert-button.png" alt="Create alert button." height="32">.

   After you save, the alert runs when the marked object leaves the monitored region and is no longer visible as configured.

## Review alerts in monitoring

When the alert fires, it appears in the monitoring view with a still, time, location, and actions such as acknowledge, play, and share.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-missing-object-alert-monitoring-example.png" alt="Monitoring view with a Missing object alert card and action buttons." width="900"></div>

Click the alert to open a video clip or image for that event.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-missing-object-video-preview.png" alt="Alert preview with Video tab and playback controls." width="900"></div>

From the preview, you can save footage to the archive with the archive icon <img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-archive-icon.png" alt="Archive icon." height="18">, or use **Share** <img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-share-icon.png" alt="Share icon." height="18"> to share the clip according to your organization's policy.

## Next steps

- Open **Alerts** and **Configuration** when you need to edit or disable the rule.
- Use [Share video](../live-video-monitoring-and-operations/share-video.md) for more detail on sharing options and access controls.
