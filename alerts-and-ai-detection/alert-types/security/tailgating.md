# Tailgating

The tailgating alert detects when multiple people enter through a single access control event. The alert triggers when one badge scan is followed by more than one person entering a secured area.

## How it works

When Kisi registers a single badge scan, Lumana monitors the camera feed to count how many people pass through the entry point. If more than one person enters, then the alert triggers.

## Requirements

This alert requires the Kisi access control integration to be active in your organization. Without it, the door event data that drives the alert is unavailable.

## Configure the alert

1. Select the **bell icon** in the navigation bar. The Alerts monitoring view opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/alerts-monitoring-view1.png" alt="" width="563"></div>

2. Select **Add alert** in the top right corner. The Configure alerts page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/alerts-configure-page.png" alt="" width="563"></div>

3. Under **Security**, select **Use template** on the **Tailgating** card. The Create tailgating page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/tailgating-template.png" alt="" width="563"></div>

4. Enter a name in the **Alert name** field, for example "Main entrance tailgating" or "Server room entry."
5. Select the **objects** field in the alert rule sentence. A dropdown opens with the available object types.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/proximity-objects-dropdown.png" alt="" width="262"></div>

Select one or more object types to monitor:

* **people**: Detects people.
* **vehicles**: Detects vehicles.
* **animals**: Detects animals.

Any custom objects you've already created appear below the built-in types, tagged as **Custom**. You can select multiple types. If you need to detect a specific object that isn't in the list, then select **+ New custom object**. Follow the steps in [Create a custom object](proximity.md#create-a-custom-object) to complete setup.

6. Select the duration counter and use the **−** and **+** controls to set the time window after entry during which Lumana checks for tailgating. The default is 0.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/proximity-counter.png" alt="" width="242"></div>

7. Select the time unit field and choose **seconds**, **minutes**, or **hours**.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/tampering-duration.png" alt="" width="242"></div>

8. Select the **camera** field to open the Choose cameras modal. Select the cameras you want to monitor, then select **Select** to confirm.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-camera-picker.png" alt="" width="375"></div>

9. Select the **time** field to set when the alert is active. [Configure alerts](../../configure-alerts.md#schedule) covers the schedule options.
10. Optionally, select **default configuration** to adjust display settings, confidence level, priority, blocking period, and alert message. [Configure alerts](../../configure-alerts.md#default-configuration) covers these settings.
11. Select **Then** <img src="../../../.gitbook/assets/alert-then.png" alt="" height="18"> to choose the action Lumana takes when the alert triggers. The available actions are covered in [Alert actions](../../alert-actions.md).
12. Select **Create alert** in the top right corner. The alert is saved and becomes active immediately.
