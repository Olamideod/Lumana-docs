# Suspect alerts

Suspect alerts let you detect specific individuals based on their identity, or flag unauthorized hand contact in sensitive areas. Use them to identify known persons of interest, monitor access to restricted equipment, or create audit records of interactions in high-risk locations.

## Alert types

There are two alert types in this group. Each is configured separately depending on what you want to detect.

### Face recognition

The face recognition alert triggers when Lumana identifies a person who appears on, or does not appear on, a defined list of faces in your organization's database.

- Detecting known persons of interest when they appear on camera
- Flagging individuals not recognized as authorized personnel in a restricted area
- Building an audit trail of who accessed a specific location

### Hands detected

The hands detected alert triggers when hands are visible within a defined zone. Use it to monitor areas where hand contact with equipment or assets should not occur.

- **Asset protection**: Prevents unauthorized interaction with sensitive equipment such as servers or network hardware.
- **Audit and compliance**: Documents hand interactions at high-risk locations for investigation records.

Both alert types are configured separately. Follow the steps for the one you need.

## Configure the alert

Use the steps below for the alert type you want to set up.

### Face recognition

Use these steps to configure the face recognition alert.

1. Select **Alerts** in the left navigation bar, then select **Configurations**.
2. Select **Add alert**.
3. Under the **Identification** category, select **Face recognition**.
4. Give the alert a name.
5. Configure whether the alert should trigger when a person appears on, or does not appear on, a list.
6. Select the relevant cameras and set the schedule.
7. Select **Then do this** to configure notifications.
8. Select **Create alert**.

### Hands detected

Use these steps to configure the hands detected alert.

1. Select **Alerts** in the left navigation bar, then select **Configurations**.
2. Select **Add alert**.
3. Under the **Safety & compliance** category, select **Hands**.
4. Set the detection schedule using **All times** or configure a custom window.
5. Select **Then do this** to configure a notification action.
6. Select **Zones** to define the areas where hand detection should be active on your cameras.
7. Draw the zone on the camera view, then select **Done**.

## Next steps

- [Gun drawn](../security/gun-drawn.md) — Detect when a weapon is actively brandished.
- [Build a database of people and vehicles](../../../databases-analytics-and-search/build-a-database-of-people-and-vehicles.md) — Create and manage face lists for identification alerts.
- [Configure alerts](../../configure-alerts.md) — Scheduling, notification options, and advanced settings.
