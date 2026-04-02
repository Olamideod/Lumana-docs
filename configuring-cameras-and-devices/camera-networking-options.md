# Camera networking options


Configure how your cameras connect to and communicate within your network, including remote access and audio integrations.

This page covers common networking options used when managing cameras in Lumana.
 

## Remote camera access (Camera VPN)

Use Camera VPN to securely access your camera’s native interface through Lumana without exposing it directly to the internet.

### When to use this

- You need to access camera settings remotely  
- You want to configure manufacturer-specific features  
- Your camera is behind a private network  

### Steps

1. Open the camera from the **Devices** list.

2. Click the **VPN icon** in the top-right corner of the camera player.

![Camera player live view with timeline scrubber](../images/configuring-cameras-and-devices/camera-player-live-view-timeline.png)

3. You will be redirected to the camera manufacturer’s login page.

![Manufacturer VPN login redirect](../images/configuring-cameras-and-devices/manufacturer-vpn-login-redirect.png)

4. Enter your camera credentials to log in.

![Hikvision manufacturer login page](../images/configuring-cameras-and-devices/hikvision-manufacturer-login.png)

5. Configure camera settings as needed.

> The available settings depend on the camera manufacturer. Refer to the manufacturer’s documentation for details.



## SIP configuration (Check Point router)

Use SIP configuration to enable communication between Lumana and external audio devices such as speakers.

This setup is typically required in advanced deployments using network-managed audio systems.


### Before you begin

- Administrative access to the Check Point router  
- Access to Check Point SmartConsole  
- Network topology details  


### Step 1: Enable VoIP

- Log in to Check Point  
- Go to **Access Policy → VoIP**  
- Enable VoIP  

![](../images/configuring-cameras-and-devices/check-point-voip-toggle-on.png)


### Step 2: Configure SIP service provider

Enable **Use SIP Service Provider** and configure the following:

#### Networks

| Name                | Address         | Subnet Mask        |
|---------------------|-----------------|--------------------|
| Oregon_Gateways     | 54.244.51.0     | 255.255.255.252    |
| Frankfrut_Gateways  | 35.156.191.128  | 255.255.255.252    |
| Virginia_Gateways   | 54.172.60.0     | 255.255.255.252    |
| Media_server_1      | 34.203.254.0    | 255.255.255.0      |
| Media_server_2      | 3.235.11.128    | 255.255.255.128    |

#### Domains

- lumana1.sip.twilio.com  
- lumana1.sip.us1.twilio.com  

![](../images/configuring-cameras-and-devices/off-premise-sip-provider-service-list.png)



### Step 3: Configure RTP services

- Disable SIP traffic inspection  
- Add the following services:

| Name          | Protocol | Port |
|---------------|----------|------|
| SIP_TLS_AUTH  | TCP      | 5061 |
| SIP_TCP       | TCP      | 5060 |
| SIP_UDP       | UDP      | 5060 |
| SIP_UDP       | UDP      | 5061 |

- Enable bidirectional traffic  

![](../images/configuring-cameras-and-devices/sip-traffic-inspection-rtp-services.png)


### Step 4: Configure on-premise devices

Add your devices (for example):

| Name             | Type       | Address         |
|------------------|------------|-----------------|
| Uniview_speaker  | Single IP  | 192.168.100.30  |

![](../images/configuring-cameras-and-devices/on-premise-devices-ip-phones.png)


### Step 5: Configure SIP services

Add the following services:

| Name         | Protocol | Ports       |
|--------------|----------|-------------|
| SIP_TLS_AUTH | TCP      | 5061        |
| SIP_TCP      | TCP      | 5060        |
| SIP_UDP      | UDP      | 5060, 5061  |
| Any_TCP      | TCP      | 1–65535     |
| Any_UDP      | UDP      | 1–65535     |

![](../images/configuring-cameras-and-devices/sip-service-ports-table.png)

