# Network Attached Storage (NAS) devices

Connect a network attached storage (NAS) device to Lumana to expand recording storage and keep a backup of recorded video.

Adding a NAS does not replace Lumana Core. The NAS works alongside the core as both an additional storage location for longer retention and a backup target for recorded data. Lumana's standard capabilities remain available.

> **Note:** If you record to NAS for more than 30 days and want to keep smart search functionality, an additional NAS license is required. No license is needed for the first 30 days.

## Prerequisites

* The storage device must support _NFS_ or _S3-compatible object storage_.
* The storage device must be reachable on the network by the Lumana Core unit.

## Add an external storage server

1. Save the IP of your network storage server and the path where Lumana should save videos.

For example:

* **NAS IP:** `192.168.100.200`
* **NAS Path:** `/share/LumanaVideos`

2. In the Lumana console, on the _Devices_ page, find the location where the NAS device is physically connected and click _Edit Location_.
3. In the left menu, click _External Storage_, then click _Add external storage_.
4. Choose your storage type. This can be either _NFS_ or _Object Storage_. See the NFS example below.

* **Storage type:** `NFS`
* **Name:** name your external storage server
* **Path:** NAS IP and a directory path

5. Click _Test_ to check connectivity to the NFS server, then click _Save external storage_.

## Configure cameras to use the external storage server

1. On the live view page of the camera, click _Edit Camera_.
2. In the edit camera menu, click _Storage_, then scroll down to _Additional Storage_.
3. Toggle _Additional storage_ to _On_, then select _External_.
4. After selecting _External_, choose the server where the camera should record. In this example, select the NFS server added earlier, named `NFS-Server-1`.
5. Configure the storage options:

* Choose the retention period for videos on the external storage: `30 / 60 / 90 / 180 / 365` days
* Enable `Storage (SQ)` for saving ordinary footage
* Enable `Alerts (HQ)` for saving high-resolution clips of triggered alerts
* If you wish to restrict the times in which the core uploads videos to the NAS server, use the scheduler at the bottom, _When the upload should occur_

## Storage capacity calculation

* `RAID 5` - minimum 3 disks
* `RAID 6` - minimum 4 disks
* For `5MP` camera SQ (`700Kbps`), `0.3TB` is required for 30 days of storage
* For `8MP` camera SQ (`1000Kbps`), `0.45TB` is required for 30 days of storage

## Examples of NAS servers

* QNAP TS-1673AU-RP-16G,16 Bay NAS
* QNAP TS-464U-RP-8G 4Bay NAS 2.5Gbe

## Examples of HDDs

* MG09ACA18 Toshiba Enterprise 3.5HDD 512E 18TB
* MG09ACA16 Toshiba Enterprise 3.5HDD 512E 16TB
* MG09ACA14 Toshiba Enterprise 3.5HDD 512E 14TB
