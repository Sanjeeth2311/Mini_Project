<xaiArtifact artifact_id="98a651c8-8556-45d7-8090-f2bd65e06474" artifact_version_id="7135d2e6-3d7a-470c-9bc0-ba2f0904370c" title="README.md" contentType="text/markdown">

# IoT-Based Livestock Animal Tracking and Health Monitoring System

## Overview
This repository contains the documentation and resources for an IoT-based system designed for livestock animal tracking and health monitoring. The system utilizes sensors to monitor vital health parameters such as body temperature and heart rate, along with GPS for real-time location tracking. Data is transmitted wirelessly and displayed on an OLED screen, with remote access via the Blynk platform.

The project is based on a conference paper presented at an IEEE conference, focusing on precision livestock farming to enhance animal welfare and farm productivity.

## Abstract
Efficient livestock control is essential to modern farming, ensuring both animal welfare and productivity. An IoT-based system that uses DS18B20 and MAX30100 sensors to continuously monitor livestock's vital health parameters, such as body temperature and heart rate, is suggested as a solution to this problem. GPS is also incorporated into the system to track locations in real-time. Data gathered by Arduino Nano-based transmitters is wirelessly sent to an ESP32 receiver via nRF24L01 modules. The receiver shows the data on an OLED screen and then uses the Blynk platform to send it to a mobile dashboard. According to experimental results, the system enables the accurate identification of abnormal health conditions and the effective real-time monitoring of livestock across large farm environments. This method facilitates the early detection of health anomalies and enhances farm management by offering a scalable and affordable precision livestock farming solution.

## System Components
### Transmitter Module
- Arduino Nano (main controller)
- DS18B20 (temperature sensor)
- MAX30100 (heart rate and SpO₂ sensor)
- GPS Module (for location tracking)
- nRF24L01 (wireless transceiver)
- Rechargeable battery or solar panel for power

### Receiver Module
- ESP32 (microcontroller for data processing and Wi-Fi connectivity)
- OLED Display (SSD1306 for local data visualization)
- nRF24L01 (wireless transceiver)

### Software
- Developed using Arduino IDE
- Libraries: RF24, TinyGPS++, MAX30100, Adafruit_SSD1306
- Communication Protocols: SPI for nRF24L01, Wi-Fi for Blynk integration

## Features
- Real-time monitoring of body temperature, heart rate, and SpO₂
- GPS-based location tracking
- Wireless data transmission using nRF24L01
- Local display on OLED screen
- Remote monitoring via Blynk mobile app and web dashboard
- Alerts for abnormal health conditions

## How to Set Up
1. Assemble the transmitter module with the sensors and attach it to the livestock (e.g., as a collar).
2. Set up the receiver module with ESP32 and OLED display.
3. Upload the Arduino code to both transmitter (Arduino Nano) and receiver (ESP32).
4. Configure Wi-Fi credentials and Blynk authentication token in the receiver code.
5. Power the devices and monitor data via OLED, serial monitor, or Blynk app.

## Results
The system accurately detects deviations in health parameters, with normal ranges programmed for various animals (e.g., cows: 38.6–39.5°C, 48–84 bpm). Experimental tests showed reliable data transmission and alerts for anomalies like elevated temperature or heart rate.

## Future Enhancements
- Integration with GSM for SMS alerts
- Solar-powered operation for off-grid use
- Machine learning for predictive health analysis
- Accelerometer for behavior monitoring