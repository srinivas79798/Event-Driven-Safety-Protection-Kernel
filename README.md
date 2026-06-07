# Event-Driven Safety Protection Kernel

## Overview

The Event-Driven Safety Protection Kernel is an ESP32-based battery safety controller designed to monitor and protect multi-cell battery systems in real time. The project uses a fully non-blocking event-driven architecture based on `millis()` timing, eliminating the use of `delay()` and enabling efficient real-time operation.

The system continuously monitors battery cell voltages and detects abnormal conditions such as weak cells, overvoltage events, sensor anomalies, and rapid voltage fluctuations. When a fault is detected, the controller activates safety mechanisms including relay cutoff, buzzer alerts, and LCD warning messages.

---

## Features

* Real-time battery voltage monitoring
* Weak cell detection
* Overvoltage protection
* Sensor fault detection
* Rapid voltage fluctuation detection
* Relay cutoff for battery protection
* Buzzer-based fault alerts
* LCD warning display
* Recovery logic for automatic fault clearing
* Anti-relay chatter protection
* Fully non-blocking `millis()`-based architecture

---

## Hardware Components

* ESP32 Development Board
* 16x2 I2C LCD Display
* Relay Module
* Active Buzzer
* Voltage Input Sources (Battery Cell Simulation)
* Connecting Wires

---

## System Operation

1. Read battery cell voltages continuously.
2. Analyze voltage levels and system conditions.
3. Detect fault events:

   * Weak Cell
   * Overvoltage
   * Sensor Fault
   * Rapid Voltage Fluctuation
4. Trigger protection mechanisms.
5. Display fault information on LCD.
6. Activate buzzer alerts.
7. Disconnect battery pack through relay when required.
8. Restore normal operation after fault recovery.

---

## Safety Functions

### Weak Cell Protection

Detects battery cells operating below safe voltage limits.

### Overvoltage Protection

Disconnects the battery pack when voltage exceeds safe thresholds.

### Sensor Fault Detection

Identifies invalid sensor readings and activates fault handling procedures.

### Voltage Fluctuation Monitoring

Detects unstable battery behavior caused by rapid voltage changes.

### Anti-Relay Chatter Logic

Prevents excessive relay switching during unstable operating conditions.

---

## Software Architecture

The project follows an event-driven design where independent tasks execute using `millis()` timers.

Main tasks include:

* Voltage Monitoring
* Fault Detection
* Relay Control
* Buzzer Control
* LCD Updates
* Recovery Monitoring

This architecture improves responsiveness, reliability, and scalability.

---

## Development Environment

* Arduino IDE
* ESP32 Board Package
* Wokwi Simulator (for testing)

---

## Applications

* Battery Management Systems (BMS)
* Electric Vehicles (EVs)
* Energy Storage Systems
* Industrial Battery Protection
* Embedded Safety Controllers

---

## Future Improvements

* IoT-based remote monitoring
* Temperature monitoring integration
* Current sensing support
* Data logging to cloud platforms
* Advanced battery diagnostics

---

## Author

**Sudanapalli Srinivas**
B.Tech – Electronics and Communication Engineering

---

