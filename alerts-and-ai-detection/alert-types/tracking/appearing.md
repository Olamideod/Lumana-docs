# Appearing

The appearing alert triggers the moment an object enters a zone you've drawn in the camera view. There's no minimum time requirement, and entry alone is enough to trigger it.

## How it works

Draw a detection zone in the camera frame. When an object of the configured type crosses into that zone, the alert triggers and saves a clip. This is useful when you want to know as soon as something appears, rather than waiting for it to linger.

Compare this with the [loitering alert](loitering.md), which requires an object to remain in a zone for a set duration before triggering.

## When to use it

Appearing detection is well suited for monitored zones where any entry, no matter how brief, is worth flagging.

* Monitoring a delivery area to know the moment a vehicle or person arrives.
* Detecting any entry into a zone where only scheduled access is expected.
* Triggering an alert the instant someone steps into a defined restricted area.

These are the most common scenarios, but any zone where the moment of entry is more important than how long an object stays is a good fit.

## Configure the alert

Use these steps to create the alert once you've identified the zone to monitor.

1. Select **Alerts** in the left navigation bar, then select **Configurations**.
2. Select **Add alert**.
3. Under the **Tracking** category, select **Appearing**.
4. Give the alert a name.
5. Select the object types to monitor, such as **Person** or **Vehicle**.
6. Draw the zone in the camera view.
7. Select the camera or cameras to monitor.
8. Set the time frame for when the alert should be active.
9. Select **Then do this** to configure a notification.
10. Select **Create alert**.

Once active, every entry into the zone triggers a clip you can review, share, or archive directly from the alert feed.
