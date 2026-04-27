# Suspect alerts

The suspect alert triggers when Lumana detects a person from a watchlist you define. Use it to identify known persons of interest, flag unauthorized individuals in restricted areas, or build an audit trail of who appeared on camera.

## How it works

Lumana matches detected faces in the camera feed against a list of people you build from your organization's database. When Lumana finds a match, the alert triggers.

## Configure the alert

1. Select the **bell icon** in the navigation bar. The Alerts monitoring view opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/alerts-monitoring-view1.png" alt="" width="563"></div>

2. Select **Add alert** in the top right corner. The Configure alerts page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/alerts-configure-page.png" alt="" width="563"></div>

3. Select **Security** in the left sidebar to go to that section, then select **Use template** on the **Suspect** card. The Create suspect page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/suspect-template.png" alt="" width="563"></div>

4. Enter a name in the **Alert name** field, for example "Persons of interest" or "Restricted area watchlist."
5. Select the **appears** field in the alert rule sentence. A dropdown opens confirming the alert triggers when a person on the list is detected.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/suspect-appears-dropdown.png" alt="" width="249"></div>

6. Select the **list** field to open the People's list modal.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/suspect-peoples-list.png" alt="" width="375"></div>

   Use the **Search people** field to find people from your organization database. Select a person to add them to the list. Each person you add appears under **Person name** with a remove button next to their name.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/suspect-peoples-list-selected.png" alt="" width="375"></div>

   * To remove a person, select the **×** button next to their name.
   * To remove everyone, select **Clear list**.

   Select **Done** to confirm the list and close the modal.

7. Select the **camera** field to open the Choose cameras modal. Select the cameras you want to monitor, then select **Select** to confirm.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-camera-picker.png" alt="" width="375"></div>

8. Select the **time** field to set when the alert is active. [Configure alerts](../../configure-alerts.md#schedule) covers the schedule options.
9. Optionally, select **default configuration** to adjust display settings, confidence level, priority, blocking period, and alert message. [Configure alerts](../../configure-alerts.md#default-configuration) covers these settings.
10. Select **Then** <img src="../../../.gitbook/assets/alert-then.png" alt="" height="18"> to choose the action Lumana takes when the alert triggers. The available actions are covered in [Alert actions](../../alert-actions.md).
11. Select **Create alert** in the top right corner. The alert is saved and becomes active immediately.
