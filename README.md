
# EMBRACE – Embedded Monitoring Band for Real-Time Anxiety & Cognitive Evaluation

Project Description

EMBRACE is a wearable stress monitoring system designed to detect stress levels in real time using heart rate analysis. The system continuously monitors the user's heart rate through a PPG-based sensor and compares the readings with a personalized baseline value. When an abnormal increase in heart rate is observed for a sustained duration, the system identifies the condition as stress and generates alerts.

The project aims to provide a lightweight, portable, and cost-effective solution for stress awareness, particularly in academic environments where students often experience stress due to examinations, assignments, and deadlines.

Hardware Components

MAX30102 / MAX30100 Heart Rate Sensor

Measures heart rate using Photoplethysmography (PPG) technology. The sensor detects variations in blood flow and sends pulse signals to the ESP32 for processing.

ESP32 Microcontroller

Acts as the central processing unit of the system. It acquires sensor data, calculates heart rate (BPM), establishes the baseline value, performs stress detection, and manages Bluetooth communication.

LED Indicator

Provides visual alerts whenever stress is detected. Different LED states can indicate normal and stress conditions.

Bluetooth Module (Built into ESP32)

Enables wireless transmission of heart rate readings and stress notifications to a smartphone or monitoring application.

Lithium-Ion Battery / Power Supply

Provides portable power for continuous operation of the wearable device.

Connecting Wires and Breadboard

Used for interfacing the heart rate sensor, ESP32, LED, and power supply during implementation and testing.

---

Software Used

Arduino IDE

Used for writing, compiling, and uploading Embedded C/C++ code to the ESP32 microcontroller.

ESP32 Libraries

Provide support for sensor interfacing, Bluetooth communication, and hardware control.

Serial Monitor / Web Dashboard (if used)

Displays heart rate readings, baseline values, and stress status during real-time monitoring.

---

Execution Steps

1. Power ON the EMBRACE device.
2. The heart rate sensor starts capturing pulse signals from the user's finger or wrist.
3. The ESP32 receives and processes the sensor data.
4. During the initial calibration phase, multiple heart rate readings are collected to establish a personalized baseline heart rate.
5. The system continuously calculates heart rate in Beats Per Minute (BPM).
6. Real-time BPM values are compared with the stored baseline value.
7. If the BPM increases approximately 15–25 BPM above the baseline for a sustained duration, the system identifies the condition as stress.
8. The LED indicator is activated to alert the user.
9. Heart rate data and stress notifications are transmitted wirelessly via Bluetooth for monitoring.
10. The monitoring process continues in real time until the device is turned OFF.

---

Stress Detection Workflow

Input Stage

- Heart rate signals are collected using the PPG sensor.

Processing Stage

- Sensor signals are filtered to remove noise.
- Heart rate is calculated in BPM.
- Baseline heart rate is established during calibration.

Analysis Stage

- Current BPM is continuously compared with the personalized baseline value.
- Threshold-based stress detection is performed.

Output Stage

- Stress status is displayed.
- LED alerts are generated.
- Bluetooth notifications are transmitted to connected devices.

---

Applications

- Student stress monitoring
- Academic wellness tracking
- Personal health awareness
- Wearable healthcare systems
- Real-time physiological monitoring

Future Enhancements

- Integration of GSR and temperature sensors
- Machine learning-based stress prediction
- Mobile application development
- Cloud-based data storage
- Long-term stress analytics
- Multi-parameter health monitoring
