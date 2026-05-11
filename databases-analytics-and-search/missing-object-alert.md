# Create a Missing object alert

The **Missing object** alert notifies you when a marked object is no longer visible in the camera view you monitor. That helps you catch removals or theft sooner and reduces the need for constant manual checks of the same scene.

## Why this alert helps


- **Real-time detection**: You get instant alerts when the object disappears, so you respond sooner instead of scrubbing footage later.
- **Automated tracking**: The system watches the marked region for you, so you rely less on manual checks of the same view.
- **Security enforcement**: Detects unauthorized removals or theft of equipment or inventory in the region you marked.
- **Operational continuity**: Helps confirm that critical items stay in place during the hours you monitor.

## Prerequisites

Make sure you can open **Alerts** and create alert rules. You need a camera that shows the object clearly enough to mark it in the frame, and permission to choose notification actions in the **Then** step.

## Configure the alert

1. In the left sidebar, select **Alerts** <img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-alert-icon.png" alt="Alerts bell icon in the sidebar." data-size="line">.

2. Select **Add alert**.

   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-alerts-monitoring-add-alert.png" alt="Alerts Monitoring with Alerts in the sidebar and Add alert in the toolbar." width="563"></div>

3. Under **Identification**, find the **Missing object** template and select **Use template**.

   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-missing-object-template.png" alt="Configure alerts with Identification selected and Missing object Use template highlighted." width="563"></div>

4. On the rule builder, enter an **Alert name** if you want. In the sentence, open the schedule link (for example **all times**) and **[default configuration]** when you need to change those values.


5. Select **[cameras]** in the sentence. In the chooser, select the camera (or cameras) that should watch the object.

   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-choose-cameras-edit.png" alt="" width="563"></div>

6. Select **Then** and choose what happens when the alert fires, for example notify someone.

   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-missing-object-alert-config.png" alt="" width="563"></div>


7. Select the pencil icon <img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-edit-pencil-icon.png" alt="Pencil icon to edit object region." data-size="line"> next to the camera so you can mark the object the alert should track.

   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-mark-object-dialog.png" alt="" width="375"></div>

8. In the **Mark object** dialog, outline the object, then select **Select**.

9. When the rest of the rule is complete, select **Create alert** <img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-create-alert-button.png" alt="Create alert button." data-size="line">.

   After you save, the alert runs when the marked object leaves the monitored region and is no longer visible as configured.

## Review alerts in monitoring

When the alert fires, it appears in the monitoring view with a still, time, location, and actions such as acknowledge, play, and share.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-missing-object-alert-monitoring-example.png" alt="Monitoring view with a Missing object alert card and action buttons." width="563"></div>

Select the alert to open a video clip or image for that event.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-missing-object-video-preview.png" alt="Alert preview with Video tab and playback controls." width="563"></div>

From the preview, you can save footage to the archive with the archive icon <img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-archive-icon.png" alt="Archive icon." data-size="line">, or use **Share** <img src="../.gitbook/assets/databases-analytics-and-search/custom-objects-share-icon.png" alt="Share icon." data-size="line"> to share the clip according to your organization's policy.

## Next steps

- Open **Alerts** and **Configuration** when you need to edit or disable the rule.
- Use [Share video](../live-video-monitoring-and-operations/share-video.md) for more detail on sharing options and access controls.
