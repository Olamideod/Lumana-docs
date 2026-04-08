# Configure alerts

<<<<<<< HEAD
=======
Lumana alerts monitor your cameras and notify you when specific conditions are detected. Some alerts are powered by AI, while others are rule-based. Each alert is built from a template written in plain language, so you can see exactly what it does before you configure it.

This page covers how to create, manage, and delete alerts. Each alert type and what it detects is covered in the [Alert types](./alert-types/) section.

## Create an alert

1. Select the **bell icon** in the navigation bar. The Alerts monitoring view opens.

<!-- IMAGE: alerts/alerts-monitoring-view.png — Alerts monitoring page showing live alert cards, filter bar with Cameras, Object, Alert type, Tags, and Unacknowledged dropdowns, and Add alert button in the top right. -->

2. Select **Add alert** in the top right corner. The Configure alerts page opens.

<!-- IMAGE: alerts/alerts-configure-page.png — Configure alerts page with left sidebar showing categories: Security, Identification, Tracking, Status, Safety and compliance, Integrations, Custom alert. Main area shows alert type cards grouped under Security, each with a description and Use template button. -->

3. Find the alert type you want. Use the left sidebar to jump to a category, or scroll through the page to browse all alert types. Each card shows a plain-language description of what the alert detects.

4. Select **Use template** on the alert type card. A new page opens with the alert rule displayed as an editable sentence.

<!-- IMAGE: alerts/alerts-create-motion.png — Create alert page for Motion showing Alert name field set to Untitled alert, the alert rule sentence with clickable inline fields for sensitivity percentage, camera, and time, a default configuration link, a Then section, and a Create alert button in the top right. -->

5. Enter a name for the alert in the **Alert name** field, for example "Main entrance motion" or "PPE violation."

6. Configure the alert rule by selecting the underlined fields in the sentence. Each field is clickable and opens an input or dropdown. The fields change depending on the alert type. For example, a Motion alert lets you set the sensitivity percentage, camera, and time window.

7. Optionally, select **default configuration** to open the Advanced configuration panel. This panel controls how the alert is displayed, sets its confidence and priority levels, configures a blocking period to reduce alert fatigue, and lets you customise the alert message with dynamic data fields. If you skip this step, the alert uses the default settings.

<!-- IMAGE: alerts/alerts-advanced-configuration.png — Advanced configuration panel showing Display alert toggle, Alert page and Walls checkboxes, Alert message text area with a dynamic field example, Confidence level dropdown set to High, Priority level dropdown set to High, Blocking period counter set to 0 seconds, Auto acknowledge toggle with seconds input, and Tags field. Done button at the bottom right. -->

   **Display and visibility**

   - **Display alert**: Toggle on to show this alert in the Alerts monitoring view. Toggle off to record and count the alert for analytics without showing it on dashboards or alert walls. Off-mode alerts are still logged and available in reports and dashboards.
   - **Alert page**: Check to show this alert on the Alerts page. Uncheck to hide it from the real-time view while keeping it as background data.
   - **Walls**: Check to show this alert on Wall displays. Uncheck to exclude it from live alert walls.

   **Alert message**

   The alert message is the notification text that appears when the alert fires. You can include dynamic fields to add context-specific information. To see the available fields, type `{{` in the message field. The supported parameters are:

   - `alert_name`
   - `timestamp`
   - `camera_name`
   - `location`
   - `alert_link`
   - `live_view_link`
   - Object attributes such as `lower_body_color`, `upper_body_color`, `hair`, `vehicle_type`, and `vehicle_color`

   **Detection and filtering**

   - **Confidence level**: The AI confidence threshold required before the alert fires. Higher confidence reduces false positives but might miss some events. Lower confidence captures more events but may include more false positives. The options are **Low**, **Medium**, and **High**. The default is **High**.
   - **Priority level**: The priority assigned to this alert. The options are **Low**, **Medium**, and **High**. The default is **High**.
   - **Blocking period**: The minimum time in seconds between consecutive alerts for the same condition. Use this to reduce notification overload and focus attention on meaningful incidents. Set to 0 to allow back-to-back alerts.
   - **Auto acknowledge**: When enabled, the alert automatically acknowledges itself after the number of seconds you set. Use this for informational alerts that don't require manual review.
   - **Tags**: Labels you can attach to this alert for filtering in the monitoring view.

   Select **Done** to close the panel and return to the alert rule. The link updates from **default configuration** to **custom configuration** to confirm your changes were applied.

8. Select **Then** to choose the action Lumana takes when the alert fires. Select one action from the list.

<!-- IMAGE: alerts/alerts-then-actions.png — Then dropdown showing Actions section with all 11 options: Notify, Toggle GPIO, Send syslog record, Play sound, Change alert group state, Change alert status, Trigger Remote IO, Notify Team3, Use http request, Send Microsoft Teams message, and Change variable value. -->

   The available actions are:

   - **Notify**: Send a notification to selected users or groups.
   - **Toggle GPIO**: Trigger a GPIO output, for example to activate a door lock or light.
   - **Send syslog record**: Send a syslog entry to an external logging system.
   - **Play sound**: Play an audio alert on a connected speaker.
   - **Change alert group state**: Update the state of an alert group when this alert fires.
   - **Change alert status**: Change the status of this alert automatically.
   - **Trigger Remote IO**: Trigger a remote input/output device.
   - **Notify Team3**: Send a notification through Team3.
   - **Use http request**: Send an HTTP request to an external endpoint.
   - **Send Microsoft Teams message**: Post a message to a Microsoft Teams channel.
   - **Change variable value**: Update the value of a configured variable.

   Each action and how to configure it is covered in [Alert actions](./alert-actions.md).

9. Select **Create alert** in the top right corner. The alert is saved and appears in the configured alerts list.

## View and manage configured alerts

To view all configured alerts, select **Configurations** from the Alerts monitoring view. The list shows every alert in your account with its name, a plain-language description of its trigger condition, and its current status.

<!-- IMAGE: alerts/alerts-list-view.png — Alerts list page showing rows of configured alerts. Each row has an enable/disable toggle on the left, a camera thumbnail, the alert name and trigger description, a green checkmark status icon, and a delete icon on the right. -->

Each row in the list shows:

- **Toggle**: Enable or disable the alert without deleting it.
- **Alert name and description**: The name you entered and a plain-language summary of the trigger condition.
- **Status icon**: A green checkmark indicates the alert is active.
- **Delete icon**: Removes the alert permanently.

To edit a configured alert, select its row in the list. The alert configuration page opens with the current settings. Update the fields you want to change, then select **Update Alert** to save. Select **Discard** to exit without saving.

## Delete an alert

To delete an alert, select the **delete icon** on the right side of the alert row in the configured alerts list.

> **Warning:** Deletion is permanent and cannot be undone.
>>>>>>> 1f9c766 (modified alert group)
