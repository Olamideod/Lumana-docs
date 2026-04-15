# Gun brandished

The gun brandished alert triggers when a gun is actively brandished on camera. It works with Lumana's professional monitoring service for immediate dispatch when needed.

## How it works

Lumana's AI model analyzes the video feed for a gun being brandished. When it detects one, the alert triggers immediately and captures a clip of the event.

## When to use it

Gun brandished detection is suited for locations where armed incidents are a defined security risk.

* Protecting high-security environments such as banks, government buildings, or data centers from armed incidents.
* Monitoring retail locations because theft and armed confrontations are an operational risk.
* Supporting weapon detection protocols in any facility where firearms are prohibited.

{% hint style="info" %}
This alert type is supported by Lumana's professional monitoring service. Trained agents can verify the alert and dispatch first responders when needed.
{% endhint %}

## Configure the alert

{% hint style="warning" %}
Gun brandished detection is currently in beta. Detection accuracy might vary depending on camera angle, image quality, and lighting conditions. Test the alert in your environment before relying on it for critical security decisions.
{% endhint %}

The general alert configuration flow, including advanced configuration and alert actions, is covered in [Configure alerts](../../configure-alerts.md). This section covers the fields specific to gun brandished detection.

1. Select the **bell icon** in the navigation bar, then select **Add alert**.
2. Under **Security**, select **Use template** on the **Gun brandished** card. The Create gun brandished page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/gun-brandished-template.png" alt="" width="563"></div>

3. Enter a name in the **Alert name** field, for example "Lobby gun brandished" or "Main entrance weapon alert."
4. Select the **camera** field to open the Choose cameras modal. Select the cameras you want to monitor, then select **Select** to confirm.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/motion-camera-picker.png" alt="" width="375"></div>

5. Select the **time** field to set when the alert is active. The schedule options are covered in [Configure alerts](../../configure-alerts.md#create-an-alert).
6. Optionally, select **default configuration** to adjust display settings, confidence level, priority, blocking period, and alert message. These settings are covered in [Configure alerts](../../configure-alerts.md#create-an-alert).
7. Select **Then** to choose the action Lumana takes when the alert triggers. For this alert type, consider notifying security personnel immediately or enabling professional monitoring. The available actions are covered in [Alert actions](../../alert-actions.md).
8. Select **Create alert** in the top right corner. The alert is saved and becomes active immediately.
