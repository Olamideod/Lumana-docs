# Recommended streaming settings

Lumana is designed to work with a range of IP cameras. If you're using a camera outside of the Lumana portfolio, then it is critical to correctly configure your camera before connecting it to Lumana.

If you're unsure, then use the recommended settings in the [Primary stream settings](#primary-stream-settings) and [Sub stream settings](#sub-stream-settings) sections below.

## Stream configuration overview

Most IP cameras provide at least two video streams, and some offer more.

- The *primary stream* uses the highest resolution and quality
- The *sub stream* uses lower resolution for efficiency

Lumana uses these streams for:

- AI analytics
- High-quality storage
- Standard-quality storage
- High- and standard-quality live view

Configure at least two streams to balance performance, storage, and bandwidth.

{% hint style="info" %}
If your camera only supports one stream, then you will need to balance resolution, storage retention, and live view performance.
{% endhint %}

## Primary stream settings

The primary stream is used for analytics, high-quality storage, and live monitoring.

### Recommended settings

- *Resolution*: Highest available camera resolution
- *Encoder*: H.265 (H.264 is supported but less efficient)
- *Bitrate type*: CBR (Constant Bit Rate)
- *Keyframe interval*: Equal to FPS

### Keyframe guidance

For optimal performance:

- Use at least one keyframe every 2 seconds
- In high-motion scenes, reduce the keyframe interval to match the FPS

For example:

- At *25 FPS*, keep the keyframe interval *50* or lower
- For heavy motion, set the interval to match *FPS* (for example *25* at 25 FPS)

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

- *Resolution*: 720p (or lower)
- *Encoder*: H.265
- *Bitrate type*: CBR
- *Image quality*: Medium
- *Keyframe interval*: 2 × FPS

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

{% hint style="info" %}
While some of the parameters have common terminology (for example, compression and resolution), other vendors use different terminology for camera parameters. The following table outlines the custom settings per brand:
{% endhint %}

|                 | Lumana | Axis | Hikvision | Uniview |
| --------------- | ------ | ---- | --------- | ------- |
| Main stream     |        |      |           |         |
| Bitrate type    | CBR    | MBR  | CBR       | CBR     |
| Quality         | N/A    | 100  | 100       | N/A     |
| Sub stream      |        |      |           |         |
| Bitrate type    | CBR    | ABR  | CBR       | CBR     |
| Quality         | N/A    | 60   | 60        | N/A     |

The rows group bitrate and quality targets for the main and sub streams.

#### FAQ: Navigating your camera configuration concerns

These questions cover how streaming settings affect storage, codecs, CBR, and Lumana cameras.

<details>

<summary>What happens to <a href="../faq-and-reference/video-storage.md">video storage and retention</a> if you don't follow Lumana camera configuration best practice?</summary>

Camera configuration best practice is required to bring you the best performance from Lumana Core. Not following the guidelines may impact two features:

1. The number of cameras that you can connect to a single Core may be lower than the spec.
2. The storage retention period may be lower than the spec. For more on retention, read [Video storage](../faq-and-reference/video-storage.md).

</details>

<details>

<summary>What is the impact of using H.264 instead of H.265?</summary>

When you choose H.264 over H.265 on the primary stream, consider image quality and Core performance together. H.264 is an older codec, so it compresses video less efficiently than H.265.

You may see roughly 20% lower image quality than you would at the same settings with H.265. Comparable quality then needs more bandwidth and storage.

Core performance can drop by about 40%. The extra work to decode larger H.264 streams leaves less headroom for concurrent cameras.

The next tables show camera counts and FPS targets for each codec.

#### Primary stream impact

|     | Resolution | FPS | H.265 cameras | H.264 cameras |
| --- | ---------- | --- | ------------- | ------------- |
| 2MP | 1920×1080  | 15  | 10            | 10            |
| 4MP | 2560×1440  | 15  | 10            | 6             |
| 5MP | 2880×1620  | 15  | 10            | 6             |
| 8MP | 3480×2160  | 10  | 8             | 5             |

#### Sub stream impact

| Main stream   | Sub stream | H.265 FPS | H.264 FPS |
| ------------- | ---------- | --------- | --------- |
| 5MP or lower  | 1280×720   | 25        | 20        |
| 8MP or higher | 1920×1080  | 25        | 15        |

</details>

<details>

<summary>Why use CBR when connecting to Lumana Core?</summary>

Lumana Core requires IP cameras to use CBR for several important reasons:

- *Stability and reliability*: CBR keeps a steady data rate. That consistency helps live view and recording stay predictable.
- *Network bandwidth management*: With CBR, you can plan bandwidth per camera so each stream gets enough capacity for usable video.

</details>

<details>

<summary>Why is a high bitrate important for CBR on Lumana Core?</summary>

Lumana Core runs video analytics, including object recognition, behavior analysis, and anomaly detection. Those features need clear input video. Here is why bitrate matters with CBR:

- *Analytics quality*: A higher CBR bitrate keeps more detail in the image. Clearer frames help detection stay accurate.
- *Model learning*: Steady, high-quality feeds support training and tuning of analytics models over time.
- *Storage with alerts*: Higher bitrates use more disk space by default. Lumana Core still targets efficient storage. It keeps rich video for review when alerts fire, without storing bulk high-bitrate footage when nothing is happening.

</details>

<details>

<summary>What happens if the bitrate is too low?</summary>

If the bitrate is set too low, then video can look blocky or soft, even on CBR. That is common in busy scenes or when lots of motion is on screen.

Poor image quality limits what the analytics can read reliably. Core functionality that depends on clean video may then underperform.

</details>

<details>

<summary>What should you configure when using Lumana cameras?</summary>

Nothing. The default Lumana camera configuration matches the recommended streaming settings on this page.

</details>
