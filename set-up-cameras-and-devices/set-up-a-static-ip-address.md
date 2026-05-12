# Set up a static IP address

Assign a static IP address so your camera keeps the same IP after reboots or when DHCP would otherwise supply a new address.

Lumana and other systems can keep using that one address for the camera.

## Choose your setup scenario

Follow the scenario below that matches your network.

- **Scenario 1**: Your network has a DHCP server and you want a permanent address. Keep the camera on DHCP and reserve its address on the router or Core so the camera always gets the same IP.
- **Scenario 2**: Your network has a DHCP server but you want a static IP on the camera itself. Set a fixed **IP address**, **subnet mask**, and **gateway** on the camera, outside the DHCP pool.
- **Scenario 3**: Your network has no DHCP server. No device hands out DHCP leases. Configure the camera's IP in its local web interface (you may need a temporary static IP on your PC first).

If you are not sure whether your network uses DHCP, then use the following subsection to pick Scenario 1, 2, or 3.

### How do I know if I have a DHCP server?

_DHCP_ stands for Dynamic Host Configuration Protocol. That service assigns each device an IP address automatically, usually from a range your router, firewall, or Lumana Core manages. Devices can then communicate without manual IP entry on each device.

You likely have DHCP when a router, office firewall, or Lumana Core on your network assigns addresses to devices. Your camera might already show an IP in Lumana before you set a static address on the device. Check your router or Core admin UI for DHCP or LAN settings if you are unsure.

You likely do not have DHCP if every device uses manually entered IPs and nothing on the subnet offers leases. Use Scenario 3 in that case.

### Reserve an IP for a camera on a DHCP network

1. Connect the camera to your network.
2. In Lumana, collect the **IP address** and **MAC address** you map on the DHCP server. If the camera is not listed under **Devices** yet, [add the camera to your organization](../getting-started/connect-a-camera.md#connect-a-camera) first.
   - From **Devices**, choose the camera and note the **IP address**.

   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/devices-list-ip-address.png" alt="Devices list showing the IP address column for cameras grouped by location; MAC address column also visible." width="563"></div>

   - Select the **Edit camera** icon <img src="../.gitbook/assets/edit-camera-icon-inline.png" alt="Edit camera pencil icon." data-size="line">, then select **Details** and copy the **MAC address**.

   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/camera-details-mac-address.png" alt="Edit camera, Details tab, showing the MAC address field." width="563"></div>

{% hint style="warning" %}
Do not forget to create a DHCP reservation for the camera’s address on the router or Core. Otherwise, the server can still offer that address to another device, and you can get an IP conflict.
{% endhint %}


3. Configure a DHCP reservation on your router using the MAC address.

   The server always offers the same lease to that MAC address, so the camera keeps the same IP after reboots or power interruptions. Refer to your router documentation for instructions.

Here is an example of [static mapping configuration](https://www.cisco.com/c/en/us/td/docs/ios/12_2sb/12_2sba/feature/guide/sbhcpsm.html) for Cisco routers.

### Set a static IP outside the DHCP pool

Assign a static IP on the camera itself and skip a DHCP reservation on the server. DHCP can keep running on the network for other devices.

Before you choose the camera’s IP, identify which addresses on your network sit outside the DHCP pool. Check your router or DHCP server documentation for the pool boundaries and any range your organization reserves for static devices.

- Identify your network’s DHCP pool range.
- Choose an IP address outside that range.
- Do not use an in-pool address unless you also create a DHCP reservation for it. Otherwise, DHCP may assign the same address to another device and cause duplicate IP conflicts.

When you have an address picked out, follow [Assign a static IP without a DHCP server](#assign-a-static-ip-without-a-dhcp-server). Use that section's first step only when the camera does not get an address automatically.

### Assign a static IP without a DHCP server

If your network does not have a DHCP server, connect to the camera’s local page and configure the IP address on the camera.

{% hint style="info" %}
The steps and screenshots below show one example camera's local web interface. Your camera's login screen, menu names, defaults, and layout may differ.
{% endhint %}

The example below assumes these factory defaults on the camera (your labels may differ):

- Default IP address for the camera is: `192.168.1.13`
- Default Subnet Mask: `255.255.255.0`
- Default user: `admin`
- Default password: `123456`

1. If the camera didn't receive an address automatically, then assign a temporary static IP to your computer on the same subnet as the camera. For example, `192.168.1.10`, subnet mask `255.255.255.0`.

{% hint style="info" %}
If you need step-by-step instructions, then refer to your computer or operating system documentation for setting a temporary static IP address.
{% endhint %}

2. Open a web browser on a computer on the same network as the camera. Enter the camera IP address in the address bar to open the configuration page.

3. Enter the camera **username** and **password** on the login page, then sign in.

    <div align="center" data-with-frame="true"><img src="../.gitbook/assets/lumix-camera-web-login-lb800.png" alt="Camera local web interface login page." width="563"></div>

4. Change the default password when prompted, then record the new credentials where your team expects them.

5. Go to **Setup → Network**.
    <div align="center" data-with-frame="true"><img src="../.gitbook/assets/lumix-network-ipv4-dhcp-settings.png" alt="Camera network settings showing IPv4 DHCP mode." width="563"></div>

6. Change the **network mode** from **DHCP** to **Static IP**.

7. Enter your **IP address**, **subnet mask**, and **gateway**.

8. Select **Save** to apply your changes.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/lumix-network-ipv4-static-settings.png" alt="Camera network settings showing static IP, subnet mask, and gateway." width="563"></div>

## Next steps

- Use [Connect cameras by brand](connect-cameras-by-brand/README.md) for brand-specific setup details after the camera has a stable address.
- Read [Configure Lumana Core as a DHCP server](network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md) if you want Lumana to manage reservations directly.
- Use [Camera networking options](camera-networking-options.md) to review how the camera connects to Lumana on your network.
