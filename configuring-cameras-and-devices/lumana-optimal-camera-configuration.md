# Lumana optimal camera configuration

Reference material for how Lumana expects camera streams to behave, including defaults on Lumana cameras, supported-brand automation, and the impact of codec and bitrate choices.

## Lumana cameras

When using Lumana cameras, the default settings already match Lumana camera configuration recommendations. No further action is needed.

## Supported brand optimized configuration

When adding a camera with optimized configuration on supported brands, Lumana Core automatically configures the camera with the recommended settings. While some of the parameters have common terminology (for example, compression and resolution), other vendors use different terminology for camera parameters. The following table outlines the custom settings per brand:

 	Lumana	Axis	Hikvision	Uniview
Main stream
Bitrate Type	CBR	MBR	CBR	CBR
Quality	N/A	100	100	N/A
Sub stream
Bitrate Type	CBR	ABR	CBR	CBR
Quality	N/A	60	60	N/A

## FAQ

### What happens to video storage if I don't follow [Lumana camera configuration best practices](https://support.lumana.ai/knowledge/articles/11867496430354/en-us?brand_id=10899747518610)?

Camera configuration best practice is required to bring you the best performance from Lumana Core. Not following the guidelines may impact two features:

1. Number of cameras that can be connected to a single Core may be lower than the spec.

2. Storage retention period may be lower than the spec. For more info on storage retention period please refer to [Lumana Video Storage: Revolutionizing Video Security Retention](https://support.lumana.ai/knowledge/articles/11078121786386/en-us?brand_id=10899747518610)

### What is the impact of using H.264 instead of H.265?

When choosing H.264 over H.265 on primary stream, it's important to consider the impact on both image quality and Lumana Core performance. Opting for H.264 can lead to a reduction in image quality of approximately 20%. This is because H.264, being an older codec, is less efficient at compressing video data, requiring more bandwidth and storage to maintain comparable quality levels. Furthermore, the core performance can suffer a significant reduction, by as much as 40%. This decrease in performance stems from the additional processing power required to handle the larger, less efficient H.264 files. As a result, the system's ability to manage multiple video streams concurrently is diminished, reducing the total number of cameras that can be connected to Lumana Core.

**Primary stream impact**

Main stream resolution	Resolution	FPS	H265 cameras	H264 cameras
2MP	1920x1080	15	10	10
4MP	2560x1440	15	10	6
5MP	2880x1620	15	10	6
8MP	3480x2160	10	8	5

**Sub stream impact**

Main stream resolution	Sub stream resolution	H265 FPS	H264 FPS
5MP or lower	1280x720	25	20
8MP or higher	1920x1080	25	15

### Why use CBR when connecting to Lumana Core?

Lumana Core requires IP cameras to use CBR for several important reasons:

Stability and Reliability: CBR provides a consistent data stream that helps maintain stable and reliable video transmission, which is crucial for real-time monitoring and recording.

Network Bandwidth Management: Using CBR allows network administrators to effectively manage and allocate network bandwidth, ensuring that each camera receives adequate resources to transmit high-quality video.

### Why is a high bitrate important for CBR on Lumana Core?

Lumana Core employs a novel AI engine designed to perform sophisticated video analytics, such as object recognition, behavior analysis, and anomaly detection. For optimal performance of these AI functionalities, high-quality video input is essential. Here’s why a high bitrate is crucial:

1. **Enhanced AI Quality**: A higher bitrate with CBR ensures that the video maintains high quality, providing the AI algorithms with clear and detailed images necessary for accurate analysis.

2. **Robust AI Learning**: High-quality video feeds enhance the AI model's learning and training processes, leading to more effective and efficient AI behavior over time.

3. **Efficient Smart Storage Utilization**:  Although higher bitrates typically require more storage space, Lumana Core integrates smart storage solutions that optimize data storage without compromising video quality. By maintaining a high bitrate, the system ensures that video data is of sufficient quality for both real-time processing and retrospective analysis, making sure the high-quality video is stored when alerts occur. This approach maximizes the utility and efficiency of storage, preserving detailed video only during critical events.

### What happens if the bitrate is too low?

If the bitrate is set too low, even on CBR, it may lead to poor video quality, characterized by pixelation and blurring, especially in scenes with high motion or complexity. This degradation in video quality can severely impair the AI’s ability to perform accurate analytics, leading to compromised functionality of Lumana Core’s AI engine.

### What should I configure when using Lumana cameras?

Nothing. Lumana default configuration fits [Lumana Optimal Camera Configuration](https://support.lumana.ai/knowledge/articles/11867496430354/en-us?brand_id=10899747518610) requirements.
