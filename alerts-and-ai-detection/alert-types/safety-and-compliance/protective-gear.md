# Protective gear detection

Protective gear detection flags workers who are missing required PPE in the camera view. It's built for environments where continuous manual compliance checks aren't practical.

## How it works

Lumana analyzes the camera feed and checks whether detected individuals are wearing the configured safety equipment. When someone is found without the required gear, Lumana flags the person and saves a clip of the event. You can configure it to check for specific items such as hard hats, safety helmets, or reflective vests.

## When to use it

This alert is most effective in environments where PPE requirements are non-negotiable and manual supervision can't provide continuous coverage.

- Enforcing hard hat requirements on construction sites or in industrial facilities.
- Monitoring production floors for workers not wearing required safety equipment.
- Providing a continuous compliance check without relying solely on manual supervision.

These are the most common scenarios, but any environment with a defined PPE requirement and a camera covering the work area is a good fit.

## Configure the alert

Use these steps to create the alert once you've identified the cameras and areas to cover.

1. Select **Alerts** in the left navigation bar, then select **Configurations**.
2. Select **Add alert**.
3. Under the **Safety & Compliance** category, select **Protective gear**.
4. Give the alert a name.
5. Select the gear type to check for, such as **Helmet** or **Safety vest**.
6. Select the camera or cameras to monitor.
7. Optionally draw a zone to restrict detection to a specific area.
8. Set the time frame for when the alert should be active.
9. Select **Then do this** to configure a notification.
10. Select **Create alert**.

Each triggered event is saved with a clip of the non-compliant worker, giving you a timestamped record for compliance reporting and follow-up.
