---

## description: Wio LoRa Module
title: Wio LoRa Module
keywords:
  - LoRa Module
image: [https://files.seeedstudio.com/media/slidebanner/wio_module_banner2_familyphoto.png](https://files.seeedstudio.com/media/slidebanner/wio_module_banner2_familyphoto.png)
slug: /wio_module_introduction
sidebar_position: 1
last_update:
  date: 10/21/2026
  author: Seeed Studio
createdAt: '2026-10-21'
updatedAt: '2026-10-21'
url: ''

A **LoRa module** is a compact wireless hardware component built around a LoRa (Long Range) radio transceiver. Some LoRa modules also integrate a microcontroller (MCU), while transceiver-only modules require an external MCU. They enable long-range, low-power wireless data exchange in Internet of Things (IoT) systems.

**Wio LoRa Module** is a family of wireless modules and evaluation hardware introduced by **Seeed Studio, an official Semtech partner**. The lineup covers Semtech's second-generation SX1262 radio platform (Wio-SX1262, including the 1 W version), third-generation LR1121 multi-band platform (Wio-LR1121), and fourth-generation LoRa Plus platform (Wio-LR2021 and LR2012 evaluation kits). It also includes Wio-E5 (STM32WLE5JC with MCU and LoRa radio), Wio-S3 (ESP32-S3 with SX1262), Wio-WM1110 (LR1110 with nRF52840 for tracking), and Wio-WM1302 (SX1302-based gateway concentrator). The series supports RF and firmware evaluation, wireless sensor design, asset tracking, Meshtastic nodes, smart metering, and multi-channel LoRaWAN gateway development, from prototypes to production-oriented hardware.

<p style={{textAlign: 'center'}}><img src="https://files.seeedstudio.com/media/slidebanner/wio_module_banner2_familyphoto.png" alt="pir" width={900} height="auto" /></p>




## Features

- **Long Range:** Sub-GHz LoRa links can reach several kilometers and, under favorable rural line-of-sight conditions, approximately 10–15 km. Actual range depends on frequency, antenna, transmit power, receiver sensitivity, terrain, and local regulations.
- **Low Power:** Low sleep and receive current supports battery-powered sensor and tracker designs with multi-year operating targets, depending on duty cycle, power supply, and device configuration.
- **Modulation:** LoRa uses chirp spread spectrum (CSS) modulation for robust, high-sensitivity wireless links. Selected products additionally support (G)FSK or FLRC, depending on the transceiver.
- **Communication Modes:** Supports point-to-point (P2P) communication and, with compatible firmware and network infrastructure, LoRaWAN star-of-stars networks. Mesh networking, such as Meshtastic, is implemented by the device firmware rather than by LoRa modulation alone.
- **Hardware Options:** Includes standalone SPI-controlled RF transceivers, modules combining an MCU and a radio, positioning-oriented modules, and multi-channel LoRaWAN gateway concentrators.


## How it Works

LoRa is a long-range, low-power wireless communication technology that provides the physical radio link between devices. Different networking protocols define how LoRa devices discover one another, route messages, manage connections, and deliver data to users or cloud applications.

### Meshtastic: Decentralized Mesh Networking

**Network Topology:** Decentralized, multi-hop mesh network.

Meshtastic is an open-source communication system that enables LoRa devices to exchange encrypted text messages, GPS locations, and telemetry without cellular coverage or internet infrastructure. Each compatible node can communicate directly with nearby nodes and relay messages to extend network coverage.

Learn more from the [Meshtastic documentation](https://meshtastic.org/docs/overview/mesh-algo/).


### MeshCore: Repeater-Based Mesh Networking

**Network Topology:** Multi-hop mesh network with dedicated repeater nodes.

MeshCore is an open-source LoRa communication system that separates device roles into companions, repeaters, and optional room servers. Companion devices provide messaging interfaces, while repeaters extend communication coverage by forwarding packets between distant devices.

Learn more from the [MeshCore documentation](https://docs.meshcore.io/).


### LoRaWAN: Gateway-Based IoT Networking

**Network Topology:** Star-of-stars topology connecting end devices, gateways, network servers, and application servers.

LoRaWAN is a standardized Low Power Wide Area Network (LPWAN) protocol designed for connecting large numbers of battery-powered IoT devices over long distances. End devices communicate wirelessly with LoRaWAN gateways, which forward received packets to a centralized network server through an IP connection.

**How LoRaWAN Data Transmission Works:**

1. **Data Collection:** Sensors or controllers collect measurements such as temperature, pressure, water consumption, energy usage, or equipment status.
2. **LoRa Uplink:** The end device encodes its measurements into a data payload and transmits an encrypted LoRaWAN packet over a regional radio frequency band, such as EU868 or US915.
3. **Gateway Reception:** One or more nearby LoRaWAN gateways receive the same uplink packet. Multi-channel gateways can receive transmissions from numerous devices using different channels and spreading factors.
4. **Network Server Processing:** Gateways forward received packets through Ethernet, Wi-Fi, or cellular backhaul to a LoRaWAN Network Server, such as The Things Stack or ChirpStack. The server validates network messages, removes duplicate receptions, manages device sessions, and selects gateways for downlink transmission.
5. **Application Server Delivery:** The Application Server processes application payloads and makes the decoded sensor data available to dashboards, databases, cloud platforms, or industrial monitoring systems through APIs, MQTT, or other integrations.
6. **Downlink Communication:** When required, the application can send commands or configuration updates back to end devices through the network server and a selected gateway.


**Typical Applications:** Smart water and electricity metering, industrial equipment monitoring, smart agriculture, environmental sensing, building automation, and smart city infrastructure.

Learn more from the [LoRa Alliance](https://lora-alliance.org/about-lorawan/).


### Amazon Sidewalk: Community-Based IoT Connectivity

**Network Topology:** Shared gateway-based network connecting IoT endpoints to Amazon Sidewalk gateways and cloud services.

Amazon Sidewalk is a low-bandwidth wireless network designed to extend IoT connectivity beyond individual homes and buildings. Compatible Amazon Echo and Ring devices can function as Sidewalk gateways, providing shared network access for authorized endpoint devices.


Learn more from the [AWS IoT Core for Amazon Sidewalk documentation](https://docs.aws.amazon.com/iot-wireless/latest/developerguide/iot-sidewalk.html).


## Supported Hardware

### LoRa Modules

<table align="center">
<tbody><tr>
<th>Wio-SX1262 with IPEX</th>
<th>Wio-SX1262 without IPEX</th>
<th>Wio-SX1262-LF</th>
</tr>
<tr>
<td><div align="center"><img src="https://media-cdn.seeedstudio.com/media/catalog/product/cache/48035b5512857d0ab907b31a092da78f/1/-/1-114993390-wio-sx1262-wireless-module.jpg" style={{width:300, height:'auto'}}/></div></td>
<td><div align="center"><img src="https://media-cdn.seeedstudio.com/media/catalog/product/cache/48035b5512857d0ab907b31a092da78f/1/-/1-113991436_wio-sx1262_wireless_module_without_ipex_tape_reel_.jpg" style={{width:350, height:'auto'}}/></div></td>
<td><div align="center"><img src="https://media-cdn.seeedstudio.com/media/catalog/product/cache/48035b5512857d0ab907b31a092da78f/1/-/1-100097817-wio--sx-1262-lf.jpg" style={{width:350, height:'auto'}}/></div></td>
</tr>
<tr>
<td align="center"><div class="get_one_now_container" style={{textAlign: 'center'}}>
<a class="get_one_now_item" href="https://www.seeedstudio.com/Wio-SX1262-Wireless-Module-p-5981.html" target="_blank">
<strong><span><font color={'FFFFFF'} size={"4"}> Check More🖱️</font></span></strong>
</a>
</div></td>
<td align="center"><div class="get_one_now_container" style={{textAlign: 'center'}}>
<a class="get_one_now_item" href="https://www.seeedstudio.com/Wio-SX1262-Wireless-Module-without-IPEX-Tape-Reel-p-6417.html" target="_blank">
<strong><span><font color={'FFFFFF'} size={"4"}> Check More🖱️</font></span></strong>
</a>
</div></td>
<td align="center"><div class="get_one_now_container" style={{textAlign: 'center'}}>
<a class="get_one_now_item" href="https://www.seeedstudio.com/Wio-SX1262-LF-Wireless-Module-p-6659.html" target="_blank">
<strong><span><font color={'FFFFFF'} size={"4"}> Check More🖱️</font></span></strong>
</a>
</div></td>
</tr>
</tbody></table>

<table align="center">
<tbody><tr>
<th>Wio-SX1262-1W</th>
<th>Wio-S3 with IPEX</th>
<th>Wio-E5</th>
</tr>
<tr>
<td><div align="center"><img src="https://media-cdn.seeedstudio.com/media/catalog/product/cache/48035b5512857d0ab907b31a092da78f/1/0/100013283-gallery_img_1.jpg" style={{width:300, height:'auto'}}/></div></td>
<td><div align="center"><img src="https://media-cdn.seeedstudio.com/media/catalog/product/cache/48035b5512857d0ab907b31a092da78f/2/-/2-100020327-wio-s3-wireless-module-with-ipex.jpg" style={{width:350, height:'auto'}}/></div></td>
<td><div align="center"><img src="https://media-cdn.seeedstudio.com/media/catalog/product/cache/48035b5512857d0ab907b31a092da78f/1/-/1-317990687-wio-e5-wireless-module-_bulk_-1111font.jpg" style={{width:350, height:'auto'}}/></div></td>
</tr>
<tr>
<td align="center"><div class="get_one_now_container" style={{textAlign: 'center'}}>
<a class="get_one_now_item" href="https://www.seeedstudio.com/Wio-SX1262-1W-p-7007.html" target="_blank">
<strong><span><font color={'FFFFFF'} size={"4"}> Check More🖱️</font></span></strong>
</a>
</div></td>
<td align="center"><div class="get_one_now_container" style={{textAlign: 'center'}}>
<a class="get_one_now_item" href="https://www.seeedstudio.com/Wio-S3-Wireless-Module-p-6832.html" target="_blank">
<strong><span><font color={'FFFFFF'} size={"4"}> Check More🖱️</font></span></strong>
</a>
</div></td>
<td align="center"><div class="get_one_now_container" style={{textAlign: 'center'}}>
<a class="get_one_now_item" href="https://www.seeedstudio.com/LoRa-E5-Wireless-Module-p-4745.html" target="_blank">
<strong><span><font color={'FFFFFF'} size={"4"}> Check More🖱️</font></span></strong>
</a>
</div></td>
</tr>
</tbody></table>

<table align="center">
<tbody><tr>
<th>Wio-LR1121</th>
<th>Wio-LR2021</th>
<th>Wio-WM1110</th>
</tr>
<tr>
<td><div align="center"><img src="https://media-cdn.seeedstudio.com/media/catalog/product/cache/48035b5512857d0ab907b31a092da78f/1/-/1-113991415-wio-lr1121_1.jpg" style={{width:300, height:'auto'}}/></div></td>
<td><div align="center"><img src="https://media-cdn.seeedstudio.com/media/catalog/product/cache/48035b5512857d0ab907b31a092da78f/1/-/1-100058045-seeed-studio-wio-lr2021-wireless-module-masked.jpg" style={{width:350, height:'auto'}}/></div></td>
<td><div align="center"><img src="https://media-cdn.seeedstudio.com/media/catalog/product/cache/48035b5512857d0ab907b31a092da78f/1/-/1-327133202-wm1110-a-45font3.1.jpg" style={{width:350, height:'auto'}}/></div></td>
</tr>
<tr>
<td align="center"><div class="get_one_now_container" style={{textAlign: 'center'}}>
<a class="get_one_now_item" href="https://www.seeedstudio.com/Wio-LR1121-with-IPEX-antenna-connector-p-6479.html" target="_blank">
<strong><span><font color={'FFFFFF'} size={"4"}> Check More🖱️</font></span></strong>
</a>
</div></td>
<td align="center"><div class="get_one_now_container" style={{textAlign: 'center'}}>
<a class="get_one_now_item" href="https://www.seeedstudio.com/Seeed-Studio-Wio-LR2021-Wireless-module-868-915MHz-Tape-reel-p-6831.html" target="_blank">
<strong><span><font color={'FFFFFF'} size={"4"}> Check More🖱️</font></span></strong>
</a>
</div></td>
<td align="center"><div class="get_one_now_container" style={{textAlign: 'center'}}>
<a class="get_one_now_item" href="https://www.seeedstudio.com/Wio-WM1110-Module-LR1110-and-nRF52840-p-5676.html" target="_blank">
<strong><span><font color={'FFFFFF'} size={"4"}> Check More🖱️</font></span></strong>
</a>
</div></td>
</tr>
</tbody></table>

<table align="center">
<tbody><tr>
<th>Wio-WM1302 (SPI, EU868)</th>
</tr>
<tr>
<td><div align="center"><img src="https://media-cdn.seeedstudio.com/media/catalog/product/cache/48035b5512857d0ab907b31a092da78f/1/-/1-114992549.jpg" style={{width:300, height:'auto'}}/></div></td>
</tr>
<tr>
<td align="center"><div class="get_one_now_container" style={{textAlign: 'center'}}>
<a class="get_one_now_item" href="https://www.seeedstudio.com/WM1302-LoRaWAN-Gateway-Module-SPI-EU868-p-4889.html" target="_blank">
<strong><span><font color={'FFFFFF'} size={"4"}> Check More🖱️</font></span></strong>
</a>
</div></td>
</tr>
</tbody></table>

### Development Boards and Evaluation Kits

<table align="center">
<tbody><tr>
<th>Semtech LR2021 Evaluation Kit-EU868</th>
<th>Semtech LR2021 Evaluation Kit-US915</th>
<th>Semtech LR2021 Evaluation Kit-CN490</th>
</tr>
<tr>
<td><div align="center"><img src="https://media-cdn.seeedstudio.com/media/catalog/product/cache/48035b5512857d0ab907b31a092da78f/1/-/1-100039980-lr2021-lora-plus-evaluation-kit-868mhz-eu.jpg" style={{width:300, height:'auto'}}/></div></td>
<td><div align="center"><img src="https://media-cdn.seeedstudio.com/media/catalog/product/cache/48035b5512857d0ab907b31a092da78f/1/-/1-100035909-lr2021-lora-plus-evaluation-kit-915mhz-us.jpg" style={{width:350, height:'auto'}}/></div></td>
<td><div align="center"><img src="https://media-cdn.seeedstudio.com/media/catalog/product/cache/48035b5512857d0ab907b31a092da78f/1/-/1-100025096-lr2021-lora-plus-evaluation-kit-490mhz-cn_1.jpg" style={{width:350, height:'auto'}}/></div></td>
</tr>
<tr>
<td align="center"><div class="get_one_now_container" style={{textAlign: 'center'}}>
<a class="get_one_now_item" href="https://www.seeedstudio.com/LR2021-LoRa-Plus-Evaluation-kit-868Mhz-EU-V2-0-p-6697.html" target="_blank">
<strong><span><font color={'FFFFFF'} size={"4"}> Check More🖱️</font></span></strong>
</a>
</div></td>
<td align="center"><div class="get_one_now_container" style={{textAlign: 'center'}}>
<a class="get_one_now_item" href="https://www.seeedstudio.com/LR2021-LoRa-Plus-Evaluation-kit-915Mhz-US-V2-0-p-6698.html" target="_blank">
<strong><span><font color={'FFFFFF'} size={"4"}> Check More🖱️</font></span></strong>
</a>
</div></td>
<td align="center"><div class="get_one_now_container" style={{textAlign: 'center'}}>
<a class="get_one_now_item" href="https://www.seeedstudio.com/LR2021-LoRa-Plus-Evaluation-kit-490Mhz-CN-p-6699.html" target="_blank">
<strong><span><font color={'FFFFFF'} size={"4"}> Check More🖱️</font></span></strong>
</a>
</div></td>
</tr>
</tbody></table>

<table align="center">
<tbody><tr>
<th>Semtech LR2012 Evaluation Kit-EU868</th>
<th>Semtech LR2012 Evaluation Kit-US915</th>
<th>Wio-WM1110 Dev Kit</th>
</tr>
<tr>
<td><div align="center"><img src="https://media-cdn.seeedstudio.com/media/catalog/product/cache/bb49d3ec4ee05b6f018e93f896b8a25d/1/0/100092071-gallery_img_1.png" style={{width:300, height:'auto'}}/></div></td>
<td><div align="center"><img src="https://media-cdn.seeedstudio.com/media/catalog/product/cache/bb49d3ec4ee05b6f018e93f896b8a25d/1/0/100015571-gallery_img_1.png" style={{width:350, height:'auto'}}/></div></td>
<td><div align="center"><img src="https://media-cdn.seeedstudio.com/media/catalog/product/cache/48035b5512857d0ab907b31a092da78f/1/-/1-114993082-wio-wm1110-dev-kit-45font.jpg" style={{width:350, height:'auto'}}/></div></td>
</tr>
<tr>
<td align="center"><div class="get_one_now_container" style={{textAlign: 'center'}}>
<a class="get_one_now_item" href="https://www.seeedstudio.com/semtech-lr2012-lora-plus-evaluation-kit-eu868-p-7004.html" target="_blank">
<strong><span><font color={'FFFFFF'} size={"4"}> Check More🖱️</font></span></strong>
</a>
</div></td>
<td align="center"><div class="get_one_now_container" style={{textAlign: 'center'}}>
<a class="get_one_now_item" href="https://www.seeedstudio.com/semtech-lr2012-lora-plus-evaluation-kit-us915-p-7005.html" target="_blank">
<strong><span><font color={'FFFFFF'} size={"4"}> Check More🖱️</font></span></strong>
</a>
</div></td>
<td align="center"><div class="get_one_now_container" style={{textAlign: 'center'}}>
<a class="get_one_now_item" href="https://www.seeedstudio.com/Wio-WM1110-Dev-Kit-p-5677.html" target="_blank">
<strong><span><font color={'FFFFFF'} size={"4"}> Check More🖱️</font></span></strong>
</a>
</div></td>
</tr>
</tbody></table>

<table align="center">
<tbody><tr>
<th>Wio-E5 Dev Kit</th>
<th>XIAO ESP32S3 & Wio-SX1262 Kit</th>
</tr>
<tr>
<td><div align="center"><img src="https://media-cdn.seeedstudio.com/media/catalog/product/cache/48035b5512857d0ab907b31a092da78f/s/k/sku113990934_0.jpg" style={{width:300, height:'auto'}}/></div></td>
<td><div align="center"><img src="https://media-cdn.seeedstudio.com/media/catalog/product/cache/48035b5512857d0ab907b31a092da78f/2/-/2-102010611-wio-sx1262-with-xiao-esp32s3.jpg" style={{width:350, height:'auto'}}/></div></td>
</tr>
<tr>
<td align="center"><div class="get_one_now_container" style={{textAlign: 'center'}}>
<a class="get_one_now_item" href="https://www.seeedstudio.com/LoRa-E5-Dev-Kit-p-4868.html" target="_blank">
<strong><span><font color={'FFFFFF'} size={"4"}> Check More🖱️</font></span></strong>
</a>
</div></td>
<td align="center"><div class="get_one_now_container" style={{textAlign: 'center'}}>
<a class="get_one_now_item" href="https://www.seeedstudio.com/Wio-SX1262-with-XIAO-ESP32S3-p-5982.html" target="_blank">
<strong><span><font color={'FFFFFF'} size={"4"}> Check More🖱️</font></span></strong>
</a>
</div></td>
</tr>
</tbody></table>

## Application

### Environmental Monitoring and Smart City Sensors

- **Air quality:** Wio-E5-based sensor nodes transmit indoor VOC / air-quality measurements and outdoor air-quality monitoring data through LoRaWAN for dashboards and remote monitoring.
- **Snow depth:** A low-power Wio-E5 monitoring project in Norway demonstrates remote snow-depth sensing for winter conditions and smart-city infrastructure.

[Indoor air quality project](https://www.seeedstudio.com/blog/2022/04/27/monitoring-indoor-air-pollutants-the-silent-issue-for-smart-city-iot-using-seeed-lora-e5-and-fusion-pcba/) | [Outdoor solar-powered air quality project](https://www.seeedstudio.com/blog/2021/12/15/solar-powered-outdoor-air-quality-monitor-transmits-data-over-lorawan-with-the-help-of-seeed-fusion/) | [Snow-depth monitoring project](https://www.seeedstudio.com/blog/2022/02/18/low-power-snow-depth-sensor-monitoring-for-iot-smart-city-based-on-lora-e5-applied-in-norway/)

<p style={{textAlign: 'center'}}><img src="https://www.seeedstudio.com/blog/wp-content/uploads/2022/04/4.27-2.png" alt="Wio-E5 indoor air quality monitoring device" width={800} height="auto" /></p>

### Water Resources and Remote Infrastructure Monitoring

- **Stream runoff:** A Wio-E5-based research sensor supports wireless reporting of stream depth, water temperature, and water-quality-related measurements from remote field locations.
- **Smart metering:** Suitable Wio radio modules can connect water meters, flow meters, and utility monitoring controllers to long-range wireless networks for periodic readings and alarm transmission.

[Stream runoff monitoring project](https://www.seeedstudio.com/blog/2022/03/04/former-ph-d-researcher-at-osu-developed-stream-runoff-monitoring-sensors-using-lora-e5-to-measure-the-temperature-quality-and-flow/)

<p style={{textAlign: 'center'}}><img src="https://www.seeedstudio.com/blog/wp-content/uploads/2022/03/%E6%BA%AA%E6%B5%812-1024x1365.jpg" alt="LoRa-E5 stream runoff and water monitoring project" width={800} height="auto" /></p>

### Off-Grid Communication and Asset Tracking

- **Meshtastic handhelds:** Wio-SX1262 can form the LoRa radio subsystem of standalone, phone-free text communicators such as RetroMeshDevice.
- **GPS trackers:** The LIA open-source design combines Wio-SX1262, an external GNSS receiver, and an ESP32-S3 host to exchange location updates and device status over a Meshtastic network.

[RetroMeshDevice project](https://www.seeedstudio.com/blog/2026/08/19/retromeshdevice-a-phone-free-meshtastic-handheld-built-in-public/) | [Pet GPS tracker project](https://www.seeedstudio.com/blog/2026/08/19/lia-an-open-meshtastic-gps-tracker-built-for-off-grid-use/)

<p style={{textAlign: 'center'}}><img src="https://www.seeedstudio.com/blog/wp-content/uploads/2026/08/1-114993390-wio-sx1262-wireless-module-2-1030x773.jpg" alt="Wio-SX1262 LoRa module for off-grid communication and Meshtastic" width={800} height="auto" /></p>

### Drone Systems and Wireless RTK Correction Delivery

- **Drone light shows:** Wio-E5 can carry correction-data messages from a reference-data source to aircraft in a drone fleet. Each aircraft's GNSS/RTK receiver uses those messages together with its own satellite observations to calculate position.
- **Shared wireless broadcast:** A common radio broadcast can distribute the same correction information to multiple receiving aircraft, subject to the selected packet throughput and timing requirements.

[Drone light-show RTK project](https://www.seeedstudio.com/blog/2026/10/21/lora-drone-light-shows-rtk-corrections/)

<p style={{textAlign: 'center'}}><img src="https://www.seeedstudio.com/blog/wp-content/uploads/2026/10/%E6%A8%A1%E7%BB%84%E6%96%87%E7%AB%A0%E6%8F%92%E5%9B%BE%E5%8F%8A%E5%B0%81%E9%9D%A2-8.png" alt="LoRa module for drone light shows and wireless RTK correction delivery" width={800} height="auto" /></p>

### Industrial LoRaWAN Gateways and Network Infrastructure

- **Multi-device reception:** Wio-WM1302, based on Semtech SX1302, provides multi-channel LoRa reception for gateway hardware that serves geographically distributed IoT devices.
- **Industrial gateway integration:** The reComputer R1225 pairs a WM1302 concentrator with a Raspberry Pi Compute Module 4-based host for network forwarding, local processing, and Ethernet or optional cellular backhaul.

[WM1302 + reComputer R1225 gateway architecture](https://www.seeedstudio.com/blog/2026/09/06/industrial-lorawan-gateway-wm1302-r1225/)

<p style={{textAlign: 'center'}}><img src="https://www.seeedstudio.com/blog/wp-content/uploads/2026/09/100021896main_4-1-1030x773.jpg" alt="reComputer R1225 industrial LoRaWAN gateway" width={800} height="auto" /></p>




## Tech Support & Product Discussion

Discover how the Seeed LoRa Modules supports your journey from early evaluation to real-world deployment, with setup guides, reference designs, SDKs, KiCad libraries, hands-on testing, and projects built by developers. Explore connectivity options across LoRa, Wi-Fi, BLE, GNSS, and more, then find the module and purchasing path that match your technical requirements, location, and development stage.

Explore the ++[Wio module portfolio](https://www.seeedstudio.com/wio-module)++, or contact ++[techsupport@seeed.io](mailto:techsupport@seeed.io)++ to discuss your project.



