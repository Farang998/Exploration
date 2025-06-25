# Industrial Plant cum Environmental Monitoring System

This project is an **IoT-based Environmental Monitoring System** that integrates sensor networks, industrial communication protocols (MODBUS RTU), MQTT messaging, and a DWIN touch display. It was developed as part of the PC223 course.

## 🚀 Overview

We designed a real-time system using ESP32 microcontrollers to measure and monitor environmental parameters such as:
- Temperature and Humidity (DHT22)
- Atmospheric Pressure (BMP280)
- Current and Voltage (ACS712)
- Air Quality/Gas (MQ135)

## 🔧 System Architecture

### 1. Dual ESP32 Setup with MODBUS RTU
- **Slave ESP32**: Reads data from sensors and sends it via MODBUS.
- **Master ESP32**: Receives sensor data and publishes it via MQTT.

### 2. Node.js + MongoDB Server
- **Node.js** handles MQTT subscription and stores the data using **mongoose** in a MongoDB database.
- Data is received via the `Exploration_sensordata` topic from the MQTT broker (HiveMQ).

### 3. DWIN Display (DGUS-based)
- Displays real-time data with touch functionality.
- Frontend created using DGUS software and deployed via SD card.

## 📦 Tech Stack

- **Hardware**: ESP32, DHT22, BMP280, MQ135, ACS712, DWIN HDL662B
- **Protocols**: MODBUS RTU, MQTT (via HiveMQ)
- **Software**:
  - Arduino IDE (ESP32 programming)
  - Node.js (Express, MQTT, CORS, Mongoose, shortid)
  - MongoDB
  - DGUS Software (DWIN UI)
  - HTML, CSS, JS (for frontend interface)

## 🔗 Repository

[GitHub Repository](https://github.com/Harsh97120/Exploration.git)

## 🛠️ Setup Instructions

### 1. ESP32 Firmware
- Flash slave ESP32 with sensor read + MODBUS write code.
- Flash master ESP32 with MODBUS read + MQTT publish code.

### 2. Node.js Server
```bash
npm install express cors mqtt mongoose shortid
node server.js
