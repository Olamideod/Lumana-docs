# AXIS 
Axis cameras are fully supported in Lumana and provide reliable performance for analytics, monitoring, and enterprise deployments.

To create a new profile on the camera, follow [AXIS camera profiles (Lumana Support)](https://support.lumana.ai/hc/en-us/articles/20392123541010).

## Axis compatibility models
Here is a list of compatible Axis models.

- AXIS Q16 Series
- AXIS P13 Series
- AXIS M11 Series
- AXIS Q17 Series
- AXIS P14 Series
- AXIS Q92 Series
- AXIS Q38 Series
- AXIS Q36 Series
- AXIS P39 Series
- AXIS P38 Series
- AXIS P37 Series
- AXIS P32 Series
- AXIS M32 Series
- AXIS M31 Series
- AXIS M30 Series
- AXIS Q60 Series
- AXIS Q61 Series
- AXIS Q62 Series
- AXIS Q63 Series
- AXIS P54 Series
- AXIS P56 Series
- AXIS M50 Series
- AXIS Q86 Series (Thermal features will require additional integration)
- AXIS Q87 Series (Thermal features will require additional integration)
- AXIS Q29 Series (Thermal features will require additional integration)
- AXIS Q19 Series (Thermal features will require additional integration)

## Connecting your AXIS camera to Lumana Core

When you add the camera in Lumana Core, enter the camera's **admin** username and password. Use the stream profile steps in the next section if you still need to create or tune profiles on the camera before you connect.

## Stream configuration profiles
To ensure your Axis camera is optimally configured for Lumana Core, especially when you're handling the setup manually due to providing lower-level credentials, you'll need to create profiles for Lumana core. This is crucial for maintaining both compatibility with Lumana Core and ensuring that your video streams are of high quality and efficiency. While the details on the exact values appear on [Lumana Camera Optimal Configuration](https://support.lumana.ai/knowledge/editor/01H9FQ7552QDHFC8J11X0BSQ2R/en-us?brand_id=10899747518610) guide, below are the detailed steps for setting these values on your Axis camera

**Main stream profile**

- Login to the Axis Web Portal: Use a web browser to log into the Axis camera interface with your admin credentials. This is necessary to access and create new profile for the camera.
- Once logged in, look for the System tab, select Stream Profiles and tap on Add stream Profile


**Adjust Video Quality Settings**:

- Resolution: Select the highest available resolution for your camera. Higher resolution provides better video quality, which is essential for identification purposes and detailed monitoring.
- Frame Rate: Set the frame rate to 15fps (frames per second).
Video Encoding: If your camera supports H.265, select this option for video encoding. H.265 offers better compression, reducing file sizes and bandwidth usage without compromising video quality. If H.265 is not available, H.264 is a suitable alternative.
- Bitrate: Set bitrate based on Lumana Camera Optimal Configuration guide,


**Ensure Enhanced features are OFF**:

- Make sure that Zipstream, Dynamic FPS, Optimized GOP is turned OFF. While these enhanced compression formats can significantly reduce storage and bandwidth needs, they might not be supported or fully optimized for use with Lumana Core, potentially leading to compatibility issues.

**Set profile name**:

The profile name is used in the rtsp path once connecting the camera to Lumana core. Once setting the profile and saving, the RTSP that needs to be used t connect to Lumana core is /axis-media/media.amp?streamprofile=<profile name>.

In the example below the RTSP path that was generated is /axis-media/media.amp?profile=lumana_main

![AXIS camera web interface on Stream profiles with Add open for main stream.](../../.gitbook/assets/configuring-cameras-and-devices/connect-cameras-by-brand/axis-stream-profile-main-add.png)

**Sub stream profile**

In **System** tab, select **Stream Profiles** and tap on **Add stream Profile*

**Adjust Video Quality Settings**:

**Video Encoding**: If your camera supports H.265, select this option for video encoding. **H.265** offers better compression, reducing file sizes and bandwidth usage without compromising video quality. If H.265 is not available, H.264 is a suitable alternative.

Set the resolution, frame rate, and bit rate based on [Lumana Camera Optimal Configuration](https://support.lumana.ai/knowledge/editor/01H9FQ7552QDHFC8J11X0BSQ2R/en-us?brand_id=10899747518610) guide

**Ensure Enhanced features are OFF**:

- Make sure that Zipstream, Dynamic FPS, Optimized GOP is turned OFF. While these enhanced compression formats can significantly reduce storage and bandwidth needs, they might not be supported or fully optimized for use with Lumana Core, potentially leading to compatibility issues.
 

**Set profile name**:

The profile name is used in the rtsp path once connecting the camera to Lumana core. Once setting the profile and saving, the RTSP that needs to be used t connect to Lumana core is /axis-media/media.amp?profile=<profile name>.


In this example the RTSP path that was generated is /axis-media/media.amp?profile=lumana_sub

![AXIS camera web interface on Stream profiles with Add open for sub stream.](../../.gitbook/assets/configuring-cameras-and-devices/connect-cameras-by-brand/axis-stream-profile-sub-add.png)

With the completion of configuring both the main profile and sub profile settings on your Axis camera, you have effectively laid the groundwork for optimal integration with Lumana Core. By assigning the appropriate user credentials and fine-tuning your camera’s stream configurations, you've ensured that Lumana Core can access and manage your camera's feeds efficiently, capitalizing on high-quality recordings for event-based captures and optimizing storage through the sub profile for continuous, non-event recordings.

You are now ready to proceed to the next phase of the integration process:  [How to configure and connect Camera to Lumana core](https://support.lumana.ai/knowledge/editor/01HB6K2TVX7JF7MPZFXBJYXCRV/en-us?brand_id=10899747518610) This guide will walk you through the steps to add your Axis camera to the Lumana Core platform

