# 🚒 Fire Fighting Robot using Sensor Fusion

## 📌 Project Overview

This project presents an **Arduino-based Fire Fighting Robot** that detects and extinguishes fire using multiple sensors.

The system uses **sensor fusion** by combining data from flame, smoke, and temperature sensors to improve detection accuracy and reduce false alarms.

---

## 🎯 Objective

To design an autonomous robot that can:

* Detect fire hazards
* Navigate safely
* Extinguish fire without human intervention

---

## 🚀 What This Project Does

Fire accidents are dangerous and require quick response.

👉 This project:

* Detects fire using multiple sensors
* Moves toward the fire source
* Activates a water pump to extinguish it

> 💡 In simple terms:
> A robot that finds fire and puts it out automatically.

---

## ✨ Features

* 🔥 Flame detection using IR sensor
* 🌡️ Temperature monitoring (DHT11)
* 💨 Smoke detection (MQ2 sensor)
* 🤖 Autonomous movement
* 🚿 Automatic water spraying system
* 📊 Real-time simulation dashboard

---

## ⚙️ Methodology

### 🔹 1. Data Sensing

The robot continuously reads:

* Flame sensor (IR)
* Smoke sensor (MQ2)
* Temperature sensor (DHT11)

---

### 🔹 2. Sensor Fusion Logic

Fire is detected when:

* Flame is detected
* OR smoke exceeds threshold
* OR temperature > 45°C

👉 Combining sensors improves reliability.

---

### 🔹 3. Robot Movement

* Moves forward in patrol mode
* Detects obstacles and hazards
* Navigates toward fire source

---

### 🔹 4. Fire Detection & Action

When fire is detected:

* Robot stops immediately
* Activates water pump
* Sprays water until fire is gone

---

### 🔹 5. Recovery

After fire is extinguished:

* Pump turns off
* Robot moves away
* Resumes monitoring

---

## 🧠 Core Concepts Used

* Sensor Fusion
* Embedded Systems
* Arduino Programming
* Robotics Automation
* Real-time Monitoring

---

## 📊 Simulation

The project includes a **web-based simulation dashboard** that shows:

* Sensor values (temperature, flame, smoke)
* Robot status (idle, moving, spraying)
* Real-time fire detection events

---



---

## 🛠️ Hardware Components

* Arduino Uno
* IR Flame Sensor
* MQ2 Smoke Sensor
* DHT11 Temperature Sensor
* L298N Motor Driver
* DC Motors & Wheels
* Water Pump
* Battery Supply

---

## ▶️ How to Run

### 🔧 Hardware

1. Upload `robotics_code.ino` to Arduino
2. Connect sensors and motor driver
3. Power the robot

### 💻 Simulation

1. Open `robotics.html` in a browser
2. Click anywhere to simulate fire events
3. Observe robot behavior

---

## 📊 Output

* ✅ Fire detection using multiple sensors
* 🚿 Automatic fire extinguishing
* 📈 Real-time simulation visualization
* 🤖 Autonomous robot response

---

## 📌 Conclusion

This project demonstrates how **sensor fusion** improves fire detection accuracy and enables safe, automated response using robotics.

It provides a practical solution for reducing human risk in fire emergencies.

---

## 🔮 Future Scope

* 🚗 Integration with real-world fire systems
* 🤖 AI-based fire prediction
* 📡 IoT connectivity for alerts
* 🏙️ Smart building safety systems

---

