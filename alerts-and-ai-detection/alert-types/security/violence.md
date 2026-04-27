# Violence

The violence detection alert triggers when Lumana detects fighting or physical aggression in the camera view. Use it to monitor high-risk environments, enable a rapid security response, or flag incidents for review.

## How it works

Lumana uses AI to analyze movement patterns and body postures in the video feed. The model identifies physical altercations such as fighting, striking, or aggressive physical contact. When it does, the alert triggers.

## Limitations

Violence detection requires a clear, unobstructed view of the monitored area. Crowded environments or scenes with rapid but non-violent movement, such as sports facilities or training areas, might produce false positives. Poor lighting also reduces detection accuracy.

Environments with stable lighting, low background movement, and an unobstructed camera view tend to produce the most reliable results.

## Configure the alert

{% hint style="warning" %}
Violence detection is currently in beta. Detection accuracy might vary depending on camera placement, lighting conditions, and the environment. Test the alert in your environment before relying on it for critical security decisions.
{% endhint %}

1. Select the **bell icon** in the navigation bar. The Alerts monitoring view opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/alerts-monitoring-view1.png" alt="" width="563"></div>

2. Select **Add alert** in the top right corner. The Configure alerts page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/alerts-configure-page.png" alt="" width="563"></div>

3. Select **Security** in the left sidebar to go to that section, then select **Use template** on the **Violence** card. The Create violence page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/violence-template.png" alt="" width="563"></div>

4. Enter a name in the **Alert name** field, for example "Lobby violence detection" or "Car park altercation alert."
5. Select the **camera** field to open the Choose cameras modal. Select the cameras you want to monitor, then select **Select** to confirm.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-camera-picker.png" alt="" width="375"></div>

6. Select the **time** field to set when the alert is active. [Configure alerts](../../configure-alerts.md#schedule) covers the schedule options.
7. Optionally, select **default configuration** to adjust display settings, confidence level, priority, blocking period, and alert message. [Configure alerts](../../configure-alerts.md#default-configuration) covers these settings.
8. Select **Then** <img src="../../../.gitbook/assets/alert-then.png" alt="" height="18"> to choose the action Lumana takes when the alert triggers. The available actions are covered in [Alert actions](../../alert-actions.md).
9. Select **Create alert** in the top right corner. The alert is saved and becomes active immediately.
