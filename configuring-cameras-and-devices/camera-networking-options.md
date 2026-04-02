# Camera networking options

Introduction
In this article we will explore how to access and utilize the Camera VPN function in the Lumana portal. This feature enables seamless remote access to third-party  cameras remotely, boosting operation efficiency and saving time for the things that matter.

 

Step 1:
To access the camera VPN first navigate to the the specific camera you want to access.

![Camera player live view with timeline scrubber](../images/configuring-cameras-and-devices/camera-player-live-view-timeline.png)


Step 2:

click on the VPN icon found in the top right of the camera player page.

 
![Manufacturer VPN login redirect](../images/configuring-cameras-and-devices/manufacturer-vpn-login-redirect.png)


Step 3:

You will then be redirected to the manufacture's login page where you can input your credentials to gain access.

![Hikvision manufacturer login page](../images/configuring-cameras-and-devices/hikvision-manufacturer-login.png)



Step 4:

Once logged in, you have the ability to configure different settings such as camera profiles, streaming configurations, video compression, and other specs related to the camera. Please note, this page will be different for each manufacturer, please reference the manufactures website for more information on their specific capabilities. 

 

This document provides a step-by-step guide to setting up and configuring a SIP connection using a Check Point router. The setup includes necessary screenshots and configuration images for better understanding.

Prerequisites
Before beginning, ensure you have the following:

Administrative access to the Check Point router.
Access to the Check Point SmartConsole.
Network topology details.
 

Step 1: Enable VoIP in Access Policy
Log in to Check Point.
Go to the Access Policy tab.
Navigate to the VoIP tab.
Enable VoIP.

![](../images/configuring-cameras-and-devices/check-point-voip-toggle-on.png)


Step 2: Configure SIP Service Provider
Enable: Use SIP Service Provider
Name: SIP-Provider
Add the following addresses:
Type	Name	Address	Subnet Mask
Network	Oregon_Gateways	54.244.51.0	255.255.255.252
Network	Frankfrut_Gateways	35.156.191.128	255.255.255.252
Network	Virginia_Gateways	54.172.60.0	255.255.255.252
Network	Media_server_1	34.203.254.0	255.255.255.0
Network	Media_server_2	3.235.11.128	255.255.255.128
Add the following domain names:
Type	Domain Name
Domain name	lumana1.sip.twilio.com
Domain name	lumana1.sip.us1.twilio.com


![](../images/configuring-cameras-and-devices/off-premise-sip-provider-service-list.png)

Step 3: Disable SIP Traffic Inspection and Configure RTP Services
Disable SIP traffic inspection.
Add the following RTP services:
Name	Protocol	Port
SIP_TLS_AUTH	TCP	5061
SIP_TCP	TCP	5060
SIP_UDP	UDP	5060
SIP_UDP	UDP	5061
Enable bidirectional traffic.

![](../images/configuring-cameras-and-devices/sip-traffic-inspection-rtp-services.png)
 
Step 4: Configure On-Premise Devices
Use on-premise phones without a SIP server (PBX).
Add all relevant resources, for example:
Name	Type	Address
Uniview_speaker	Single IP	192.168.100.30

![](../images/configuring-cameras-and-devices/on-premise-devices-ip-phones.png)

Step 5: Configure SIP Services
Add the following services:

Name	Type	Protocol	Destination Ports
SIP_TLS_AUTH	SIP_TLS_AUTH	TCP	5061
SIP_TCP	SIP_TCP	TCP	5060
sip_any-tcp	sip_any-tcp	TCP	5060
SIP_UDP	SIP_UDP	UDP	5060
Any_TCP	Any_TCP	TCP	1-65535
SIP_UDP	SIP_UDP	UDP	5061
Any_UDP	Any_UDP	UDP	1-65535

![](../images/configuring-cameras-and-devices/sip-service-ports-table.png)

Speaker configuration - Examples
Note: SIP credentials (address, username, password) are supplied by your CSM.

Example 1: Uniview Speaker Configuration
Log in to the Uniview speaker interface.
Go to the SIP Account section.
Add the following details:
Username
ID
Password
Display Name - used ad identifier to use on alerts
Server Host
Port
Expire Time > 600
Set Auto Answer to Immediately
Save the configuration.
Verify that the speaker status changes to Registered.

![](../images/configuring-cameras-and-devices/sip-account-setup-example.png)

Example 2: TOA Speaker Configuration
Log in to the TOA speaker interface.
Go to the SIP section.
Update the following details:
SIP Server Address
SIP Server Port
Registration Expiry > 3600
User ID
Display Name - used ad identifier to use on alerts
Password
Audio Codec: Enable all codecs
Save the configuration.

 

![](../images/configuring-cameras-and-devices/toa-speaker-sip-account-registered.png)

