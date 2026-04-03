# Recommended streaming settings

Configure your camera streams to ensure optimal performance for analytics, storage, and live monitoring in Lumana.

If you're unsure, use the recommended settings below.

---

## Quick recommended configuration

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

---

## Stream configuration overview

Most IP cameras provide at least two video streams, and some offer more.

- The **primary stream** uses the highest resolution and quality  
- The **sub stream** uses lower resolution for efficiency  

Lumana uses these streams for:

- AI analytics  
- High-quality storage  
- Standard-quality storage  
- High- and low-quality live view  

We recommend configuring at least two streams to balance performance, storage, and bandwidth.

> If your camera only supports one stream, you will need to balance resolution, storage retention, and live view performance.

---

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
- At 25 FPS → keyframe interval should be ≤ 50  
- For high motion → set it to 25  


### Reference values

|  | Resolution  | FPS | Bitrate (Kbps) |
|--|-------------|-----|----------------|
| VGA (16:9) | 640×360     | 15  | 800            |
| VGA        | 640×480     | 15  | 800            |
| HD         | 1280×720    | 15  | 1,800          |
| 2MP        | 1920×1080   | 15  | 2,048          |
| 3MP        | 3072×1028   | 15  | 3,084          |
| 4MP        | 2560×1440   | 15  | 3,584          |
| 5MP        | 2592×1944   | 15  | 3,584          |
| 5MP        | 2880×1620   | 15  | 3,584          |
| 8MP        | 3480×2160   | 10  | 5,120          |
| 12MP       | 4000×3000   | 10  | 6,144          |


## Sub stream settings

The sub stream is used for standard-quality storage and bandwidth optimization.

### Recommended settings

- Resolution: 720p (or lower)  
- Encoder: H.265  
- Bitrate type: CBR  
- Image quality: Medium  
- Keyframe interval: 2 × FPS  


### Reference values

|  | Resolution  | FPS | Bitrate (Kbps) |
|--|-------------|-----|----------------|
| VGA (16:9) | 640×360     | 25  | 700            |
| VGA        | 640×480     | 25  | 700            |
| HD         | 1280×720    | 25  | 700            |
| 2MP        | 1280×720    | 25  | 700            |
| 3MP        | 1280×720    | 25  | 700            |
| 4MP        | 1280×720    | 25  | 700            |
| 5MP        | 1280×720    | 25  | 700            |
| 5MP        | 1280×720    | 25  | 700            |
| 8MP        | 1920×1080   | 25  | 1,024          |
| 12MP       | 1920×1080   | 25  | 1,024          |


## Lumana cameras

When using Lumana cameras, default settings already match recommended configuration.

No additional setup is required.

---

## Supported brand optimization

When adding supported camera brands, Lumana Core automatically applies optimized configurations.

Some parameter names may differ between vendors.

|  | Lumana | Axis | Hikvision | Uniview |
|--|--------|------|-----------|---------|
| **Main stream** | | | | |
| Bitrate type | CBR | MBR | CBR | CBR |
| Quality | N/A | 100 | 100 | N/A |
| **Sub stream** | | | | |
| Bitrate type | CBR | ABR | CBR | CBR |
| Quality | N/A | 60 | 60 | N/A |

## FAQ: Navigating your camera configuration concerns

<details>
<summary>What happens to video storage if you don't follow Lumana camera configuration best practice?</summary>

Camera configuration best practice is required to bring you the best performance from Lumana Core. Not following the guidelines may impact two features:

1. The number of cameras that you can connect to a single Core may be lower than the spec.
2. The storage retention period may be lower than the spec. For more on retention, see [Lumana Video Storage: Revolutionizing Video Security Retention](https://support.lumana.ai/knowledge/articles/11078121786386/en-us?brand_id=10899747518610).

</details>

<details>
<summary>What is the impact of using H.264 instead of H.265?</summary>

When you choose H.264 over H.265 on the primary stream, consider the impact on image quality and Lumana Core performance. H.264 can reduce image quality by approximately 20%. H.264 is less efficient at compression, so it needs more bandwidth and storage for comparable quality. Core performance can drop by as much as 40% because processing larger, less efficient streams takes more resources. That limits how many concurrent streams the system can handle and how many cameras you can connect to Lumana Core.

**Primary stream impact**

|  | Resolution | FPS | H.265 cameras | H.264 cameras |
|--|------------|-----|---------------|---------------|
| 2MP | 1920×1080 | 15 | 10 | 10 |
| 4MP | 2560×1440 | 15 | 10 | 6 |
| 5MP | 2880×1620 | 15 | 10 | 6 |
| 8MP | 3480×2160 | 10 | 8 | 5 |

**Sub stream impact**

| Main stream | Sub stream | H.265 FPS | H.264 FPS |
|-------------|------------|-----------|-----------|
| 5MP or lower | 1280×720 | 25 | 20 |
| 8MP or higher | 1920×1080 | 25 | 15 |

</details>

<details>
<summary>Why use CBR when connecting to Lumana Core?</summary>

Lumana Core requires IP cameras to use CBR for several important reasons:

- **Stability and reliability:** CBR provides a consistent data stream that helps maintain stable, reliable video transmission for real-time monitoring and recording.
- **Network bandwidth management:** CBR helps you manage and allocate bandwidth so each camera gets enough capacity for high-quality video.

</details>

<details>
<summary>Why is a high bitrate important for CBR on Lumana Core?</summary>

Lumana Core uses an AI engine for video analytics such as object recognition, behavior analysis, and anomaly detection. Those features need high-quality video input. A higher bitrate matters because:

- **Enhanced AI quality:** A higher bitrate with CBR keeps video sharp so algorithms get clear, detailed images for accurate analysis.
- **Robust AI learning:** High-quality feeds support model learning and training so behavior improves over time.
- **Efficient smart storage:** Higher bitrates use more space by default, but Lumana Core can optimize storage without sacrificing quality. Strong source quality supports real-time processing and review, and high-quality video can be retained when alerts occur so storage focuses on critical events.

</details>

<details>
<summary>What happens if the bitrate is too low?</summary>

If the bitrate is set too low, even with CBR, you may see poor video quality such as pixelation and blur, especially in high-motion or complex scenes. That can reduce how well the AI performs and limit Lumana Core’s analytics.

</details>

<details>
<summary>What should you configure when using Lumana cameras?</summary>

Nothing. Lumana default configuration already matches the recommendations on this page.

</details>