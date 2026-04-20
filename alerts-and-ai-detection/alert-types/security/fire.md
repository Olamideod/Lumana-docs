# Fire

The fire alert triggers when flames or smoke are visible in the camera feed. It works as a visual detection layer alongside your existing alarm systems, covering areas that physical sensors might not reach.

## How it works

Lumana's AI model analyzes the video feed for the visual signatures of fire or smoke. When the configured condition is detected, the alert triggers immediately and a clip is saved. Because detection is camera-based, it can cover outdoor areas, large open spaces, and locations where smoke detectors aren't practical.

## When to use it

Fire detection works best as a supplementary layer in environments where visual detection can help speed up response time.

* Adding detection coverage in warehouses, production floors, or large open spaces where fire can spread quickly.
* Covering outdoor areas or locations where smoke detectors are impractical.
* Supporting faster incident response by providing a video clip alongside the alert notification.

In each case, visual detection adds a coverage layer that's independent of physical sensors and available wherever cameras are deployed.

## Configure the alert

The general alert configuration flow, including advanced configuration and alert actions, is covered in [Configure alerts](../../configure-alerts.md). This section covers the fields specific to fire detection.

1. Select the **bell icon** in the navigation bar, then select **Add alert**.
2. Under **Security**, select **Use template** on the **Fire** card. The Create fire page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/fire-template.png" alt="" width="563"></div>

3. Enter a name in the **Alert name** field, for example "Warehouse fire detection" or "Loading dock smoke alert."
4. Select the **fire** field in the alert rule sentence. A dropdown opens with the available detection types.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/fire-type-dropdown.png" alt="" width="249"></div>

Select the condition you want to detect:

* **fire**: Detects visible flames in the camera feed.
* **smoke**: Detects visible smoke in the camera feed.

5. Select the **camera** field to open the Choose cameras modal. Select the cameras you want to monitor, then select **Select** to confirm.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-camera-picker.png" alt="" width="375"></div>

6. Select the **time** field to set when the alert is active. The schedule options are covered in [Configure alerts](../../configure-alerts.md#create-an-alert).
7. Optionally, select **default configuration** to adjust display settings, confidence level, priority, blocking period, and alert message. These settings are covered in [Configure alerts](../../configure-alerts.md#create-an-alert).
8. Select **Then** to choose the action Lumana takes when the alert triggers. The available actions are covered in [Alert actions](../../alert-actions.md).
9. Select **Create alert** in the top right corner. The alert is saved and becomes active immediately.
