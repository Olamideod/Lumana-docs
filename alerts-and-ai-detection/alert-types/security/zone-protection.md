# Zone protection

Zone protection monitors a defined area for objects that linger. Unlike trespassing, which triggers on entry alone, it requires an object to stay inside the zone past a minimum dwell time before triggering.

## How it works

Define a zone within the camera frame and set a minimum dwell time. Lumana tracks detected objects and triggers the alert only when one has stayed inside the zone past the configured threshold. This filters out people or vehicles that are just passing through, so you're only alerted when presence is intentional.

## Configure the alert

1. Select the **bell icon** in the navigation bar. The Alerts monitoring view opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/alerts-monitoring-view1.png" alt="" width="563"></div>

2. Select **Add alert** in the top right corner. The Configure alerts page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/alerts-configure-page.png" alt="" width="563"></div>

3. Select **Security** in the left sidebar to go to that section, then select **Use template** on the **Zone protection** card. The Create zone protection page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/zone-protection-template.png" alt="" width="563"></div>

4. Enter a name in the **Alert name** field, for example "Restricted area dwell" or "After-hours parking zone."
5. Select the **objects** field in the alert rule sentence. A dropdown opens with the available object types.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/proximity-objects-dropdown.png" alt="" width="375"></div>

Select one or more object types to monitor:

* **people**: Detects people.
* **vehicles**: Detects vehicles.
* **animals**: Detects animals.

Any custom objects you've already created appear below the built-in types, tagged as **Custom**. You can select multiple types. If you need to detect a specific object that isn't in the list, then select **+ New custom object**. Follow the steps in [Create a custom object](proximity.md#create-a-custom-object) to complete setup.

6. Select the **zone** field to open the Choose cameras modal. Select the cameras you want to monitor, then select **Select** to confirm.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-camera-picker.png" alt="" width="375"></div>

After selecting a camera, draw a detection zone to limit detection to a specific area of the frame. Select the **edit icon** next to the camera name to open the Select region of interest dialog.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-zone-drawing.png" alt="" width="563"></div>

Select points on the camera feed to define the zone boundary. Each point connects to the next with a green line. When the polygon is closed, the enclosed area fills with a green overlay indicating the active detection zone.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-zone-complete.png" alt="" width="563"></div>

* **Exclude**: Toggle on to invert the zone. Objects outside the drawn area trigger the alert instead of objects inside it.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-zone-invert.png" alt="" width="563"></div>

* **Reset**: Clears all points and lets you start over.
* **Select**: Confirms the zone and closes the dialog.

7. Set the dwell time threshold. Select **+** to increase the value or **-** to decrease it. Then select the unit dropdown next to the counter and choose **seconds**, **minutes**, or **hours**. The alert only triggers when an object has been inside the zone for at least this long.
8. Select the **time** field to set when the alert is active. [Configure alerts](../../configure-alerts.md#schedule) covers the schedule options.
9. Optionally, select **default configuration** to adjust display settings, confidence level, priority, blocking period, and alert message. [Configure alerts](../../configure-alerts.md#default-configuration) covers these settings.
10. Select **Then** <img src="../../../.gitbook/assets/alert-then.png" alt="" height="18"> to choose the action Lumana takes when the alert triggers. The available actions are covered in [Alert actions](../../alert-actions.md).
11. Select **Create alert** in the top right corner. The alert is saved and becomes active immediately.
