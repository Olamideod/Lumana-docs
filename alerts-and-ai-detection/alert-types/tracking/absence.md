# Absence

Absence detection triggers when no objects of a configured type are detected on a camera for longer than a duration you set.

## How it works

Set the object types to monitor and a minimum absence duration. Lumana monitors the camera feed and triggers the alert when no objects of the configured type are detected for longer than that duration.

## Configure the alert

1. Select the **bell icon** in the navigation bar. The Alerts monitoring view opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/alerts-monitoring-view1.png" alt="" width="563"></div>

2. Select **Add alert** in the top right corner. The Configure alerts page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/alerts-configure-page.png" alt="" width="563"></div>

3. Under **Tracking**, select **Use template** on the **Absence** card. The Create absence page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/absence-template.png" alt="" width="563"></div>

4. Enter a name in the **Alert name** field, for example "Security post unstaffed" or "Parking lot empty."
5. Select the **objects** field in the alert rule sentence. A dropdown opens with the available object types.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/proximity-objects-dropdown.png" alt="" width="262"></div>

Select one or more object types to monitor:

* **people**: Detects people.
* **vehicles**: Detects vehicles.
* **animals**: Detects animals.

Any custom objects you've already created appear below the built-in types, tagged as **Custom**. You can select multiple types. If you need to detect a specific object that isn't in the list, then select **+ New custom object**. Follow the steps in [Create a custom object](../security/proximity.md#create-a-custom-object) to complete setup.

6. Set the duration in the **for more than** field. Select **−** or **+** to adjust the value, or enter a value directly.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/proximity-counter.png" alt="" width="242"></div>

7. Select the **seconds** field and choose **seconds**, **minutes**, or **hours**.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/tampering-duration.png" alt="" width="242"></div>

8. Select the **camera** field to open the Choose cameras modal. Select the cameras you want to monitor, then select **Select** to confirm.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-camera-picker.png" alt="" width="375"></div>

9. Select the **time** field to set when the alert is active. [Configure alerts](../../configure-alerts.md#schedule) covers the schedule options.
10. Optionally, select **default configuration** to adjust display settings, confidence level, priority, blocking period, and alert message. [Configure alerts](../../configure-alerts.md#default-configuration) covers these settings.
11. Select **Then** <img src="../../../.gitbook/assets/alert-then.png" alt="" height="18"> to choose the action Lumana takes when the alert triggers. [Alert actions](../../alert-actions.md) covers the available actions.
12. Select **Create alert** in the top right corner. The alert is saved and becomes active immediately.
