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

To add the camera in Lumana Core, enter the camera's **admin** username and password. Use the stream profile steps in the next section if you still need to create or tune profiles on the camera before you connect.

## Stream configuration profiles
If Lumana cannot create the required stream profiles automatically, you can configure them manually on the Axis camera before connecting it. Use the recommended values from [Recommended streaming settings](../recommended-streaming-settings.md), then follow the steps below to create the profiles in the Axis interface.

Before creating the stream profiles:

- **Log in to the Axis Web Portal:** Use a web browser to log into the Axis camera interface with your admin credentials.
- **Open Stream Profiles:** In the *System* tab, select *Stream Profiles* and click *Add stream Profile*.
- **Turn enhanced features off:** Set *Zipstream*, *Dynamic FPS*, and *Optimized GOP* to *Off*. These features can cause compatibility issues with Lumana Core.
- **Set a profile name:** The profile name is used in the [Real Time Streaming Protocol (RTSP)](../../faq-and-reference/lumana-glossary.md#rtsp) path when connecting the camera to Lumana Core. After you save the profile, use `/axis-media/media.amp?streamprofile=<profile name>` as the RTSP path in Lumana Core.

**Main stream profile**

- **Resolution:** Select the highest available resolution for your camera.
- **Frame Rate:** Set the frame rate to `15fps`.
- **Video Encoding:** If your camera supports **H.265**, select this option for video encoding. If **H.265** is not available, **H.264** is a suitable alternative.
- **Bitrate:** Set bitrate based on the [Recommended streaming settings](../recommended-streaming-settings.md) guide.
- **Profile name:** In the example below the RTSP path that was generated is `/axis-media/media.amp?profile=lumana_main`

![AXIS Stream profiles, main stream Add form.](../../.gitbook/assets/configuring-cameras-and-devices/connect-cameras-by-brand/axis-stream-profile-main-add.png)

**Sub stream profile**

- **Video Encoding:** If your camera supports **H.265**, select this option for video encoding. If **H.265** is not available, **H.264** is a suitable alternative.
- **Resolution, Frame Rate, and Bitrate:** Set these values based on the [Recommended streaming settings](../recommended-streaming-settings.md) guide.
- **Profile name:** In this example the RTSP path that was generated is `/axis-media/media.amp?profile=lumana_sub`

![AXIS Stream profiles, sub stream Add form.](../../.gitbook/assets/configuring-cameras-and-devices/connect-cameras-by-brand/axis-stream-profile-sub-add.png)

After both profiles are saved, return to Lumana Core and connect the camera using its **admin** credentials.

