# Environmental Monitoring System

This project is a real-time IoT-based **Environmental Monitoring System** using ESP32 microcontrollers, which measures and transmits sensor data including:

- Temperature and Humidity (DHT22)
- Pressure (BMP280)
- Current and Voltage (ACS712)
- Air Quality/Gas Concentration (MQ135)

### Core Components

- **ESP32 Slave**: Collects sensor data and sends it via MODBUS RTU protocol.
- **ESP32 Master**: Receives the data and publishes it using MQTT protocol to a Node.js server.
- **Node.js Server**: Stores data into MongoDB using Mongoose, and communicates via the HiveMQ broker.
- **DWIN Touch Display**: Displays data using DGUS GUI interface, built with HTML/CSS and JavaScript.

### Technologies Used

- Arduino IDE with ESP32
- MODBUS RTU Protocol
- MQTT Protocol (HiveMQ broker)
- Node.js + Express + Mongoose
- MongoDB
- DGUS Software for DWIN display

---

For detailed design, setup, and explanation:

- 📄 See `Project_Report.pdf`
- 🖼️ See `Project_Poster.pdf`
- 💻 Final code is available in:
  - `Final_Master.ino`
  - `Final_Slave.ino`
