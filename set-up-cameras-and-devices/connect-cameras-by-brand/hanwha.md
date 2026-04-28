# Hanwha

Hanwha Wisenet cameras are supported in Lumana for analytics, monitoring, and typical enterprise deployments.

## Supported Hanwha models

Supported Hanwha Wisenet series:

* Hanwha Wisenet P Series
* Hanwha Wisenet X Series
* Hanwha Wisenet T Series (thermal features require additional integration)
* Hanwha Wisenet A Series
* Hanwha Wisenet L Series

## Connect your Hanwha camera to Lumana Core

This guide explains how to connect your Hanwha camera to Lumana Core. If needed, you can connect using the admin credentials, an ONVIF profile, or a new profile.

Choose the connection method that fits your setup:

* **Admin credentials:** Best option when available. Gives Lumana the highest level of access and compatibility.
* **ONVIF:** Useful when you need a standards-based connection.
* **New profile:** Useful when you do not want to use the admin account directly and want to manage access separately.

{% hint style="info" %}
Using reduced-permission accounts may limit some functionality in Lumana.
{% endhint %}

{% hint style="success" %}
Use the camera's admin username and password when possible. This provides the highest level of compatibility and access.
{% endhint %}

## Prepare your Hanwha camera

Ensure your Hanwha camera is updated, correctly configured, and ready to connect, whether using admin credentials, an ONVIF profile, or a new profile.

### Set an IP address

Assign a static IP through the web interface or Wisenet device manager. A static IP is recommended to ensure a consistent connection to Lumana Core.

For general guidance, see [Set up a static IP address](../set-up-a-static-ip-address.md).

This can be done under **Basic** -> **IP and port**.

### Configure the profile on your Hanwha camera

1. Log into the Hanwha Web Portal
2. Under **Basic** -> **Video Profile**, select the video profile name you would like to use.

(In the example below the selected profile is called H.265 and it is profile 3)

Note: you can always use the **Add** button to add another video profile.

3. Make that profile the default profile and select codec H.265.
4. Configure the main profile:

* Disable ATC mode
* Frame rate should be 15
* Target bit rate follow the [Recommended streaming settings](../recommended-streaming-settings.md)
* Bitrate control CBR
* GOV length 15
* Smart Codec disabled
* Dynamic GOV disable
* Dynamic FPS disabled

5. Create the storage substream profile:

* Select or add another profile, name it **Storage**.
* In the below example it will be profile 4.
* Make sure to select codec H.265 for it.

6. Configure the storage profile:

* Disable ATC mode
* Frame rate should be 20-30
* Target bit rate follow the [Recommended streaming settings](../recommended-streaming-settings.md)
* Bitrate control CBR
* GOV length 2x frame rate
* Smart Codec disabled
* Dynamic GOV disable
* Dynamic FPS disabled

7. Add camera to Core

[Follow Connect a camera](../../getting-started/connect-a-camera.md)

Use the following [Real Time Streaming Protocol (RTSP)](https://github.com/Olamideod/Lumana-docs/blob/main/faq-and-reference/lumana-glossary.md#rtsp) paths based on the profiles above:

Main stream: `/0/profile3/media.smp or /profile3/media.smp`

Substream (Storage): `/0/profile4/media.smp or /profile4/media.smp`

Voila, You’re all set!
