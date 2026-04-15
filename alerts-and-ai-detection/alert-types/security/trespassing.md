# Trespassing

Trespassing detection flags any object that enters a defined area, with no minimum time requirement. Unlike zone protection, which waits for a dwell threshold before triggering, this alert triggers the moment an object appears.

## How it works

Lumana detects when a person, vehicle, or other object enters the configured camera view or zone. The alert triggers immediately and records a clip for review.

**Trespassing zones** work the same way but apply to a specific drawn zone within the camera frame rather than the full view.

## When to use it

This alert works best in spaces that should remain completely off-limits, with no exceptions for brief or incidental entry.

* Monitoring restricted areas such as server rooms, storage facilities, or private property.
* Detecting after-hours access to spaces that are only authorized during specific times.
* Flagging any entry into a defined perimeter, regardless of how briefly an object appears.

What these scenarios have in common is that entry itself is the incident, with no grace period or minimum presence needed.

## Configure the alert

The general alert configuration flow, including advanced configuration and alert actions, is covered in [Configure alerts](../../configure-alerts.md). This section covers the fields specific to Trespassing.

1. Select the **bell icon** in the navigation bar, then select **Add alert**.
2. Under **Security**, select **Use template** on the **Trespassing** card. The Create trespassing page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/trespassing-template.png" alt="" width="563"></div>

3. Enter a name in the **Alert name** field, for example "After-hours server room" or "Restricted perimeter entry."
4. Select the **objects** field in the alert rule sentence. A dropdown opens with the available object types.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/proximity-objects-dropdown.png" alt="" width="375"></div>

Select one or more object types to monitor:

* **people**: Detects people.
* **vehicles**: Detects vehicles.
* **animals**: Detects animals.

Any custom objects you've already created appear below the built-in types, tagged as **Custom**. You can select multiple types. If you need to detect a specific object that isn't in the list, then select **+ New custom object**. The custom object creation process is covered in [Proximity: Create a custom object](proximity.md#create-a-custom-object).

5. Select the **camera** field to open the Choose cameras modal. Select the cameras you want to monitor, then select **Select** to confirm.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-camera-picker.png" alt="" width="375"></div>

6. Select the **time** field to set when the alert is active. The schedule options are covered in [Configure alerts](../../configure-alerts.md#create-an-alert).
7. Optionally, select **default configuration** to adjust display settings, confidence level, priority, blocking period, and alert message. These settings are covered in [Configure alerts](../../configure-alerts.md#create-an-alert).
8. Select **Then** to choose the action Lumana takes when the alert triggers. The available actions are covered in [Alert actions](../../alert-actions.md).
9. Select **Create alert** in the top right corner. The alert is saved and becomes active immediately.
