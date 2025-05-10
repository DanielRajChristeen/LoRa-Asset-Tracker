## 📊 Outputs (Detailed Explanation)

This section presents and explains the critical outputs obtained from the LoRa-based Asset Tracking and Geo-Fencing system during its development, testing, and validation phases.

---

### 🧩 1. LoRa Tracker Module

![LoRa Tracker Module](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/blob/main/outputs/LoRa%20Tracker%20module.jpeg)

The customized LoRa Tracker Node was successfully fabricated using a compact Surface-Mount Device (SMD) design. It integrates core components such as the Seeed Studio Wio-E5 LoRa module, Quectel L89 GNSS module, LIS3DHTR accelerometer, a power management IC, USB Type-C interface, and a GPIO-controlled power switch. The PCB design prioritized low power consumption, minimized footprint, and ensured seamless communication. The fabricated hardware was enclosed in a protective casing, making it suitable for outdoor real-time asset tracking and geo-fencing applications:contentReference[oaicite:0]{index=0}.

---

### 🛠️ 2. LoRa Gateway Setup

![LoRa Gateway Setup](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/blob/main/outputs/LoRa-Gateway%20setup.jpeg)

The LoRaWAN gateway was built using the WM1302 module, Raspberry Pi 4, and WM1302 Pi HAT. This setup established reliable connectivity with The Things Network (TTN). The process involved firmware flashing, hardware configuration, and gateway registration on TTN. The Raspberry Pi acted as the computational backbone, managing packet forwarding and ensuring the secure transmission of sensor data. Successful data flow from the tracker to the TTN console validated the communication infrastructure:contentReference[oaicite:1]{index=1}.

---

### 📈 3. Anomaly Detection Graph

![Anomaly Detection Graph](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/blob/main/outputs/anomaly%20detection%20graph.jpg)

The anomaly detection model was trained using real-time accelerometer data collected under both normal and abnormal movement conditions. The model effectively distinguished between standard and suspicious asset motion using Mahalanobis Distance analysis. The output graph demonstrates clear separation between predicted and actual categories, confirming the model’s ability to classify movement anomalies accurately:contentReference[oaicite:2]{index=2}.

---

### 📊 4. Anomaly Detection Accuracy

![Anomaly Detection Accuracy](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/blob/main/outputs/anomaly%20detction%20accuracy%20graph.png)

To validate model performance, an accuracy validation graph was generated, revealing a classification accuracy of 96.73%. The model’s learning curve stabilized over several epochs, indicating its capacity to generalize well on unseen data and effectively support the detection of real-time abnormal asset movements:contentReference[oaicite:3]{index=3}.

---

### 📡 5. GNSS Satellite Signal Quality

![GNSS Satellite Signal Quality](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/blob/main/outputs/GNSS%20Satellite%20signal%20Quality%20Graph.png)

This graph illustrates the Signal-to-Noise Ratio (SNR) of satellites detected during real-time field testing. The evaluation showed the presence of 11 GPS, 7 Galileo, and 1 SBAS satellite, with most SNR values ranging between 20–35 dB-Hz. These strong signals confirmed stable satellite visibility, essential for accurate position tracking and geo-fence operations:contentReference[oaicite:4]{index=4}.

---

### 🌌 6. GNSS Sky View Plot

![GNSS Sky View Plot](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/blob/main/outputs/GNSS%20Sky%20View%20Plot.jpg)

The GNSS sky plot provides a spatial visualization of the satellites in use during field testing. It shows azimuth and elevation angles across GPS, Galileo, and SBAS constellations. The plot confirmed optimal satellite distribution, reduced Position Dilution of Precision (PDOP), and overall superior geo-location geometry—essential for maintaining continuous tracking performance:contentReference[oaicite:5]{index=5}.

---

### 🗺️ 7. Dashboard with Geo-Fence Feature

![Dashboard with Geo-Fence](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/blob/main/outputs/dashboard%20with%20Geo-Fence%20feature.jpeg)

The geo-fencing mechanism was implemented by defining virtual boundaries via latitude and longitude in The Things Network Stack. The system continuously monitored GNSS data to determine asset location and flagged events when a breach occurred. This provided proactive boundary monitoring and enhanced asset security by detecting unauthorized exits from defined zones:contentReference[oaicite:6]{index=6}.

---

### 📧 8. Email Alert

![Email Alert](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/blob/main/outputs/E-mail%20alert.jpg)

Email alert notifications were generated when the system detected a geo-fence breach or abnormal movement. Alerts were automatically triggered and relayed through Firebase to registered users, containing time, location, and event specifics. This ensured swift and reliable stakeholder awareness and response during critical incidents:contentReference[oaicite:7]{index=7}.

---

### 💬 9. Telegram Alert

![Telegram Alert](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/blob/main/outputs/telegram-alert.jpg)

Telegram bot notifications were integrated as part of the multi-channel alert mechanism. These notifications delivered real-time updates about asset status or geo-fence violations to users, enabling responsive field intervention. The bot offered a free, encrypted, and scalable notification alternative on mobile platforms:contentReference[oaicite:8]{index=8}.

---

### 📱 10. SMS Alert

![SMS Alert](https://github.com/DanielRajChristeen/LoRa-Asset-Tracker/blob/main/outputs/sms-alert.jpg)

To ensure connectivity in low-network environments, SMS alerts were implemented. These messages were triggered automatically via Firebase and conveyed essential details about asset status. SMS integration enhanced system reliability by providing fallback notification in scenarios where email or internet-based messaging might fail:contentReference[oaicite:9]{index=9}.

---

Each of these outputs validates a specific functionality of the system—hardware deployment, communication reliability, intelligent sensing, and responsive alerting—ultimately proving the success of the LoRa-based Asset Tracking and Geo-Fencing solution.
