# IoT-Smart-Switchboard-Energy-Monitor
# IoT Smart Switchboard with Energy Monitoring

A smart home automation system designed to remotely control AC appliances and monitor real-time electrical parameters using IoT technology.  
Powered by **ESP32**, **PZEM-004T Energy Meter**, **Active-Low Relay**, and **Blynk Cloud Platform**.

---

## ✨ Key Features

- Remote ON/OFF control via smartphone (Blynk IoT)
- Local control through push button
- Real-time monitoring:
  - Voltage (V)
  - Current (A)
  - Active Power (W)
  - Energy Consumption (kWh)
  - Frequency (Hz)
  - Power Factor
- LCD display for offline visibility
- Wi-Fi connectivity indicator
- Compact and safe switchboard design

---

## 🧩 Components Used

| Component | Specification |
|----------|---------------|
| ESP32 Dev Board | Wi-Fi + BLE microcontroller |
| PZEM-004T v3.0 | Energy measurement module (CT based) |
| Relay Module | Active-Low switching control |
| 16x2 LCD with I2C | Two-wire display interface |
| Push Button | Manual toggle |
| Socket & Wiring | AC load connection |
| Wi-Fi Router / Hotspot | Internet connectivity |

---

## 🔌 Circuit Overview

Interface Mapping:

| Function | ESP32 Pin |
|---------|-----------|
| Relay Control | GPIO 13 |
| Push Button | GPIO 14 (INPUT_PULLUP) |
| Wi-Fi Status LED | GPIO 2 |
| LCD SDA | GPIO 21 |
| LCD SCL | GPIO 22 |
| PZEM004T RX | GPIO 16 |
| PZEM004T TX | GPIO 17 |

project circuit diagram
(iot project ckt diagram.pdf) 

---

## 📱 Blynk Integration

Virtual Pin Assignments:

| Blynk Pin | Data |
|----------|------|
| V0 | Relay Switch |
| V1 | Voltage |
| V2 | Current |
| V3 | Power |
| V4 | Energy |
| V5 | Frequency |
| V6 | Power Factor |

⚠️ Update credentials in the code:
```cpp
#define BLYNK_AUTH_TOKEN "YOUR_AUTH_TOKEN"
char ssid[] = "YOUR_WIFI_NAME";
char pass[] = "YOUR_WIFI_PASSWORD";
