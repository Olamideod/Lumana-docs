# Tailgating detection

The tailgating alert detects when multiple people enter through a single access control event. It triggers when one badge scan results in more than one person entering a secured area, flagging potential unauthorized access before it becomes an incident.

## How it works

When Kisi registers a single badge scan, Lumana monitors the camera feed to count how many people pass through the entry point. If more than one person enters, the alert triggers and captures a clip of the event.

## Requirements

This alert requires the Kisi access control integration to be active in your organization. Without it, the door event data that drives the alert is unavailable. See [Kisi access control](../../../software-integrations/kisi-access-control.md) for setup instructions.

The Kisi integration is the only prerequisite; once it's active, the door event data Lumana needs is available.

## Configure the alert

Use these steps to create the alert once Kisi is configured.

1. Select **Alerts** in the left navigation bar, then select **Configurations**.
2. Select **Add alert**.
3. Scroll down and select **Door tailgating**.
4. Give the alert a name, then select **Doors** to choose which access points to monitor.
5. Select the pencil icon next to each door to set up the line crossing event that counts individuals entering.
6. Select the object type to track: people, vehicles, pets, or shopping carts.
7. Set the time window after a door opens during which Lumana checks for tailgating.
8. Configure the schedule for when the alert should be active.
9. Select **Then do this** to configure notifications.
10. Select **Create alert**.

When tailgating is detected, the clip is saved alongside the corresponding door event, giving you a complete record of the entry.
