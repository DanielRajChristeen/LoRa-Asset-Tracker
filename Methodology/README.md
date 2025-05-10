# 📂 Methodology

This directory contains visual diagrams that illustrate key components of the LoRaWAN-based asset tracking system. Each section below includes an image followed by a detailed explanation.

---

## 🧭 Architecture Overview

![Architecture.png](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/blob/main/Methodology/Architecture.png)

This diagram illustrates the complete end-to-end architecture of a LoRaWAN-based asset tracking system. Sensor nodes equipped with location and motion sensors are deployed within a geo-fenced area and communicate wirelessly using the LoRaWAN protocol. These nodes transmit data to LoRa gateways, which forward it to a centralized LoRaWAN network server—specifically, The Things Stack V3.0. The server handles network management, routing, and device authentication. The data is then pushed to a cloud application server such as Firebase via HTTP or MQTT protocols. Firebase manages cloud storage and event-driven alerting. From here, users can monitor assets in real time using a live dashboard, while alerts and notifications are sent via email, Telegram, and SMS. This system provides end-users with an intuitive and reliable interface for remote asset management.

---

## 🔧 LoRa Tracker Block Diagram

![LoRa Tracker block diagram.jpg](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/blob/main/Methodology/LoRa%20Tracker%20block%20diagram.jpg)

This block diagram shows the internal hardware architecture of the LoRa-based tracking device. At the center is the LoRa-E5 MCU, which coordinates communication and control. It interfaces with a GNSS module (Quectel L89) via UART to gather geolocation data. An onboard accelerometer (LIS3DHTR) communicates over I2C to detect motion and orientation, supporting anomaly detection. Additional GPIO connections support a user switch, an LED indicator, and a buzzer for alerts. The system is powered by a 402025 Li-Po battery and a USB Type-C interface managed by a PMIC (Power Management IC). The Power Header allows for programming and debugging through SWCLK and SWDIO lines. This setup enables compact, energy-efficient asset tracking with support for both location awareness and alerting.

---

## 🌐 LoRa Gateway Block Diagram

![LoRa-Gateway block diagram.png](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/blob/main/Methodology/LoRa_Gateway_block_diagram.png)

This diagram highlights the gateway-level architecture for relaying sensor data to the cloud. The setup consists of a LoRa Gateway Module and a microprocessor (such as a Raspberry Pi), connected via an SPI interface. A common power supply supports both components. The microprocessor manages packet forwarding and handles cloud communication via an Ethernet (internet) connection. This architecture ensures seamless data relay from end devices to cloud servers, playing a crucial role in LoRaWAN deployments by bridging long-range sensor communication with internet-based services.

---

## 📦 Payload Structure

![Payload structure.png](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/blob/main/Methodology/Payload%20structure.png)

The payload structure used for data transmission is designed to be lightweight and informative. It consists of five fields: Latitude (in degrees), Longitude (in degrees), and Altitude (in meters), which provide the physical location of the asset. The Emergency Alert field is a binary flag indicating whether a critical condition (such as a fall or breach) has occurred (1 for alert, 0 for none). The final field, Anomaly Detection Result, also uses a binary value to represent detected anomalies (1 for abnormal behavior, 0 for normal). This structure supports real-time geolocation monitoring and intelligent alerting with minimal transmission overhead.

---

📁 *Return to the main project [here](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker).*
