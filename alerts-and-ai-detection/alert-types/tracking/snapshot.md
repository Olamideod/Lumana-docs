# Snapshot

Snapshot captures a still image from a zone at a regular interval you configure.

## How it works

Set an interval and draw a zone on the camera frame. Lumana captures a still image from the zone at the configured frequency.

## Configure the alert

1. Select the **bell icon** in the navigation bar. The Alerts monitoring view opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/alerts-monitoring-view1.png" alt="" width="563"></div>

2. Select **Add alert** in the top right corner. The Configure alerts page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/alerts-configure-page.png" alt="" width="563"></div>

3. Under **Tracking**, select **Use template** on the **Snapshot** card. The Create snapshot page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/snapshot-template.png" alt="" width="563"></div>

4. Enter a name in the **Alert name** field, for example "Entrance hourly check" or "Storage area snapshot."
5. Set the interval in the **every** field. Select **−** or **+** to adjust the value, or enter a value directly.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/proximity-counter.png" alt="" width="242"></div>

6. Select the **minutes** field and choose **seconds**, **minutes**, or **hours**.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/tampering-duration.png" alt="" width="242"></div>

7. Select the **zone** field to open the Choose cameras modal. Select the camera you want to monitor, then select **Select** to confirm.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-camera-picker.png" alt="" width="375"></div>

After selecting a camera, draw a zone on the camera frame. Select the **edit icon** next to the camera name to open the Select region of interest dialog.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-zone-drawing.png" alt="" width="563"></div>

Select points on the camera feed to define the zone boundary. Each point connects to the next with a green line. When the polygon is closed, the enclosed area fills with a green overlay indicating the active zone.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/snapshot-zone-complete.png" alt="" width="563"></div>

Use the navigation icons below the camera feed to review previous captures while drawing the zone:

* <img src="../../../.gitbook/assets/snapshot-nav-previous.png" alt="" height="18"> **Previous**: Shows the most recent previous capture from this alert.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/snapshot-previous-capture.png" alt="" width="563"></div>

* <img src="../../../.gitbook/assets/snapshot-nav-next.png" alt="" height="18"> **Next**: Returns to the current view. This icon only appears after at least one capture exists.

* **Exclude**: Toggle on to invert the zone. Lumana captures the area outside the drawn zone instead of inside it.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/snapshot-zone-invert.png" alt="" width="563"></div>

* **Reset**: Clears all points and lets you start over.
* **Select**: Confirms the zone and closes the dialog.

8. Select the **time** field to set when the alert is active. [Configure alerts](../../configure-alerts.md#schedule) covers the schedule options.
9. Optionally, select **default configuration** to adjust display settings, confidence level, priority, blocking period, and alert message. [Configure alerts](../../configure-alerts.md#default-configuration) covers these settings.
10. Select **Then** <img src="../../../.gitbook/assets/alert-then.png" alt="" height="18"> to choose the action Lumana takes when the alert triggers. [Alert actions](../../alert-actions.md) covers the available actions.
11. Select **Create alert** in the top right corner. The alert is saved and becomes active immediately.
