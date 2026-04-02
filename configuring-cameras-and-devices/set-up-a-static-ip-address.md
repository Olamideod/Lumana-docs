# Set up a static IP address

Assign a static IP address to ensure your camera remains reachable and does not change after reboots or network interruptions.
 

> **Note:** It is important not to allocate static IP addresses from the DHCP pool, as this can cause IP conflicts.


This guide outlines the procedure for assigning a static IP address to your camera in three scenarios.


## Choose your setup scenario

Follow the steps for your network configuration:

- **Scenario 1**: You have a DHCP server and want to reserve an IP address
- **Scenario 2**: You do not have a DHCP server
- **Scenario 3**: You want to assign a static IP outside the DHCP pool


### Scenario 1: 
Your Network Includes a DHCP Server and You Wish to Assign a Permanent IP Address

1. Connect the camera to your network

2. Find the camera's IP address and MAC address
	- Open the Lumana app
	- Go to the **Devices** list
	- Add the camera to your organization

3. Find the camera's IP address and MAC address:
	- In Lumana, open the camera from the **Devices** list.
	- Use the **IP address** shown for the camera.
 ![](../images/configuring-cameras-and-devices/devices-list-ip-address.png)
	- Open **Camera** -> **Edit camera** -> **Details** to copy the **MAC address**.
![](../images/configuring-cameras-and-devices/camera-details-mac-address.png)

4. Configure DHCP reservation on your router using the MAC address.
This ensures the camera keeps the same IP address after reboots or power interruptions.
Refer to your router documentation for instructions.

Here's an example of [static mapping configuration](https://www.cisco.com/c/en/us/td/docs/ios/12_2sb/12_2sba/feature/guide/sbhcpsm.html) for a cisco routers


### Scenario 2: Your Network Lacks a DHCP Server

If your network does not have a DHCP server, you will need to connect to the camera via the local page and configure the IP address directly on the camera.

**Default camera settings (example)**

- Default IP address for the camera is: `192.168.1.13`
- Default Subnet Mask: `255.255.255.0`
- Default user: `admin` 
- Default password: `123456`


1. Open a web browser on a device connected to the same network.

2. Enter the camera’s IP address and log in.

    ![](../images/configuring-cameras-and-devices/lumix-camera-web-login-lb800.png)

3. Change the default password when prompted.

4. Go to **Setup → Network**.
    ![](../images/configuring-cameras-and-devices/lumix-network-ipv4-dhcp-settings.png)
5. Change the network mode from DHCP to Static IP.

6. Enter your **IP address**, **subnet mask**, and **gateway**.

7. Save your changes.

![](../images/configuring-cameras-and-devices/lumix-network-ipv4-static-settings.png)


### Scenario 3: 
Use this method if you want to manually assign a static IP without DHCP reservation.
 
**Before you begin**
- Identify your network’s DHCP range
- Choose an IP address outside that range

> **Note:** Assigning an IP address within the DHCP pool can result in duplicate IP conflicts.

- Follow the same steps as in [Scenario 2](#scenario-2-your-network-lacks-a-dhcp-server) to configure the static IP on the camera.
