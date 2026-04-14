# Set up a static IP address

Assign a static IP address to ensure your camera remains reachable and does not change after reboots or network interruptions.
> **Note:** It is important not to allocate static IP addresses from the DHCP pool, as this can cause IP conflicts.

This guide outlines the procedure for assigning a static IP address to your camera in three scenarios.

## Choose your setup scenario

Follow the steps for your network configuration:

- **Scenario 1**: You have a DHCP server and want to reserve an IP address
- **Scenario 2**: You do not have a DHCP server
- **Scenario 3**: You want to assign a static IP outside the DHCP pool

### Scenario 1: Your network includes a DHCP server and you wish to assign a permanent IP Address

1. Connect the camera to your network
2. Find the camera's IP address and MAC address
   - Open the Lumana app
   - Go to the **Devices** list
   - Add the camera to your organization
3. Find the camera's IP address and MAC address:
   - In Lumana, open the camera from the **Devices** list.
   - Use the **IP address** shown for the camera.

 <div align="center" data-with-frame="true"><img src="../.gitbook/assets/devices-list-ip-address.png" alt="Devices list showing the camera IP address."></div>

   - Open **Camera** -> **Edit camera** -> **Details** to copy the **MAC address**.

 <div align="center" data-with-frame="true"><img src="../.gitbook/assets/camera-details-mac-address.png" alt="Camera details page showing the MAC address field."></div>

4. Configure DHCP reservation on your router using the MAC address.
This ensures the camera keeps the same IP address after reboots or power interruptions.
Refer to your router documentation for instructions.

Here's an example of [static mapping configuration](https://www.cisco.com/c/en/us/td/docs/ios/12_2sb/12_2sba/feature/guide/sbhcpsm.html) for Cisco routers.

### Scenario 2: Your network lacks a DHCP server

If your network does not have a DHCP server, you will need to connect to the camera via the local page and configure the IP address directly on the camera.

**Default camera settings (example)**

- Default IP address for the camera is: `192.168.1.13`
- Default Subnet Mask: `255.255.255.0`
- Default user: `admin`
- Default password: `123456`

1. If your device is not receiving an IP address automatically, assign a temporary static IP address on the same subnet as the camera (for example, `192.168.1.10` with subnet mask `255.255.255.0`).

> **Note:** If needed, refer to your computer or operating system documentation for instructions on setting a temporary static IP address.

2. Open a web browser on a device connected to the same network.

3. Enter the camera’s IP address and log in.

    <div align="center" data-with-frame="true"><img src="../.gitbook/assets/lumix-camera-web-login-lb800.png" alt="Camera local web interface login page."></div>

4. Change the default password when prompted.

5. Go to **Setup → Network**.
    <div align="center" data-with-frame="true"><img src="../.gitbook/assets/lumix-network-ipv4-dhcp-settings.png" alt="Camera network settings showing IPv4 DHCP mode."></div>

6. Change the network mode from DHCP to Static IP.

7. Enter your **IP address**, **subnet mask**, and **gateway**.

8. Save your changes.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/lumix-network-ipv4-static-settings.png" alt="Camera network settings showing static IP, subnet mask, and gateway."></div>

### Scenerio 3: Assign a static IP outside the DHCP pool

Use this method if you want to manually assign a static IP without DHCP reservation.

**Before you begin**

- Identify your network’s DHCP range
- Choose an IP address outside that range

> **Note:** Assigning an IP address within the DHCP pool can result in duplicate IP conflicts.

- Follow the same steps as in [Scenario 2](#scenario-2-your-network-lacks-a-dhcp-server) to configure the static IP on the camera.
