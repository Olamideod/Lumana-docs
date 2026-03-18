# License plate recognition

License plate recognition lets you flag specific vehicles as they enter or exit your camera coverage area. The alert triggers when a detected plate matches, or doesn't match, a list you configure.

## How it works

Lumana reads license plates from the camera feed and compares them against your configured list. When a match is found, the alert triggers and a clip of the vehicle is saved. You can set it to trigger on plates that are on the list, such as an approved-entry list, or on plates that aren't on it.

## When to use it

License plate recognition is most effective when you need to control or audit vehicle access at a defined entry point.

- Monitoring gated entry points to flag vehicles that aren't on an approved list.
- Tracking the arrival and departure of specific vehicles at a premises.
- Detecting a known vehicle of interest associated with previous incidents.

These are the most common scenarios, but any situation requiring vehicle-level access control or audit trails at a defined entry point is a good fit.

## Configure the alert

Use these steps to create the alert once your plate list is ready.

1. Select **Alerts** in the left navigation bar, then select **Configurations**.
2. Select **Add alert**.
3. Under the **Identification** category, select **License plate**.
4. Give the alert a name.
5. Add the plate numbers to watch for, or import a list.
6. Choose whether to alert when a plate is found on the list or when it isn't on the list.
7. Select the camera or cameras to monitor.
8. Set the time frame for when the alert should be active.
9. Select **Then do this** to configure a notification.
10. Select **Create alert**.

Each match is logged with a clip of the vehicle and the detected plate number, creating a timestamped record for access audits or incident review.
