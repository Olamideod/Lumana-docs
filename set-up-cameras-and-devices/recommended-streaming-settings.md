# Recommended streaming settings

Use this page to see how your primary and sub streams should look for Lumana. If you use Lumana cameras or a supported brand that Lumana Core sets up for you, then you might not need to change anything. Otherwise copy the values from [Primary stream settings](#primary-stream-settings) and [Sub stream settings](#sub-stream-settings) into the camera’s own settings.

## Stream configuration overview

Most IP cameras provide at least two video streams, and some offer more.

- The primary stream uses the highest resolution and quality
- The sub stream uses lower resolution for efficiency

Lumana uses these streams for:

- AI analytics
- High-quality storage
- Standard-quality storage
- High-quality live view
- Standard-quality live view

Configure at least two streams to balance performance, storage, and bandwidth.

{% hint style="info" %}
If your camera only supports one stream, then you need to balance resolution, storage retention, and live view performance.
{% endhint %}

## Primary stream settings

The primary stream is used for analytics, high-quality storage, and live monitoring.

### Recommended settings

- **Resolution**: Highest available camera resolution
- **Encoder**: H.265 (H.264 is supported but less efficient)
- **Bitrate type**: CBR (Constant Bit Rate)
- **Keyframe interval**: Equal to FPS

### Keyframe guidance

For optimal performance:

- Use at least one keyframe every 2 seconds
- In high-motion scenes, reduce the keyframe interval to match the FPS

For example:

- At 25 FPS, keep the keyframe interval 50 or lower
- For heavy motion, set the interval to match FPS (for example 25 at 25 FPS)

### Reference values

|            | Resolution | FPS | Bitrate (Kbps) |
| ---------- | ---------- | --- | -------------- |
| VGA (16:9) | 640×360    | 15  | 800            |
| VGA        | 640×480    | 15  | 800            |
| HD         | 1280×720   | 15  | 1,800          |
| 2MP        | 1920×1080  | 15  | 2,048          |
| 3MP        | 3072×1728  | 15  | 3,084          |
| 4MP        | 2560×1440  | 15  | 3,584          |
| 5MP        | 2592×1944  | 15  | 3,584          |
| 5MP        | 2880×1620  | 15  | 3,584          |
| 8MP        | 3840×2160  | 10  | 5,120          |
| 12MP       | 4000×3000  | 10  | 6,144          |

## Sub stream settings

The sub stream is used for standard-quality storage and bandwidth optimization.

### Recommended settings

- **Resolution**: 720p (or lower)
- **Encoder**: H.265
- **Bitrate type**: CBR
- **Image quality**: Medium
- **Keyframe interval**: 2 × FPS

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

## Lumana cameras

When using Lumana cameras, default settings already match recommended configuration.

No additional setup is required.

### Supported brand optimization

When you add a camera from a **supported brand**, Lumana Core updates its streaming options so they match the recommendations on this page.

{% hint style="info" %}
Many options use familiar names such as compression and resolution, but vendors label those settings differently.
{% endhint %}

The table below lists bitrate type and quality targets for the main and sub streams by brand.

|                 | Lumana | Axis | Hikvision | Uniview |
| --------------- | ------ | ---- | --------- | ------- |
| Main stream     |        |      |           |         |
| Bitrate type    | CBR    | MBR  | CBR       | CBR     |
| Quality         | N/A    | 100  | 100       | N/A     |
| Sub stream      |        |      |           |         |
| Bitrate type    | CBR    | ABR  | CBR       | CBR     |
| Quality         | N/A    | 60   | 60        | N/A     |


### Frequently asked questions

These questions cover how streaming settings affect storage, codecs, CBR, and Lumana cameras.

<details>

<summary>What happens to <a href="../faq-and-reference/video-storage.md">video storage and retention</a> if you don't follow Lumana camera configuration best practices?</summary>

Camera configuration best practices help Lumana Core reach its expected performance. If you do not follow the guidelines, then you might see lower results in two areas:

1. You may connect fewer cameras to a single Core than the specification describes.
2. Your storage retention period may be shorter than the specification describes. For more on retention, read [Video storage](../faq-and-reference/video-storage.md).

</details>

<details>

<summary>What is the impact of using H.264 instead of H.265?</summary>

When you choose H.264 over H.265 on the primary stream, weigh image quality and Core performance together. H.264 is an older codec and compresses video less efficiently than H.265.

- You may see roughly 20% lower image quality than at the same settings with H.265. Matching that quality needs more bandwidth and storage.
- Core performance can drop by about 40%. The extra work to decode larger H.264 streams leaves less headroom for concurrent cameras.

The tables below show camera counts and FPS targets for each codec.

### Primary stream impact

|     | Resolution | FPS | H.265 cameras | H.264 cameras |
| --- | ---------- | --- | ------------- | ------------- |
| 2MP | 1920×1080  | 15  | 10            | 10            |
| 4MP | 2560×1440  | 15  | 10            | 6             |
| 5MP | 2880×1620  | 15  | 10            | 6             |
| 8MP | 3840×2160  | 10  | 8             | 5             |

### Sub stream impact

| Main stream   | Sub stream | H.265 FPS | H.264 FPS |
| ------------- | ---------- | --------- | --------- |
| 5MP or lower  | 1280×720   | 25        | 20        |
| 8MP or higher | 1920×1080  | 25        | 15        |

</details>

<details>

<summary>Why use CBR when connecting to Lumana Core?</summary>

Lumana Core requires IP cameras to use **CBR** (constant bit rate) for several important reasons:

- **Stability and reliability**: CBR keeps a steady data rate. That consistency helps live view and recording stay predictable.
- **Network bandwidth management**: With CBR, you can plan bandwidth per camera so each stream gets enough capacity for usable video.

</details>

<details>

<summary>Why does bitrate need to be high enough when you use CBR with Lumana Core?</summary>

Lumana Core uses an **AI engine** for video analytics, including object recognition, behavior analysis, and anomaly detection. Those features work best when the incoming video is detailed and stable. With **CBR**, a bitrate set **high enough** keeps that quality consistent. Here is what you gain:

- **Accurate AI analysis**: A higher bitrate with CBR preserves more detail in each frame, so AI algorithms get the clear images they need for reliable results.
- **Stronger AI learning over time**: High-quality feeds support AI model training and tuning, which helps detection and behavior stay effective as your deployment runs.
- **Smarter storage around alerts**: Higher bitrates usually mean more data. Lumana Core still uses **smart storage** so you are not wasting space. Video stays high enough quality for **live processing** and **retrospective review**. When alerts fire, Lumana keeps richer recordings. That prioritizes detail for **critical events** without hoarding bulk high-bitrate footage when nothing important is happening.

</details>

<details>

<summary>What happens if the bitrate is too low?</summary>

If the bitrate is set too low, even on CBR, then video quality may suffer, with pixelation and blurring in scenes with high motion or complexity. Lower quality reduces the AI's ability to perform accurate analytics, which compromises Lumana Core's AI engine.

</details>

<details>

<summary>What should you configure when using Lumana cameras?</summary>

Nothing. The default Lumana camera configuration matches the recommended streaming settings on this page.

</details>
