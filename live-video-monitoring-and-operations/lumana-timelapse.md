# Use Lumana timelapse

Use Lumana timelapse to review recent activity across a camera without scrubbing through full video manually. By default, timelapse is available for recent snapshots, and you can extend that retention window when you need a longer view.

## Prerequisites

Make sure you can open the camera settings for the camera you want to use. You also need permission to change snapshot retention settings.

## Understand timelapse availability

Timelapse is enabled by default and is available for the most recent three days of retained snapshots.

Timelapse snapshots are not generated retroactively. If you increase retention today, then the system starts collecting additional days of timelapse snapshots from that point forward.

## Create a timelapse

Use **Create timelapse** when you want a fast-motion replay from snapshots that fall inside your current **Snapshot retention days** window.

1. Open the camera from **Devices** or **Live view**.
2. Open **Create timelapse** from the camera or timelapse toolbar (wording can vary slightly by deployment).
3. Enter a **Name**, confirm **Camera**, set **Timeframe** (for example **Last 3 Days**), **Duration**, and any timestamp or label placement options.
4. Select **Create**.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/live-video-monitoring-and-operations/lumana-timelapse-create-dialog.png" alt="Create timelapse dialog with Name, Camera, Timeframe, Duration, timestamp placement, and Create." width="563"></div>

## Extend timelapse retention

You can extend timelapse retention on the camera **Storage** page when you need a longer review window.

1. Open **Devices**, select the camera you want, then open **Edit camera**.
2. Select **Storage** in the sidebar.
3. Under **Data retention**, open **Snapshot retention days** and choose a period from the list. Typical options are **3**, **7**, **14**, and **30 days**. Your organization may also offer **90 days** when that tier is enabled (the dropdown shows every value your deployment supports).
4. Select **Save** in the upper right.

   The new retention setting applies going forward.

{% hint style="info" %}
Once you increase retention, additional snapshots begin collecting from that point. You must wait for time to pass before you can generate longer timelapse videos.
{% endhint %}

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/live-video-monitoring-and-operations/lumana-timelapse-retention-settings.png" alt="" width="563"></div>

Once you know the default window and the longest **Snapshot retention days** option in your deployment, decide whether the built-in range covers your workflow.

## Extend history beyond snapshot retention

If you need timelapse history beyond the maximum **Snapshot retention days** value available in your deployment, then contact Customer Support to discuss extended storage options.

## Next steps

After you review timelapse settings, you can continue with related playback and monitoring tasks.

- Use [Multi-camera playback](multi-camera-playback.md) to review recorded footage across multiple cameras.
- Use [Live view](live-view.md) to monitor cameras in real time.