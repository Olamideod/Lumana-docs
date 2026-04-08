# Recommended streaming settings

Lumana is designed to integrate seamlessly with a range of IP cameras. If you’re using a camera outside of the Lumana portfolio, it is critical to correctly configure your camera before connecting it to Lumana.

If you're unsure, use the recommended settings below.

## Quick recommended configuration

Start with these defaults on each camera, then adjust only if you have a specific constraint. The sections below explain what each stream does and how to tune bitrate, resolution, and keyframes.

### Primary stream

- Resolution: Highest available
- Encoder: H.265 (H.264 supported but less efficient)
- Bitrate type: CBR
- Keyframe interval: Equal to FPS

### Sub stream

- Resolution: 720p (or lower)
- Encoder: H.265
- Bitrate type: CBR
- Image quality: Medium
- Keyframe interval: 2 × FPS

## Stream configuration overview

Most IP cameras provide at least two video streams, and some offer more.

- The **primary stream** uses the highest resolution and quality
- The **sub stream** uses lower resolution for efficiency

Lumana uses these streams for:

- AI analytics
- High-quality storage
- Standard-quality storage
- High- and standard-quality live view

We recommend configuring at least two streams to balance performance, storage, and bandwidth.

> If your camera only supports one stream, you will need to balance resolution, storage retention, and live view performance.

## Primary stream settings

The primary stream is used for analytics, high-quality storage, and live monitoring.

### Recommended settings

- Resolution: Highest available
- Encoder: H.265 (H.264 is supported but less efficient)
- Bitrate type: CBR
- Keyframe interval: Equal to FPS

### Keyframe guidance

For optimal performance:

- Use at least one keyframe every 2 seconds
- In high-motion scenes, reduce the keyframe interval to match the FPS

For example:

if your camera is at 25 fps, your keyframe interval should be no higher than 50. If you have a lot of motion in the scene, reduce the keyframe interval until it is equal to the FPS, like, if the camera is at 25 fps, set the keyframe interval to 25

- At 25 FPS → keyframe interval should be ≤ 50
- For high motion → set it to 25

### Reference values

|            | Resolution | FPS | Bitrate (Kbps) |
| ---------- | ---------- | --- | -------------- |
| VGA (16:9) | 640×360    | 15  | 800            |
| VGA        | 640×480    | 15  | 800            |
| HD         | 1280×720   | 15  | 1,800          |
| 2MP        | 1920×1080  | 15  | 2,048          |
| 3MP        | 3072×1028  | 15  | 3,084          |
| 4MP        | 2560×1440  | 15  | 3,584          |
| 5MP        | 2592×1944  | 15  | 3,584          |
| 5MP        | 2880×1620  | 15  | 3,584          |
| 8MP        | 3480×2160  | 10  | 5,120          |
| 12MP       | 4000×3000  | 10  | 6,144          |

## Sub stream settings

The sub stream is used for standard-quality storage and bandwidth optimization.

### Recommended settings

- Resolution: 720p (or lower)
- Encoder: H.265
- Bitrate type: CBR
- Image quality: Medium
- Keyframe interval: 2 × FPS

### Reference values

|            | Resolution | FPS | Bitrate (Kbps) |
| ---------- | ---------- | --- | -------------- |
| VGA (16:9) | 640×360    | 25  | 700            |
| VGA        | 640×480    | 25  | 700            |
| HD         | 1280×720   | 25  | 700            |
| 2MP        | 1280×720   | 25  | 700            |
| 3MP        | 1280×720   | 25  | 700            |
| 4MP        | 1280×720   | 25  | 700            |
| 5MP        | 1280×720   | 25  | 700            |
| 5MP        | 1280×720   | 25  | 700            |
| 8MP        | 1920×1080  | 25  | 1,024          |
| 12MP       | 1920×1080  | 25  | 1,024          |

### Lumana cameras

When using Lumana cameras, default settings already match recommended configuration.

No additional setup is required.

### Supported brand optimization

When adding supported camera brands, Lumana Core automatically applies optimized configurations.

> **Note:** While some of the parameters have common terminology (e.g. compression, resolution and etc.), other vendors use different terminology for camera parameters. The following table outlines the custom settings per brand:

|                 | Lumana | Axis | Hikvision | Uniview |
| --------------- | ------ | ---- | --------- | ------- |
| **Main stream** |        |      |           |         |
| Bitrate type    | CBR    | MBR  | CBR       | CBR     |
| Quality         | N/A    | 100  | 100       | N/A     |
| **Sub stream**  |        |      |           |         |
| Bitrate type    | CBR    | ABR  | CBR       | CBR     |
| Quality         | N/A    | 60   | 60        | N/A     |

#### FAQ: Navigating your camera configuration concerns

<details>

<summary>What happens to video storage if you don't follow <a href="./recommended-streaming-settings.md">Lumana camera configuration best practice?</a></summary>

Camera configuration best practice is required to bring you the best performance from Lumana Core. Not following the guidelines may impact two features:

1. The number of cameras that you can connect to a single Core may be lower than the spec.
2. The storage retention period may be lower than the spec. For more on retention, see [Video storage](../faq-and-reference/video-storage.md).

</details>

<details>

<summary>What is the impact of using H.264 instead of H.265?</summary>

When choosing H.264 over H.265 on primary stream, it's important to consider the impact on both image quality and Lumana core performance. Opting for H.264 can lead to a reduction in image quality of approximately 20%. This is because H.264, being an older codec, is less efficient at compressing video data, requiring more bandwidth and storage to maintain comparable quality levels. Furthermore, the core performance can suffer a significant reduction, by as much as 40%. This decrease in performance stems from the additional processing power required to handle the larger, less efficient H.264 files. As a result, the system's ability to manage multiple video streams concurrently is diminished, reducing the total number of cameras that can be connected to the Lumana core.

**Primary stream impact**

|     | Resolution | FPS | H.265 cameras | H.264 cameras |
| --- | ---------- | --- | ------------- | ------------- |
| 2MP | 1920×1080  | 15  | 10            | 10            |
| 4MP | 2560×1440  | 15  | 10            | 6             |
| 5MP | 2880×1620  | 15  | 10            | 6             |
| 8MP | 3480×2160  | 10  | 8             | 5             |

**Sub stream impact**

| Main stream   | Sub stream | H.265 FPS | H.264 FPS |
| ------------- | ---------- | --------- | --------- |
| 5MP or lower  | 1280×720   | 25        | 20        |
| 8MP or higher | 1920×1080  | 25        | 15        |

</details>

<details>

<summary>Why use CBR when connecting to Lumana Core?</summary>

Lumana Core requires IP cameras to use CBR for several important reasons:

* **Stability and Reliability**: CBR provides a consistent data stream that helps maintain stable and reliable video transmission, which is crucial for real-time monitoring and recording.
* **Network Bandwidth Management**: Using CBR allows network administrators to effectively manage and allocate network bandwidth, ensuring that each camera receives adequate resources to transmit high-quality video.

</details>

<details>

<summary>Why is a high bitrate important for CBR on Lumana Core?</summary>

Lumana Core employs a novel AI engine designed to perform sophisticated video analytics, such as object recognition, behavior analysis, and anomaly detection. For optimal performance of these AI functionalities, high-quality video input is essential. Here’s why a high bitrate is crucial:

* **Enhanced AI Quality**: A higher bitrate with CBR ensures that the video maintains high quality, providing the AI algorithms with clear and detailed images necessary for accurate analysis.I
* **Robust AI Learning**: High-quality video feeds enhance the AI model's learning and training processes, leading to more effective and efficient AI behavior over time.
* **Efficient Smart Storage Utilization**: Although higher bitrates typically require more storage space, Lumana Core integrates smart storage solutions that optimize data storage without compromising video quality. By maintaining a high bitrate, the system ensures that video data is of sufficient quality for both real-time processing and retrospective analysis, making sure the high-quality video is stored when alerts occur. This approach maximizes the utility and efficiency of storage, preserving detailed video only during critical events.

</details>

<details>

<summary>What happens if the bitrate is too low?</summary>

If the bitrate is set too low, even on CBR, it may lead to poor video quality, characterized by pixelation and blurring, especially in scenes with high motion or complexity. This degradation in video quality can severely impair the AI’s ability to perform accurate analytics, leading to compromised functionality of Lumana Core’s AI engine.

</details>

<details>

<summary>What should you configure when using Lumana cameras?</summary>

Nothing. Lumana default configuration fits the [recommended streaming settings](./recommended-streaming-settings.md).

</details>
