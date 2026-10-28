# Automated Gas Leak Detection & Mitigation System

An Arduino Uno embedded system that continuously monitors air quality, alerts on hazardous gas levels, and automatically runs an exhaust fan to ventilate leaks.

---

## Features

- **Real-Time Monitoring:** Reads analog gas levels using an MQ gas sensor.
- **LCD Display:** Shows live PPM readings and current status (`SAFE` / `ALERT`).
- **Alarms:** 
  - **Normal:** Green LED on
  - **Leak:** Red LED on + Buzzer alarm
- **Active Mitigation:** Triggers a 5V relay module to run an exhaust fan whenever gas exceeds **100 PPM**.

---

## Components

- **Arduino Uno**
- **MQ Gas Sensor** (MQ-2 / MQ-4)
- **16x2 LCD Display**
- **5V Relay Module** + **Exhaust Fan**
- **Active Buzzer** & **LEDs** (Red, Green)

---

## Logic Summary

| Gas Level | Status | Indicators | Relay / Fan |
| :--- | :--- | :--- | :--- |
| **< 100 PPM** | `SAFE` | Green LED ON | OFF |
| **≥ 100 PPM** | `ALERT` | Red LED + Buzzer ON | ON (Ventilating) |

---

## How to Run

1. Open `sketch.ino` in the [Arduino IDE](https://www.arduino.cc/en/software).
2. Connect your Arduino Uno and upload the code.
3. Test virtually using the [Wokwi Simulation](https://wokwi.com/projects/477779837293426689#).
