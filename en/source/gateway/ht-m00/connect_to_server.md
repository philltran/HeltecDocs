# Connect HT-M00 to LoRa Server
[简体中文](https://heltec-automation.readthedocs.io/zh_CN/latest/gateway/ht-m00/connect_to_server.html)

## Summary

This article aims to describe how to connect [HT-M00 Gateway](https://heltec.org/project/ht-m00/) to a LoRa server, such as [TTN](https://www.thethingsnetwork.org/), [ChirpStack](https://www.chirpstack.io/), [Heltec Cloud Server](http://cloud.heltec.org/), which facilitates secondary development and rapid deployment of LoRa devices.

Before all operation, make sure the HT-M00 is runing well . If not, please refer to this [HT-M00 Quick Start](https://heltec-automation-docs.readthedocs.io/en/latest/gateway/ht-m00/quick_start.html) document.

&nbsp;

## Connect to TTN

### Register a LoRa gateway in TTN

Create and active an account in TTN. Select ```Gateway``` in the [console](https://console.thethingsnetwork.org/) page.

![](img/connect_to_server/02.png)

Fill in the HT-M00 information as shown below and complete the addition.

![](img/connect_to_server/03.png)

- **Gateway EUI** -- The unique ID of HT-M00 gateway, view from the display screen of the HT-M00 or view through the serial port (the gateway ID will be printed through the serial port when the HT-M00 starts);
- **I'm using the legacy packet forwarder** -- Must select this;
- **Frequency Plan** -- Must matach the LoRa band configuration in HT-M00.
- **Router** -- Must use the default router allocated by TTN system.

``` Tip:: That four points are the key to success connection with TTN.

```



### Connect to TTN

Users  need config the server address, port and channel in the  HT-M00 gateway. The server address, port and channel are configured in the "HT-M00 Config" interface, Please refer to [HT-M00 Quick Start](https://heltec-automation-docs.readthedocs.io/en/latest/gateway/ht-m00/qucik_start.html) document.

![](img/connect_to_server/01.png)

The TTN's router addresses for different region:

[https://www.thethingsnetwork.org/docs/gateways/packet-forwarder/semtech-udp.html#router-addresses](https://www.thethingsnetwork.org/docs/gateways/packet-forwarder/semtech-udp.html#router-addresses)

![](img/connect_to_server/04.png)

View gateway status, it is runing:

![](img/connect_to_server/05.png)

&nbsp;

## Connect to ChirpStack server

[ChirpStack](https://www.chirpstack.io/) is the most popular LoRa server open source project, widely used in many fields, and also the best choise for a private LoRa server.

- ChirpStack Installation guide: [https://www.chirpstack.io/overview/](https://www.chirpstack.io/overview/)
- ChirpStack support forum: [https://forum.chirpstack.io/](https://forum.chirpstack.io/)

### ChirpStack Gateway Bridge

**One thing need attention!** the ChirpStack need a special service named `Gateway Bridge`, which converts LoRa® Packet Forwarder protocols into a ChirpStack Network Server common data-format(JSON and Protobuf).

the `Gateway Bridge` service can running on the Raspberry Pi or the ChirpStack server.

Install ChirpStack Gateway Bridge: [https://www.chirpstack.io/gateway-bridge/install/debian/](https://www.chirpstack.io/gateway-bridge/install/debian/)

### Register LoRa Gateway in ChirpStack

Fill in the HT-M00 information as shown below and complete the addition.

![](img/connect_to_server/06.png)

- **Gateway ID** -- The unique ID of HT-M00 gateway, view from the display screen of the HT-M00 or view through the serial port (the gateway ID will be printed through the serial port when the HT-M00 starts).

### Connect to ChirpStack server

Users  need config the server address, port and channel in the  HT-M00 gateway. The server address, port and channel are configured in the "HT-M00 Config" interface, Please refer to [HT-M00 Quick Start](https://heltec-automation-docs.readthedocs.io/en/latest/gateway/ht-m00/qucik_start.html) document.

![](img/connect_to_server/01.png)

View gateway status, it is runing:

![](img/connect_to_server/07.png)

&nbsp;

## Connect to HelTec server

### Register LoRa Gateway in HelTec Cloud Server

Fill in the HT-M00 information as shown below and complete the addition.

![](img/connect_to_server/09.png)

- **Gateway ID** -- The unique ID of HT-M00 gateway, view from the display screen of the HT-M00 or view through the serial port (the gateway ID will be printed through the serial port when the HT-M00 starts).

### Connect to HelTec server

Users  need config the server address, port and channel in the  HT-M00 gateway. The server address, port and channel are configured in the "HT-M00 Config" interface, Please refer to [HT-M00 Quick Start](https://heltec-automation-docs.readthedocs.io/en/latest/gateway/ht-m00/qucik_start.html) document.

![](img/connect_to_server/01.png)

The server addresses corresponding to different regions are as follows:

`CN470` --  `cn01.cloud.heltec.cn`

`EU868` --  `eu01.cloud.heltec.org`

`US915` --  `us01.cloud.heltec.org`

`AU915` --  `au01.cloud.heltec.org`

`AS923` --  `as01.cloud.heltec.org`

View gateway status, it is runing:

![](img/connect_to_server/11.png)