# Tampering

Tampering detection triggers when a camera is physically interfered with, such as being moved, covered, or obstructed. Use it to detect interference before surveillance coverage is lost.

## How it works

Lumana monitors the camera feed for sudden visual changes that indicate physical interference. When tampering persists beyond the duration you set, the alert triggers and a video clip is saved to the alert feed.

## When to use it

Tampering detection is useful in any environment where camera coverage must remain uninterrupted.

- Securing cameras in public or semi-public areas where physical access is difficult to control.
- Detecting interference before a larger security incident occurs.
- Ensuring continuous coverage in high-security or compliance-sensitive locations.

## Configure the alert

The general alert configuration flow, including advanced configuration and alert actions, is covered in [Configure alerts](../../configure-alerts.md). This section covers the fields specific to Tampering.

1. Select the **bell icon** in the navigation bar, then select **Add alert**.
2. Under **Security**, select **Use template** on the **Tampering** card. The Create tampering page opens.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/tampering-template.png" alt="" width="563"></div>

3. Enter a name in the **Alert name** field, for example "Camera tampering" or "Entrance camera interference."
4. Select the camera environment field in the alert rule sentence and choose **Indoor** or **Outdoor** depending on where the camera is installed.
5. Select the **camera** field to open the Choose cameras modal. Select the cameras you want to monitor, then select **Select** to confirm.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/tampering-camera-picker.png" alt="" width="375"></div>

6. Select the duration counter and use the **−** and **+** controls to set how long tampering must persist before the alert triggers. The default is 10.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/tampering-counter.png" alt="" width="242"></div>

7. Select the time unit field and choose **seconds**, **minutes**, or **hours**.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/tampering-duration.png" alt="" width="242"></div>

8. Select the **time** field to set when the alert is active. The schedule options are covered in [Configure alerts](../../configure-alerts.md#create-an-alert).
9. Optionally, select **default configuration** to adjust display settings, confidence level, priority, blocking period, and alert message. These settings are covered in [Configure alerts](../../configure-alerts.md#create-an-alert).
10. Select **Then** to choose the action Lumana takes when the alert triggers. The available actions are covered in [Alert actions](../../alert-actions.md).
11. Select **Create alert** in the top right corner. The alert is saved and becomes active based on the schedule you set.