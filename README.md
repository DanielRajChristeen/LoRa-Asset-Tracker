# LoRa-Based Asset Tracking with Geo-Fencing

A secure and energy-efficient asset tracking system leveraging LoRaWAN technology for long-range communication. Built using the STM32WLE5JC (Wio-E5) and Quectel L89 GNSS module, the system offers real-time location tracking, geo-fencing alerts, emergency button support, and anomaly detection using Mahalanobis Distance.

---

## 🚀 Features

- 📍 Real-time GPS tracking using Quectel L89 R2.0  
- 🌐 LoRaWAN-based long-range, low-power communication  
- 🛑 Geo-fencing with virtual boundary breach alerts  
- 🚨 Emergency alert system with panic button support  
- 📊 Anomaly detection using Mahalanobis Distance (fall detection, irregular movement)  
- 🔋 Power-efficient design with MP2667 Power Management IC  
- ☁️ Data visualization via The Things Stack V3 & Firebase  
- 🧱 Modular SMD hardware for scalable deployment  

---

## 🧩 Hardware Used

| Component            | Description                            |
|---------------------|----------------------------------------|
| Wio-E5 Dev Board    | LoRaWAN module with STM32WLE5JC        |
| Quectel L89 R2.0    | GNSS module for GPS                    |
| LIS3DHTR            | 3-axis accelerometer                   |
| MP2667              | Power management IC                    |
| Raspberry Pi 4B     | Gateway host system                    |
| WM1302 LoRa Gateway | LoRaWAN gateway module                 |
| 3.6V Li-Po Battery  | Power source for node                  |

---

## 🛠️ Software Stack

- **Embedded C (STM32CubeIDE)** – Firmware for sensor node  
- **Python & Node.js** – Backend data handling and visualization  
- **JavaScript (TTN Payload Formatter)** – Payload decoding  
- **The Things Stack (TTN)** – LoRaWAN network server  
- **Firebase** – Real-time database & alert system  

---

## 📡 System Architecture

1. **Sensor Node**  
   - Collects GPS & accelerometer data  
   - Detects anomalies using Mahalanobis Distance  
   - Sends LoRa payload to TTN  

2. **Gateway**  
   - WM1302 with Raspberry Pi 4  
   - Forwards packets to The Things Stack V3  

3. **Cloud**  
   - TTN decodes and forwards data to Firebase  
   - Firebase triggers alerts and dashboard updates  

---

## 📦 Payload Format

The payload sent from the sensor node over LoRa follows a comma-separated string format:

### 🧾 Field Descriptions

| Field              | Description                                |
|-------------------|--------------------------------------------|
| `latitude`         | GNSS latitude in decimal degrees            |
| `longitude`        | GNSS longitude in decimal degrees           |
| `altitude`         | Altitude in meters                         |
| `emergency_status` | `1` = Panic button pressed, `0` = Normal   |
| `anomaly_status`   | `1` = Anomaly detected, `0` = Normal       |

---

## 🔍 Anomaly Detection

Anomaly detection is based on the **Mahalanobis Distance** algorithm to identify irregular patterns in motion, such as:

- Free fall  
- Excessive vibration  
- Sudden orientation changes  

---

## 📈 Applications

- Logistics & supply chain  
- Fleet & vehicle management  
- Smart agriculture  
- Construction equipment tracking  
- Coastal vessel monitoring  
- Urban infrastructure monitoring  

---

## 📬 Alerts & Notifications

- **Geo-fence breach** → Email/SMS/Telegram  
- **Emergency button press** → Real-time alert  
- **Anomaly detection** → Logged in dashboard  

---

## 🔒 Security

- Unique DevEUI, AppKey, and OTAA authentication  
- Encrypted communication via LoRaWAN security stack  
- Firebase HTTPS endpoints for secure data handling  

---

## 🎥 Project Overview Video

📺 Watch the full project overview here:  
[https://youtu.be/-xaInsjvY7k?si=eaUaM28JZm8MWVSY](https://youtu.be/-xaInsjvY7k?si=eaUaM28JZm8MWVSY)

---

## 📚 Contributors

- **Adhikesavan M**  
- [**Daniel Raj C**](https://github.com/DanielRajChristeen)  
- **Dibesh S**  
- [**Hrithik Kumar J**](https://github.com/hrithikkumar1211)

> Department of Electronics and Communication Engineering  
> Vel Tech Multi Tech Dr. Rangarajan Dr. Sakunthala Engineering College  
> Anna University, Chennai

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 🌐 Acknowledgements

- Guided by **Dr. A. Karthikeyan**, M.E.., Ph.D., Vel Tech Multi Tech Dr. Rangarajan Dr. Sakunthala Engineering College. 
- Thanks to **NEEVEE Technologies** for hardware guidance  
- Supported by Anna University curriculum and ECE department, Vel Tech Multi Tech Dr. Rangarajan Dr. Sakunthala Engineering College.
