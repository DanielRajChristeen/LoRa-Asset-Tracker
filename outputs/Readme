## 📊 Outputs (Detailed Explanation)

This section provides an in-depth explanation of the key results generated from the development and deployment of the LoRa-based Asset Tracking system. Each output validates a specific stage of implementation, from hardware design to data transmission, anomaly detection, and alert generation.

---

### 🧩 1. Asset Tracker Schematic

![Asset Tracker Schematic](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/raw/main/outputs/asset_tracker_schematic.png)

The asset tracker schematic illustrates the complete hardware integration of the LoRa-based sensor node. It includes essential components such as the Seeed Studio Wio-E5 module, which is powered by the STM32WLE5JC SoC that combines an ARM Cortex-M4 microcontroller with a LoRa radio transceiver. Additionally, the LIS3DHTR accelerometer is connected to detect three-axis movement for anomaly detection. The Quectel L89 GNSS module provides precise location data, and the MP2667 power management IC ensures efficient battery charging and low-power operation. This schematic confirms the functional interconnection between the modules and the robustness of the electrical design, enabling seamless data acquisition, processing, and wireless transmission in a compact footprint.

---

### 🖼️ 2. Device Layout

![Device Layout](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/raw/main/outputs/device_layout.jpg)

The device layout presents the physical implementation of the schematic on a compact Surface-Mount Device (SMD) PCB. Components are carefully positioned to maintain signal integrity and mechanical stability in outdoor and mobile applications. The central placement of the LIS3DHTR accelerometer ensures consistent motion detection, while the GNSS antenna and LoRa transceiver are oriented to minimize interference and maximize reception quality. The layout optimizes space for a lightweight and portable build while maintaining separation between power and communication lines to reduce noise. This fabricated board is the backbone of the asset tracker and demonstrates readiness for rugged, field-level deployment.

---

### 🗺️ 3. Tracking Map

![Tracking Map](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/raw/main/outputs/tracking_map.png)

The tracking map displays real-time geographic positions transmitted from the GNSS-enabled sensor node to The Things Stack cloud infrastructure. The data packets include latitude and longitude coordinates obtained from the Quectel L89 module, along with movement status flags. This information is processed and visualized using third-party mapping tools such as TTN Mapper or Firebase. The successful mapping of these coordinates confirms that the system accurately captures and reports the physical location of tracked assets. This feature is critical for applications such as fleet tracking, warehouse logistics, and smart agriculture, where continuous position monitoring is essential.

---

### 📉 4. Anomaly Detection Graph

![Anomaly Detection Graph](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/raw/main/outputs/anomaly_detection_graph.png)

This output graph represents the detection of abnormal movements, such as sudden shocks, tilts, or free falls, based on data from the LIS3DHTR accelerometer. A machine learning model trained using Edge Impulse and Mahalanobis Distance analysis processes three-axis acceleration data to classify events as normal or abnormal. The plotted data illustrates clear spikes during anomalous activity and baseline behavior during periods of stability. This graph is essential for evaluating the effectiveness of the model and verifying that the device can intelligently recognize unusual patterns in movement, a key feature for theft detection or equipment misuse.

---

### ✅ 5. Anomaly Detection Accuracy

![Anomaly Detection Accuracy](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/raw/main/outputs/anomaly_detection_accuracy.png)

This plot illustrates the training and testing accuracy of the anomaly detection model. With 2000 labeled samples (1000 normal and 1000 abnormal), the model achieved a classification accuracy of 95.06%. The training process successfully differentiated between typical operational vibrations and suspicious events. The high level of accuracy indicates that the model can reliably operate in field conditions and supports the real-time classification of sensor readings on the edge device (Wio-E5), without needing cloud computation. This result underlines the project's success in deploying lightweight intelligence on embedded hardware.

---

### 📡 6. GNSS Signal Quality

![GNSS Satellite Signal Quality](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/raw/main/outputs/gnss_signal_quality.png)

The satellite signal quality graph evaluates the signal-to-noise ratio (SNR) of various GNSS signals acquired by the Quectel L89 module. Each bar represents the strength of individual satellite connections during operation. Strong, stable signals are crucial for achieving fast fixes and maintaining high location accuracy, especially in dynamic environments. This analysis confirms that the GNSS module can consistently lock onto multiple satellites with high signal integrity, which is essential for reliable geo-fencing and location monitoring.

---

### 🌌 7. GNSS Sky View Plot

![GNSS Sky View Plot](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/raw/main/outputs/gnss_skyview_plot.png)

The GNSS sky view plot shows the positional distribution of satellites overhead at the time of data capture. It helps visualize which satellites are available and in use by the GNSS receiver for triangulation. A balanced spread across the sky with strong elevation angles ensures better positioning accuracy. This visualization validates the multi-constellation capability of the L89 module, which can access GPS, GLONASS, BeiDou, and IRNSS networks simultaneously for faster and more robust location fixes.

---

### 📍 8. Geo-Fencing Implementation

![Geo-Fencing Implementation](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/raw/main/outputs/geofencing_demo.png)

The geo-fencing implementation plot demonstrates how virtual boundaries are established using GNSS coordinates. When the tracked asset crosses these defined boundaries, the device sends alert packets via LoRaWAN to the cloud. The Things Stack then triggers notifications based on coordinate comparison logic. This output confirms the successful deployment of dynamic perimeter monitoring, which is essential for securing high-value assets in transit or within restricted areas. The geo-fencing logic runs on-device, ensuring low latency and offline functionality even without persistent internet access.

---

### 📧 9. Email Alert Notification

![Email Alert](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/raw/main/outputs/email_alert.png)

The email alert demonstrates the system's ability to notify users via SMTP when an anomaly or geo-fence breach is detected. The payload includes information such as event type, timestamp, and current location. The email functionality ensures users receive immediate updates on critical movements or incidents, making the system effective in scenarios like theft prevention or hazardous condition alerts. It offers seamless integration with platforms like Gmail using Python or Node-RED.

---

### 💬 10. Telegram Bot Notification

![Telegram Bot](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/raw/main/outputs/telegram_bot_alert.png)

This screenshot shows a Telegram bot sending a real-time alert to the user when a threshold breach or unauthorized motion is detected. It includes relevant context such as timestamp and asset location. Using Telegram bots provides a secure, free, and scalable messaging channel, which is ideal for mobile-first asset managers or logistics operators who need prompt updates without relying on SMS networks.

---

### 📱 11. SMS Alert Notification

![SMS Alert](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/raw/main/outputs/sms_alert.png)

The SMS alert demonstrates fallback notification capability in low-connectivity or rural regions. It is triggered by server-side logic or cloud functions when an alert packet is received. SMS alerts ensure that even users without internet connectivity can receive critical information promptly, making the system resilient and inclusive for varied field conditions.

---

These outputs collectively demonstrate the system’s complete life cycle — from hardware validation and firmware deployment to intelligent sensing, communication, and alert delivery. Each visual reinforces the functional reliability of the LoRa-based asset tracking system and its potential scalability across diverse real-world applications.

