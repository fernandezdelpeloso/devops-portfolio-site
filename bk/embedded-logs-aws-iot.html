---
layout: default
title: Embedded Device Logging to AWS IoT Project
permalink: /projects/embedded-logs-aws-iot.html
---

# Logging Embedded Device Data to AWS IoT Core

## 🔍 Project Overview
This project demonstrates how to connect an **embedded device** to **AWS IoT Core**, sending telemetry data (e.g., temperature, humidity, voltage) using the **MQTT protocol**. The goal is to enable real-time monitoring and data collection in the cloud from low-cost edge hardware.

## 🧰 Tools & Technologies
- **AWS IoT Core**
- **MQTT Protocol** (via `paho-mqtt` / native SDK)
- **STM32 or Arduino Uno R3** (or BeagleBone Black)
- **Python for PC-side testing**
- **CloudWatch / AWS Timestream** for metrics and storage

## 📷 Architecture Diagram
![IoT Logging Diagram](../assets/embedded-iot-logging-placeholder.png)

## 📁 Repository
- GitHub: [embedded-logs-aws-iot](https://github.com/fernandezdelpeloso/embedded-logs-aws-iot)

## 📡 Project Flow
1. Device reads sensor values (e.g., from I²C/analog input)
2. Data is serialized as JSON and published via MQTT
3. AWS IoT Core receives data and forwards to:
   - CloudWatch Logs
   - Timestream or DynamoDB
   - Lambda (for alerting or processing)

## 🔐 AWS IoT Setup
1. Create a **Thing** in AWS IoT
2. Generate and download the **X.509 certificate** and keys
3. Attach a policy allowing publish/subscribe to `iot/topic`
4. Note endpoint: `XXXXXXXXX-ats.iot.<region>.amazonaws.com`

## 🧪 MQTT Test Script (Python)
```python
import paho.mqtt.client as mqtt
import json

client = mqtt.Client()
client.tls_set("root-CA.crt")
client.username_pw_set("<thingName>", password=None)
client.connect("<iot-endpoint>", 8883, 60)

data = {"temperature": 24.7, "voltage": 3.2}
client.publish("iot/ed/logs", json.dumps(data))
client.disconnect()
```

## 🧠 Lessons Learned
- Managing TLS on microcontrollers
- Efficient message encoding for constrained devices
- IAM permissions and IoT policies
- Using AWS IoT Rules Engine to route data

## 📌 Next Steps
- Integrate sensor readings from real devices
- Add local buffering for offline fallback
- Visualize data with Grafana + Timestream
- Trigger alerts based on thresholds using Lambda or EventBridge

---

**Back to [Home](../index.html)**
