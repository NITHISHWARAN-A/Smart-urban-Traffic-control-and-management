# Smart-urban-Traffic-control-and-management

## 🧩 About

An IoT-based smart system designed to monitor traffic flow and environmental conditions in real-time.  
Utilizing an ESP32 microcontroller, it controls traffic lights based on vehicle detection through sensors and also keeps track of air quality, temperature, and humidity.  
Sensor data is transmitted to a webhook for remote monitoring, with live updates displayed on an LCD screen.  
This project aims to contribute towards smarter and safer cities with responsive traffic management and environmental awareness.

---

### Project Link
[🔗 View Project on Wokwi](https://wokwi.com/projects/398934633069967361)

---

## ⚙️ Working Instructions

### 📦 Components Required
- ESP32 Development Board
- MQ135 Gas Sensor
- Ultrasonic Sensor (HC-SR04)
- PIR Motion Sensor
- DHT22 Temperature & Humidity Sensor
- I2C LCD Display (16x2)
- LEDs (Red, Yellow, Green)
- Jumper wires
- Breadboard
- Wi-Fi network

### 🔌 Circuit Connections

| Component               | ESP32 Pin |
|-------------------------|-----------|
| MQ135 (PPM Sensor)      | GPIO 16   |
| PIR Motion Sensor       | GPIO 2    |
| Ultrasonic Trigger Pin  | GPIO 5    |
| Ultrasonic Echo Pin     | GPIO 13   |
| Red LED                 | GPIO 12   |
| Yellow LED              | GPIO 4    |
| Green LED               | GPIO 27   |
| DHT22 Sensor            | GPIO 15   |
| I2C LCD (SDA, SCL)      | GPIO 21, GPIO 22 |

### 🚀 Usage

- **Startup:** ESP32 connects to Wi-Fi and starts monitoring sensors.
- **Motion Detection:** If motion is detected, the red LED turns on, and "Stop Traffic" is displayed.
- **Distance Measurement:** Based on the distance measured by the ultrasonic sensor:
  - **< 20 cm**: Red LED ON (Stop Traffic)
  - **20–50 cm**: Yellow LED ON (Use Caution)
  - **> 50 cm**: Green LED ON (Allow Traffic)
- **Air Quality Monitoring:** Reads gas concentration (PPM) from MQ135.
- **Environment Monitoring:** Displays temperature and humidity on the serial monitor and sends data via webhook.
- **LCD Display:** Real-time status updates.

---

## 💡 Future Improvements

- Add Buzzer for critical alerts.
- Integrate cloud dashboard for live data visualization.
- Solar-powered ESP32 deployment.

---

Feel free to contribute or raise issues!

⭐️ Star this repository if you found it helpful!
