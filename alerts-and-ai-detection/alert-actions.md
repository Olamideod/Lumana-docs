# Alert actions

<!-- When an alert fires, Lumana can do more than just log the event. Actions let you define what happens next, whether that's notifying a person, triggering a device, or sending data to an external system. You set the action in the **Then** section when creating or editing an alert.

Each alert supports one action. The action runs every time the alert's conditions are met, subject to any blocking period you've configured.

## Add an action

When creating or editing an alert, scroll down to the **Then** section and select it to open the action list.

<!-- IMAGE: alerts/alerts-then-actions.png — Then dropdown showing the Actions section with all available action options listed. -->

<!-- Select the action you want to use. The section expands to show the configuration fields for that action. Fill in the required fields, then continue to save the alert.

## Available actions

### Notify

Sends a notification to selected users or groups when the alert fires. Use this to alert your team about events that need immediate attention.

To configure it, select the users or groups who should receive the notification. You can notify individuals, roles, or entire teams depending on how your organization is set up.

### Toggle GPIO

Triggers a GPIO output on a connected Core device. Use this to activate a physical device, for example a door relay, a siren, or a warning light, when the alert fires.

To configure it, select the Core device and the GPIO output you want to toggle. For more on how GPIO works, see [GPIO](../configuring-cameras-and-devices/other-devices/gpio.md).

### Send syslog record

Sends a syslog entry to an external logging or SIEM system when the alert fires. Use this to integrate Lumana alerts into your existing security event pipeline.

To configure it, enter the syslog server address, port, and protocol. The syslog message includes the alert name, timestamp, camera, and trigger details.

### Play sound

Plays an audio alert on a connected speaker when the alert fires. Use this as an on-site deterrent or audible notification.

To configure it, select the speaker and the sound file to play.

### Change alert group state

Updates the state of an alert group when the alert fires. Use this when you want one alert to change the conditions or behavior of a related group of alerts.

To configure it, select the alert group and the target state.

### Change alert status

Changes the status of this alert automatically when it fires. Use this for alerts that should self-resolve or change priority based on what triggered them.

To configure it, select the new status to apply.

### Trigger Remote IO

Triggers a remote input/output device connected to your system. Use this to activate external hardware or integration points beyond GPIO.

To configure it, select the remote IO target and define the trigger parameters.

### Notify Team3

Sends a notification through the Team3 integration. Use this if your organization uses Team3 for incident communication.

To configure it, enter the Team3 channel or contact details.

### Use HTTP request

Sends an HTTP request to an external endpoint when the alert fires. Use this to trigger webhooks, push data to third-party platforms, or integrate with custom applications.

To configure it, enter the URL, select the HTTP method (GET, POST, and so on), and optionally add headers and a body payload.

### Send Microsoft Teams message

Posts a message to a Microsoft Teams channel when the alert fires. Use this to surface Lumana alerts directly in your team's communication workspace.

To configure it, connect your Microsoft Teams account and select the channel where messages should appear.

### Change variable value

Updates the value of a configured variable when the alert fires. Use this in combination with variable-based alert rules to create conditional or stateful alert logic.

To configure it, select the variable and enter the new value to set. --> -->
