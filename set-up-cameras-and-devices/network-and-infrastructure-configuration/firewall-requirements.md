# Firewall requirements

The Lumana Platform necessitates an outbound internet connection to communicate with Lumana Cloud. Our system is designed to prioritize security and safeguard against cyberattacks by not requiring inbound connections. If your network firewall monitors outbound traffic, you need to add the following sites to the approved outbound port to ensure the proper functioning of the system.

## 1. Infrastructure

Lumana provides two methods to configure your firewall:

Lumana URLs:

A list of domains with their corresponding access requirements.

Lumana IPs:

An API endpoint that returns all Lumana infrastructure IPs.

### 1.1 Lumana infrastructure URL's:

Allow outbound TCP 443 to the following:

* \*.lumix.ai - 443 TCP outbound
* \*.lumana.ai - 443 TCP outbound
* _.us-west_.compute.amazonaws.com - 443 TCP outbound
* _eu-central_.compute.amazonaws.com - 443 TCP outbound
* _.us-east_.compute.amazonaws.com - 443 TCP outbound
* \*cloudfront.net - 443 TCP outbound
* auth.docker.io - 443 TCP outbound
* \*.docker.io - 443 TCP outbound
* production.cloudflare.docker.com - 443 TCP outbound
* storage.googleapis.com - 443 TCP outbound
* www.googleapis.com - 443 TCP outbound
* \*bc.googleusercontent.com - 443, TCP outbound
* \*nac.nodebalancer.linode.com - 443 TCP outbound
* prometheus-prod-56-prod-us-east-2.grafana.net - 443 TCP outbound
* prometheus-us-central1.grafana.net - 443 TCP outbound
* www.speedtest.net - 443 TCP outbound
* api.speedtest.net - 443 TCP outbound
* c.speedtest.net - 443 TCP outbound

Media server signalling:

US-central:

* stream-us-central1.lumana.ai - 443 TCP outbound - Signal connection over secure WebSocket
* turn-us-central1.lumana.ai - 443 TCP outbound - TURN/TLS. Used when UDP connection isn't viable. Need to allow TLS traffic (not only HTTPS traffic)

US-east:

* stream-us-east1.lumana.ai - 443 TCP outbound - Signal connection over secure WebSocket
* turn-us-east1.lumana.ai - 443 TCP outbound - TURN/TLS. Used when UDP connection isn't viable. Need to allow TLS traffic (not only HTTPS traffic)

US-west:

* stream-us-west1.lumana.ai - 443 TCP outbound - Signal connection over secure WebSocket
* turn-us-west1.lumana.ai - 443 TCP outbound - TURN/TLS. Used when UDP connection isn't viable. Need to allow TLS traffic (not only HTTPS traffic)

Israel:

* stream-me-west1.lumana.ai - 443 TCP outbound - Signal connection over secure WebSocket
* turn-me-west1.lumana.ai - 443 TCP outbound - TURN/TLS. Used when UDP connection isn't viable. Need to allow TLS traffic

### 1.2 Lumana infrastructure IP's:

Instead of managing URL-based firewall rules, you may whitelist IPs directly.

### Step 1: Generating API Key

Navigate to:

Organisation Settings -> API Keys -> Generate Key

### Step 2: Get List of IP's

Call:

https://access.lumana.ai/v1/network/get-ip-addresses

API reference:

https://apidocs.lumana.ai/reference/networkcontroller\_getipaddresses-1

### Step 3: Put the IP's on Firewall allowed list

Add the returned IPs to your firewall’s allowlist.

Important:

Lumana infrastructure IPs may change periodically. Annual review and update is recommended.

## 2. Media servers

Lumana Live View uses WebRTC + WebSocket.

All traffic is encrypted with TLS and DTLS.

If UDP is blocked, TURN/TLS over TCP 443 is used.

### Ports

* UDP 3478 – TURN
* UDP 50000–60000 – WebRTC media
* TCP/UDP 7881 – ICE

For best audio/video performance:

Allow the UDP ports above

Enable UDP hole-punching or disable symmetric NAT

### 2.1 Regional Media Server IPs

US-Central

Load balancer: 34.27.216.77

Media server hostnames: stream-us-central1-\*.lumana.ai

Media server IPs:

* 34.27.11.6
* 35.225.131.69
* 34.57.39.16
* 35.202.149.180
* 34.46.106.42
* 34.41.133.0
* 34.29.153.34
* 35.202.93.234
* 34.45.55.192
* 34.60.41.218

US-East

Load balancer: 35.196.117.219

Media server hostnames: stream-us-east1-\*.lumana.ai

Media server IPs:

* 34.75.254.27
* 104.196.29.253
* 34.73.113.91
* 35.243.236.207
* 34.139.235.43
* 34.148.161.83
* 34.75.232.205
* 35.237.127.235
* 35.196.67.179
* 34.23.19.135

US-West

Load balancer: 35.199.186.174

Media server hostnames: stream-us-west1-\*.lumana.ai

Media server IPs:

* 35.247.26.49
* 35.203.141.127
* 34.19.8.114
* 34.169.52.181
* 35.227.169.160
* 34.168.155.221
* 34.169.112.111
* 34.83.57.138
* 34.19.100.187
* 34.105.37.179

Israel

Load balancer: 34.165.216.47

Media server hostnames: stream-me-west1-\*.lumana.ai

Media server IPs:

* 34.165.44.152
* 34.165.88.175
* 34.165.75.89
* 34.165.47.176
* 34.165.22.239
* 34.165.201.74
* 34.165.187.232
* 34.165.25.182
* 34.165.19.119
* 34.165.34.86

## 3. NTP (Time Synchronization):

Need minimum two of the below:

* time.cloudflare.com - 123 UDP outbound
* ntp.ubuntu.com - 123 UDP outbound
* pool.ntp.org - 123 UDP outbound
* time.google.com - 123 UDP out
* 0.pool.ntp.org - 123 UDP outbound
* 1.pool.ntp.org - 123 UDP outbound
* 0.fr.pool.ntp.org - 123 UDP outbound

## 4. OS Updates

* archive.ubuntu.com - ports: 80, 443 TCP outbound
* security.ubuntu.com - ports: 80, 443 TCP outbound
* \*canonical.com - ports: 80, 443 TCP outbound
* ports.ubuntu.com, 443 TCP outbound
* repo.download.nvidia.com, 443 TCP outbound
* nvidia.github.io, 443 TCP outbound

## Lumana Web application firewall requirements

The Lumana Web application necessitates an outbound internet connection to communicate with Lumana Cloud. Our system is designed to prioritize security and safeguard against cyberattacks by not requiring inbound connections. If your network firewall monitors outbound traffic, you may need to add the following sites to the approved outbound port to ensure the proper functioning of the application. Should you require any assistance, please feel free to contact our support team for additional guidance.

### Lumana infrastructure:

* \*.lumix.ai - 443 TCP outbound
* \*.lumana.ai - 443 TCP outbound

### Corporate firewalls:

Lumana live view uses WebSocket and WebRTC to transmit data and media. All transmissions are encrypted with TLS and DTLS. If needed Lumana live view uses TURN servers.

### Stun servers:

* global.stun.twilio.com - 3478 UDP outbound
* stun1.l.google.com - 19302 UDP outbound
* stun.l.google.com - 19302 UDP outbound

### US-Central Live view servers:

* stream-us-central1.lumana.ai - 443 TCP outbound - Signal connection over secure WebSocket
* turn-us-central1.lumana.ai - 443 TCP outbound - TURN/TLS. Used when UDP connection isn't viable. Need to allow TLS traffic (not only HTTPS traffic)
* 34.27.216.77 - 443 TCP - livekit-external-lb

Media servers hosts

* 3478 UDP outbound for TURN
* 50000-60000 UDP outbound for WebRTC media connection
* 7881 TCP and UDP outbound for ICE

Media servers (URL): stream-us-central1-\*.lumana.ai

Media servers (IP's):

* 34.27.11.6
* 35.225.131.69
* 34.57.39.16
* 35.202.149.180
* 34.46.106.42
* 34.41.133.0
* 34.29.153.34
* 35.202.93.234
* 34.45.55.192
* 34.60.41.218

### US-East Live view servers:

* stream-us-east1.lumana.ai - 443 TCP outbound - Signal connection over secure WebSocket
* turn-us-east1.lumana.ai - 443 TCP outbound - TURN/TLS. Used when UDP connection isn't viable. Need to allow TLS traffic (not only HTTPS traffic)
* 35.196.117.219 - 443 TCP - livekit-external-lb

Media servers hosts

* 3478 UDP outbound for TURN
* 50000-60000 UDP outbound for WebRTC media connection
* 7881 TCP and UDP outbound for ICE

Media servers (URL): stream-us-east1-\*.lumana.ai

Media servers (IP's):

* 34.75.254.27
* 104.196.29.253
* 34.73.113.91
* 35.243.236.207
* 34.139.235.43
* 34.148.161.83
* 34.75.232.205
* 35.237.127.235
* 35.196.67.179
* 34.23.19.135

### US-West Live view servers:

* stream-us-west1.lumana.ai - 443 TCP outbound - Signal connection over secure WebSocket
* turn-us-west1.lumana.ai - 443 TCP outbound - TURN/TLS. Used when UDP connection isn't viable. Need to allow TLS traffic (not only HTTPS traffic)
* 35.199.186.174 TCP - livekit-external-lb

Media servers hosts

* 3478 UDP outbound for TURN
* 50000-60000 UDP outbound for WebRTC media connection
* 7881 TCP and UDP outbound for ICE

Media servers (URL): stream-us-west1-\*.lumana.ai

Media servers (IP's):

* 35.247.26.49
* 35.203.141.127
* 34.19.8.114
* 34.169.52.181
* 35.227.169.160
* 34.168.155.221
* 34.169.112.111
* 34.83.57.138
* 34.19.100.187
* 34.105.37.179

### Israel Live view servers:

* stream-me-west1.lumana.ai - 443 TCP outbound - Signal connection over secure WebSocket
* turn-me-west1.lumana.ai - 443 TCP outbound - TURN/TLS. Used when UDP connection isn't viable. Need to allow TLS traffic
* 34.165.216.47 TCP - livekit-external-lb

Media servers hosts

* 3478 UDP outbound for TURN
* 50000-60000 UDP outbound for WebRTC media connection
* 7881 TCP and UDP outbound for ICE

Media servers (URL): stream-me-west1-\*.lumana.ai

Media servers (IP's):

* 34.165.44.152
* 34.165.88.175
* 34.165.75.89
* 34.165.47.176
* 34.165.22.239
* 34.165.201.74
* 34.165.187.232
* 34.165.25.182
* 34.165.19.119
* 34.165.34.86

In order to obtain the best audio and video quality, we recommend allowing access to the UDP ports listed above. Additionally, please ensure UDP hole-punching is enabled (or disable symmetric NAT). This helps machines behind the firewall to establish a direct connection to Lumana Cloud media server.
