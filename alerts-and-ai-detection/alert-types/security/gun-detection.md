# Gun detection

Gun detection alerts you when a firearm is visible in the camera view, regardless of whether it's being actively held or brandished. It's distinct from the [gun brandished alert](gun-brandished.md), which looks specifically for a weapon raised in a threatening posture.

## How it works

Lumana's AI model scans the video feed for firearms within the frame. When one is identified, the alert triggers.

## Configure the alert

{% hint style="warning" %}
Gun detection is currently in beta. Detection accuracy might vary depending on camera angle, image quality, and lighting conditions. Test the alert in your environment before relying on it for critical security decisions.
{% endhint %}

1. Select the **bell icon** in the navigation bar. The Alerts monitoring view opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/alerts-monitoring-view1.png" alt="" width="563"></div>

2. Select **Add alert** in the top right corner. The Configure alerts page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/alerts-configure-page.png" alt="" width="563"></div>

3. Select **Security** in the left sidebar to go to that section, then select **Use template** on the **Gun detection** card. The Create gun detection page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/gun-detection-template.png" alt="" width="563"></div>

4. Enter a name in the **Alert name** field, for example "Lobby gun detection" or "Main entrance weapon alert."
5. Select the **camera** field to open the Choose cameras modal. Select the cameras you want to monitor, then select **Select** to confirm.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-camera-picker.png" alt="" width="375"></div>

6. Select the **time** field to set when the alert is active. [Configure alerts](../../configure-alerts.md#schedule) covers the schedule options.
7. Optionally, select **default configuration** to adjust display settings, confidence level, priority, blocking period, and alert message. [Configure alerts](../../configure-alerts.md#default-configuration) covers these settings.
8. Select **Then** <img src="../../../.gitbook/assets/alert-then.png" alt="" height="18"> to choose the action Lumana takes when the alert triggers. The available actions are covered in [Alert actions](../../alert-actions.md).
9. Select **Create alert** in the top right corner. The alert is saved and becomes active immediately.
