# 🌐 SDN-Based IoT Traffic Monitoring & Anomaly Detection System

## 📌 Project Overview
This project implements an **Anomaly Detection System for IoT Networks** using **Software Defined Networking (SDN)**.

The system uses:
- 🌐 **Mininet** to simulate IoT network topology  
- 🧠 **Ryu SDN Controller** for centralized control  
- 📊 **Flow statistics analysis** to detect abnormal traffic  

It continuously monitors network traffic and identifies suspicious behavior based on packet flow rates.

---

## 🎯 What This Project Does

IoT networks are highly vulnerable to attacks due to limited security.

👉 This project:
- Monitors real-time traffic using SDN controller  
- Calculates packet flow rate for each communication  
- Classifies traffic into severity levels  
- Automatically blocks malicious flows  

📌 In simple terms:
> This project detects abnormal traffic in IoT networks and temporarily blocks suspicious devices to maintain network security.

---

## 🚀 Features

- 🌐 IoT network simulation using Mininet  
- 📡 Centralized monitoring using Ryu SDN controller  
- 📊 Flow statistics-based traffic analysis  
- ⚠️ Severity classification (Normal, Low, Medium, High)  
- 🚫 Automatic blocking of high-risk flows  
- 🔄 Automatic unblocking after timeout  
- 🧠 Real-time anomaly detection  

---

## ⚙️ Methodology

The system follows a structured SDN-based workflow:

---

### 🔹 Step 1: IoT Network Setup

- Create IoT topology using Mininet :contentReference[oaicite:0]{index=0}  
- Components:
  - Switch (`s1`)  
  - IoT Devices (`h1`, `h3`)  
  - Server (`h2`)  

👉 All devices are connected through an OpenFlow switch  

---

### 🔹 Step 2: SDN Controller Initialization

- Ryu controller (`flow_monitor.py`) is started :contentReference[oaicite:1]{index=1}  
- Establish connection between:
  - Switch  
  - Controller  

👉 Controller maintains:
- Flow statistics  
- Device mappings  
- Blocked flows list  

---

### 🔹 Step 3: Packet Handling & MAC Learning

- Incoming packets are processed by controller  
- Learn:
  - Source MAC → Port mapping  
- If destination unknown:
  - Packet is flooded  
- Otherwise:
  - Forwarded to correct port  

👉 Flow rules are installed dynamically  

---

### 🔹 Step 4: Flow Statistics Monitoring

- Controller periodically collects:
  - Source IP  
  - Destination IP  
  - Packet count  

- Packet rate is calculated as:

  Rate = (Current Packets - Previous Packets) / Time Interval  

👉 Monitoring interval = 5 seconds  

---

### 🔹 Step 5: Anomaly Detection

Traffic behavior is analyzed using **threshold-based detection**:

- Normal → rate < 20  
- Low → 20 < rate < 50  
- Medium → 50 < rate < 100  
- High → rate > 100  

👉 High rate indicates possible attack or abnormal behavior  

---

### 🔹 Step 6: Severity Classification

Each flow is classified as:

- 🟢 NORMAL  
- 🟡 LOW  
- 🟠 MEDIUM  
- 🔴 HIGH  

👉 Based on packet rate  

---

### 🔹 Step 7: Automated Mitigation

- If severity = HIGH:
  - Flow is **blocked automatically**  
  - Drop rule installed in switch  

- Blocking uses:
  - `idle_timeout = 30 sec`  
  - `hard_timeout = 60 sec`  

👉 After timeout, flow is automatically unblocked  

---

### 🔹 Step 8: Continuous Monitoring

- System runs continuously  
- Tracks:
  - Flow rates  
  - Alerts generated  
  - Blocked flows  

👉 Ensures real-time network protection  

---

##  Core Concepts Used

- Software Defined Networking (SDN)  
- OpenFlow Protocol  
- Flow Table Management  
- Network Traffic Analysis  
- Anomaly Detection  
- Threshold-Based Classification  



 

---


## 📊 Output

- Real-time traffic logs:
  - Source IP  
  - Destination IP  
  - Packet rate  

- Severity classification display  
- Alerts for abnormal traffic  
- Automatic blocking messages  
- Flow unblocking after timeout  

---

##  Conclusion

This project demonstrates how **SDN enables centralized monitoring and control of IoT networks**.

It effectively:
- Detects abnormal traffic patterns  
- Classifies severity levels  
- Automatically mitigates threats  

 Improving network security and stability  

---

## 🔮 Future Scope

- Machine learning-based anomaly detection  
- Detection of specific attacks (DDoS, botnets)  
- Large-scale IoT deployment  
- Real-time dashboard visualization  
