# Recommended setup tasks

This guide walks you through configuring cameras, connected devices, and the network settings Lumana needs to run reliably.

By the end, you'll have cameras streaming to Lumana Core. The rest of your network stack satisfies live monitoring, event detection, and video search workloads.

## What you’ll achieve

After completing this section, you can:

* Connect and configure supported cameras.
* Optimize streaming settings and camera performance.
* Integrate supported devices such as sensors, storage, and GPIO.
* Configure network and infrastructure requirements.

## Prerequisites

Make sure you have:

* Access to your network configuration (router, firewall, or DHCP settings).
* Physical access to the cameras and devices you're configuring.
* Supported hardware.
* Administrator access to Lumana Core.

## Suggested setup order

When you are ready to set up cameras and devices, use this list as a simple order to follow. You can change the order if your IT staff or camera installers work differently.

1. **[Set up a static IP address](set-up-a-static-ip-address.md)**: Plan stable IP assignments or reservations for cameras and Core so devices keep the same addresses.
2. **[Connect cameras by brand](connect-cameras-by-brand/)**: Add supported cameras to Lumana and finish the steps for each manufacturer.
3. **[Recommended streaming settings](recommended-streaming-settings.md)**: Apply encoder, bitrate, and resolution defaults so feeds behave well on your network.

### Recommended for most sites

4. **[Set up a camera floor plan](set-up-a-camera-floor-plan.md)**: Place cameras on a floor plan so operators can navigate faster.
5. **[Create camera shortcuts](create-camera-shortcuts.md)**: Add on-image links to jump between related live views.

### If your cameras support pan, tilt, and zoom

6. **[Enable PTZ control](enable-ptz-control.md)**

## Other topics in this section

The pages below cover optional or situational setup: remote access to a camera’s web UI, integrations such as storage and sensors, and Lumana Core networking requirements.

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/icon-link.svg" alt=""></td><td><strong>Camera networking options</strong></td><td>Use Camera VPN to open a camera manufacturer’s web interface when you are off the camera LAN.</td><td><a href="camera-networking-options.md">camera-networking-options.md</a></td></tr><tr><td><img src="../.gitbook/assets/icon-wrench.svg" alt=""></td><td><strong>Other devices</strong></td><td>Connect storage, sensors, GPIO, smart speakers, and other supported devices.</td><td><a href="other-devices/">other-devices</a></td></tr><tr><td><img src="../.gitbook/assets/icon-settings.svg" alt=""></td><td><strong>Network and infrastructure configuration</strong></td><td>Firewall rules, DHCP, NTP, and Core hardware requirements.</td><td><a href="network-and-infrastructure-configuration/">network-and-infrastructure-configuration</a></td></tr></tbody></table>
