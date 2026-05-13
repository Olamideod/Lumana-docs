# Connect Lumana cameras

Dome, Bullet, and Turret quick start PDFs plus Lumana Camera Finder reference material from the prior documentation set.

If you have questions, contact [support@lumana.ai](mailto:support@lumana.ai).

## Prerequisites

- Physical access to Lumana cameras and a Windows or macOS PC on the same LAN for Camera Finder.
- Administrator credentials for cameras you will configure.
- A Lumana organization where you can [add cameras](../../getting-started/connect-a-camera.md#connect-a-camera) after network setup.

## Quick start PDFs

- [Turret quick start (PDF)](https://support.lumana.ai/hc/en-us/article_attachments/17249698970770)
- [Bullet quick start (PDF)](https://support.lumana.ai/hc/en-us/article_attachments/17249693176210)
- [Dome quick start (PDF)](https://support.lumana.ai/hc/en-us/article_attachments/17249698971026)

## Download Lumana Camera Finder

The Lumana Camera Finder is an external application for Windows PCs and macOS. It helps you batch configure and manage Lumana-branded cameras before installation.

Use it from a computer on the same local area network (LAN) as the cameras when you run discovery.

- [Download Camera Finder for Windows (Google Drive)](https://drive.google.com/file/d/1r-jZcDPfi7JrTTHKFjIRG1BGrq1rggeG/view?usp=sharing)
- [Download Camera Finder for macOS (Google Drive)](https://drive.google.com/file/d/1jxiqh_opqocBNdHJ5_VIQwqWI-a9F598/view?usp=sharing)

## Device search

The software scans for devices on the LAN where the PC is connected and lists discovered devices. You can search by MAC address or within a specific IP range for more precise results.

You need to log in to the devices before you change the configuration.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/set-up-cameras-and-devices/connect-cameras-by-brand/lumana/camera-finder-device-management.png" alt="Lumana Camera Finder device list with discovered cameras; model names depend on hardware." width="563"></div>

## Management and configuration

The following capabilities are available for bulk operations across multiple devices:

- **Manage device passwords**: Change from the default password to unique, secure passwords for each camera.
- **Additional bulk configuration**: System time, daylight saving time (DST), DNS, port settings, Universal Plug and Play (UPnP), and ONVIF protocols.

The following features are available for individual cameras only:

- **Change device IP address**: Assign a static address or update DHCP results before the camera joins Lumana.
- **Camera name**: Edit the label operators see in Lumana.
- **Restore default settings**: Reset a camera to its factory configuration.

## Import and export configuration

### Import configuration

Upload a configuration file from your computer to a device so the device’s current settings follow the imported file.

### Export configuration

Save the current configuration of a device as a file for backup or replication purposes.

## Debugging and support

If you run into camera issues, then the Lumana Camera Finder application offers debugging tools. You can retrieve the device’s serial number and access diagnostic information through the advanced menu. You can provide this data to Lumana Support for further troubleshooting.

## Next steps

- [Connect a camera](../../getting-started/connect-a-camera.md#connect-a-camera) in the Lumana portal after cameras are on the network.
- Use [Set up a static IP address](../set-up-a-static-ip-address.md) when cameras need fixed addresses before discovery.
- Return to [Connect cameras by brand](README.md) for other manufacturers mixed into the same site.
