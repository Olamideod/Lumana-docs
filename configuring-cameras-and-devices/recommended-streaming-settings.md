# Recommended streaming settings

Lumana is designed to integrate seamlessly with a range of IP cameras. If you’re using a camera outside of the Lumana portfolio, configure your camera streams before you connect the device to Lumana.

Use the steps below for **primary** and **sub** stream settings. For Lumana camera defaults, supported-brand automation, codec impact, and FAQs, see [Lumana optimal camera configuration](lumana-optimal-camera-configuration.md).

## Stream configuration

Most IP cameras provide at least two video streams, with some offering three or more. These consist of a primary stream with the highest resolution and a secondary stream with lower resolution. Lumana uses these video streams for multiple purposes, including the following:

- Analytics
- Standard-quality storage
- High-quality storage
- Standard-quality live view
- High-quality live view

We recommend configuring your camera with at least two streams: the primary stream for maximum resolution and quality and a secondary stream for additional functions like standard-quality live view. If your camera only supports one stream, you’ll need to strike a balance between the benefits of high-resolution analytics and the considerations of storage duration and live-view bandwidth.

### Primary stream

The primary stream is used for analytics, high-quality storage, and live view.

Recommended settings for the main stream, assuming you’re also using the sub stream:

1. Resolution: highest camera resolution from the table below
2. Encoder: H265 (H264 is less preferred but also acceptable)
3. CBR (Constant Bit Rate)
4. Keyframe intervals: same as FPS

(*) Generally, you want the highest frame rate and at least one keyframe every 2 seconds. For example, if your camera is at 25 fps, your keyframe interval should be no higher than 50. If you have a lot of motion in the scene, reduce the keyframe interval until it is equal to the FPS. For example, if the camera is at 25 fps, set the keyframe interval to 25.

 	Resolution	FPS	Bitrate (Kbps)
VGA (16:9)	640x360	15	800
VGA	640X480	15	800
HD	1280x720	15	1,800
2MP	1920x1080	15	2,048
3MP	3072x1028	15	3,084
4MP	2560x1440	15	3,584
5MP	2592x1944	15	3,584
5MP	2880x1620	15	3,584
8MP	3480x2160	10	5,120
12MP	4000x3000	10	6,144

### Sub stream

This stream is used for standard-quality storage.

Recommended settings for the sub stream:

1. Resolution: see below
2. Encoder: H265
3. CBR
4. Image quality: medium
5. Keyframe intervals: same as FPS x 2

 	Resolution	FPS	Bitrate (Kbps)
VGA (16:9)	640x360	25	700
VGA	640x480	25	700
HD	1280x720	25	700
2MP	1280x720	25	700
3MP	1280x720	25	700
4MP	1280x720	25	700
5MP	1280x720	25	700
5MP	1280x720	25	700
8MP	1920x1080	25	1,024
12MP	1920x1080	25	1,024
