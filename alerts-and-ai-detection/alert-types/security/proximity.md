# Proximity detection

The proximity alert fires when two objects stay within a defined distance of each other for longer than a set duration. Use it to detect loitering near vehicles, unauthorized closeness to restricted equipment, or any situation where sustained proximity between objects is a security concern.

## How it works

Lumana monitors the positions of detected objects in the camera view. When two objects remain within the defined proximity threshold for longer than the configured time, the alert fires and the event is logged with a video clip. You can set it to detect any combination of object types: person to person, person to vehicle, or vehicle to vehicle.

## When to use it

Proximity detection is a good fit when brief contact between objects is normal, but sustained closeness is a concern.

- Detecting a person loitering near a parked vehicle, which may indicate an attempted theft
- Monitoring restricted areas where people should not approach certain equipment or assets
- Identifying sustained contact between individuals in sensitive or secure environments

Here's how to configure the alert once you've identified the cameras and areas to monitor.

## Configure the alert

Use the steps below to set up the proximity alert once you've identified the cameras and areas to monitor.

1. Select **Alerts** in the left navigation bar, then select **Configurations**.
2. Select **Add alert**.
3. Under the **Security** category, select **Proximity**.
4. Give the alert a name.
5. Select the object types to monitor, such as **Person** and **Vehicle**.
6. Set the proximity threshold and the duration in seconds.
7. Select the camera or cameras to monitor.
8. Set the time frame for when the alert should be active.
9. Select **Then do this** to configure a notification.
10. Select **Create alert**.

## Next steps

The guide below covers scheduling, notification options, and advanced settings.

- [Configure alerts](../../configure-alerts.md) covers scheduling, notification options, and advanced configuration settings.
