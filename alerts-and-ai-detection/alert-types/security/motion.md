# Motion

The Motion alert triggers when Lumana detects movement within a camera's view. Use it as a baseline alert for spaces where any activity outside normal hours is a security concern.

## How it works

Lumana analyzes the video feed continuously and triggers the alert when movement exceeds the sensitivity threshold you set. You can restrict detection to a specific zone within the frame or apply it to the entire camera view. If no zone is drawn, then any movement across the full frame triggers the alert.

Drawing a detection zone reduces false positives in busy environments where only a portion of the frame needs monitoring.

## Configure the alert

1. Select the **bell icon** in the navigation bar. The Alerts monitoring view opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/alerts-monitoring-view1.png" alt="" width="563"></div>

2. Select **Add alert** in the top right corner. The Configure alerts page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/alerts-configure-page.png" alt="" width="563"></div>

3. Under **Security**, select **Use template** on the **Motion** card. The Create motion page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-template.png" alt="" width="563"></div>

4. Enter a name in the **Alert name** field, for example "After-hours motion" or "Warehouse perimeter."
5. Select the sensitivity value in the alert rule sentence. A slider opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-sensitivity-slider.png" alt="" width="242"></div>

Drag the slider to set the motion sensitivity threshold. The range is 0 to 100 and the default is 50. A higher value requires more significant movement before the alert triggers, which reduces false positives. A lower value makes the alert more sensitive to subtle movement.

6. Select the **camera** field to open the Choose cameras modal. Select the cameras you want to monitor and select **Select** to confirm.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-camera-picker.png" alt="" width="375"></div>

After selecting a camera, you can optionally draw a detection zone to limit motion detection to a specific area of the frame. Select the **edit icon** next to the camera name to open the Select region of interest dialog.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-zone-drawing.png" alt="" width="563"></div>

Select points on the camera feed to define the zone boundary. Each point connects to the next with a green line. When the polygon is closed, the enclosed area fills with a green overlay indicating the active detection zone.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-zone-complete.png" alt="" width="563"></div>

* **Exclude**: Toggle on to invert the zone. Motion outside the drawn area triggers the alert instead of motion inside it.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-zone-invert.png" alt="" width="563"></div>

* **Reset**: Clears all points and lets you start over.
* **Select**: Confirms the zone and closes the dialog.

If you do not draw a zone, motion anywhere in the full camera frame triggers the alert.

7. Select the **time** field to set when the alert is active. [Configure alerts](../../configure-alerts.md#schedule) covers the schedule options.
8. Optionally, select **default configuration** to adjust display settings, confidence level, priority, blocking period, and alert message. [Configure alerts](../../configure-alerts.md#default-configuration) covers these settings.
9. Select **Then** <img src="../../../.gitbook/assets/alert-then.png" alt="" height="18"> to choose the action Lumana takes when the alert triggers. The available actions are covered in [Alert actions](../../alert-actions.md).
10. Select **Create alert** in the top right corner. The alert is saved and becomes active immediately.
