# Understand live view streaming and quality

Use this page to understand how Lumana delivers live video, when local or cloud streaming is used, and how stream quality changes based on your device and layout.

## How live view delivery works

Lumana can deliver live video through a local connection or through Lumana Cloud. The available path depends on your network, device, browser support, and the number of streams you open.

## Local streaming

Local streaming sends video from Lumana Core directly to the viewing device without relying on Lumana Cloud. This reduces internet traffic and can improve live view performance on the local network.

### Requirements for local streaming

Use local streaming when the viewing device can reach Lumana Core directly on the network.

- Direct access to the Lumana Core local IP.
- No proxy between the client and Lumana Core.

> **Note:** If a camera uses H.265 and the viewing browser or device does not support H.265, then MQ local streaming may work while HQ local streaming does not.

![Local streaming diagram.](../.gitbook/assets/live-video-monitoring-and-operations/live-view-local-streaming-diagram.png)

### Local live view flow

When you open Live view, Lumana first checks whether the viewing device can reach Lumana Core on the local network. If the connection is available, then Lumana starts the stream directly from Lumana Core.

## Cloud streaming

Cloud streaming delivers live video through Lumana Cloud when local streaming is not available. Use this path when the viewing device cannot connect directly to Lumana Core.

### Cloud live view flow

If Lumana cannot establish a local connection, then it switches to cloud streaming. Cloud streaming uses WebRTC to deliver the live view to the client.

![Cloud streaming diagram.](../.gitbook/assets/live-video-monitoring-and-operations/live-view-cloud-streaming-diagram.png)

## Manage streaming quality

Lumana can adjust live view quality automatically, and you can also change it manually in the player.

![Streaming quality diagram.](../.gitbook/assets/live-video-monitoring-and-operations/live-view-quality-routing-diagram.png)

### How quality selection works

Lumana supports `SQ`, `MQ`, and `HQ` live view quality modes. The selected mode depends on the stream layout, the available bandwidth, and the player size.

- Lumana may choose a lower quality automatically when you open multiple streams at the same time.
- You can change the stream quality manually from the player controls.
- In multi-camera layouts, Lumana may prioritize smoother playback over higher quality.

![Multi-stream live view example.](../.gitbook/assets/live-video-monitoring-and-operations/live-view-multi-stream-example.png)

In the example above, the top cameras use `MQ`, while the lower cameras use `SQ`. Hovering over a stream lets you change the stream quality.

### Reference values

Use the following table as a reference for typical local and cloud live view resolutions and bitrates.

| Native resolution | Quality    | Resolution | Estimated bitrate |
| ----------------- | ---------- | ---------- | ----------------- |
| 3480x2160 (8MP)   | HQ (Local) | 3480x2160  | 5.12 Mbps         |
| 3480x2160 (8MP)   | HQ (Cloud) | 1920x1080  | <3 Mbps           |
| 3480x2160 (8MP)   | MQ         | 960x540    | <0.8 Mbps         |
| 3480x2160 (8MP)   | SQ         | 426x240    | <0.2 Mbps         |
| 2880x1620 (5MP)   | HQ (Local) | 2880x1620  | 3.5 Mbps          |
| 2880x1620 (5MP)   | HQ (Cloud) | 1920x1080  | <3 Mbps           |
| 2880x1620 (5MP)   | MQ         | 960x540    | <0.8 Mbps         |
| 2880x1620 (5MP)   | SQ         | 426x240    | <0.2 Mbps         |
| 2592x1944 (5MP)   | HQ (Local) | 2592x1944  | 3.5 Mbps          |
| 2592x1944 (5MP)   | HQ (Cloud) | 1440x1080  | <3 Mbps           |
| 2592x1944 (5MP)   | MQ         | 720x540    | <0.8 Mbps         |
| 2592x1944 (5MP)   | SQ         | 320x240    | <0.2 Mbps         |
| 2560x1440 (4MP)   | HQ (Local) | 2560x1440  | 3 Mbps            |
| 2560x1440 (4MP)   | HQ (Cloud) | 1920x1080  | <3 Mbps           |
| 2560x1440 (4MP)   | MQ         | 960x540    | <0.8 Mbps         |
| 2560x1440 (4MP)   | SQ         | 426x240    | <0.2 Mbps         |
| 1920x1080 (2MP)   | HQ (Local) | 1920x1080  | 2 Mbps            |
| 1920x1080 (2MP)   | HQ (Cloud) | 1920x1080  | <2 Mbps           |
| 1920x1080 (2MP)   | MQ         | 960x540    | <0.8 Mbps         |
| 1920x1080 (2MP)   | SQ         | 426x240    | <0.2 Mbps         |
| 1280x720 (HD)     | HQ (Local) | 1280x720   | 1.8 Mbps          |
| 1280x720 (HD)     | HQ (Cloud) | 1280x720   | <1.8 Mbps         |
| 1280x720 (HD)     | MQ         | 960x540    | <0.8 Mbps         |
| 1280x720 (HD)     | SQ         | 426x240    | <0.2 Mbps         |
