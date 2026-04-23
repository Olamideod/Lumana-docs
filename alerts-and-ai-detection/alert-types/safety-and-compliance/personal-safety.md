# Personal safety

Personal safety detection triggers when workers are too close to a vehicle on a camera for longer than a duration you set.

## How it works

Lumana monitors the camera feed for workers in close proximity to vehicles. When that proximity persists for longer than a duration you set, the alert triggers.

## Configure the alert

1. Select the **bell icon** in the navigation bar. The Alerts monitoring view opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/alerts-monitoring-view1.png" alt="" width="563"></div>

2. Select **Add alert** in the top right corner. The Configure alerts page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/alerts-configure-page.png" alt="" width="563"></div>

3. Under **Safety and compliance**, select **Use template** on the **Personal safety** card. The Create personal safety page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/personal-safety-template.png" alt="" width="563"></div>

4. Enter a name in the **Alert name** field, for example "Forklift proximity alert" or "Vehicle pedestrian warning."
5. Select the **camera** field to open the Choose cameras modal. Select the cameras you want to monitor, then select **Select** to confirm.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-camera-picker.png" alt="" width="375"></div>

6. Set the duration in the **for more than** field. Select **−** or **+** to adjust the value, or enter a value directly.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/proximity-counter.png" alt="" width="242"></div>

7. Select the **seconds** field and choose **seconds**, **minutes**, or **hours**.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/tampering-duration.png" alt="" width="242"></div>

8. Select the **time** field to set when the alert is active. [Configure alerts](../../configure-alerts.md#schedule) covers the schedule options.
9. Optionally, select **default configuration** to adjust display settings, confidence level, priority, blocking period, and alert message. [Configure alerts](../../configure-alerts.md#default-configuration) covers these settings.
10. Select **Then** <img src="../../../.gitbook/assets/alert-then.png" alt="" height="18"> to choose the action Lumana takes when the alert triggers. [Alert actions](../../alert-actions.md) covers the available actions.
11. Select **Create alert** in the top right corner. The alert is saved and becomes active immediately.
