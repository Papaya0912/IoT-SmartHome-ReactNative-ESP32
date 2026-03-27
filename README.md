# 🏠 Full-Stack IoT Smart Home System

![React Native](https://img.shields.io/badge/App-React_Native-blue.svg)
![Microcontroller](https://img.shields.io/badge/MCU-ESP32-orange.svg)
![Backend](https://img.shields.io/badge/Backend-Firebase-yellow.svg)
![Language](https://img.shields.io/badge/Language-C++-purple.svg)

## 📌 Overview
A comprehensive Internet of Things (IoT) Smart Home automation system. This project features a custom-built mobile application (React Native) that communicates with an ESP32 microcontroller via Firebase Realtime Database. Users can remotely monitor home conditions (temperature, humidity, rain) and control home appliances (doors, automatic shelters, lights, and fans) in real-time.

## ✨ Key Features
**📱 Mobile Application (React Native):**
* **User Authentication**: Secure Login/Register using Firebase Auth.
* **Real-time Control & Monitoring**: Toggle appliances and read sensor data with near-zero latency.
* **Smart UI/UX**: Includes a dark/light mode toggle and an intuitive dashboard for room management.
* **Activity Logs**: Tracks and displays the history of device interactions.

**⚙️ Hardware Integration (ESP32):**
* **Climate Monitoring**: Reads real-time temperature and humidity via the DHT11 sensor.
* **Weather Automation**: Detects rain and can automatically trigger the shelter servo mechanism.
* **Access Control**: Actuates servo motors to simulate main door locking/unlocking.
* **Bi-directional Sync**: Constantly listens to Firebase streams to update hardware states based on app inputs.

## 🛠️ Tech Stack
* **Frontend**: React Native, TypeScript/JavaScript
* **Backend**: Firebase (Authentication, Realtime Database)
* **Hardware/Firmware**: ESP32, C++ (Arduino Framework), `FirebaseESP32` library.

## 🔌 Hardware Pin Mapping (ESP32)

| Component | ESP32 Pin | Function |
| :--- | :--- | :--- |
| **DHT11** | `GPIO 21` | Temperature & Humidity Sensor |
| **Rain Sensor** | `GPIO 36` | Digital input (LOW = Rain detected) |
| **Shelter Servo** | `GPIO 14` | Controls the automated roof/shelter |
| **Door Servo** | `GPIO 27` | Controls the main door lock |

## 🚀 Getting Started

### Prerequisites
1. Node.js & React Native Environment set up.
2. Arduino IDE or PlatformIO for flashing the ESP32.
3. A Firebase Project with Realtime Database and Authentication enabled.

### Setup Instructions
1. **Clone the repo:**
2. Mobile App: Navigate to /MobileApp, run npm install, and configure your Firebase credentials. Run npx react-native run-android or run-ios.
3. Firmware: Open /Firmware in Arduino IDE, update your WiFi credentials (WIFI_SSID, WIFI_PASSWORD) and Firebase config (API_KEY, DATABASE_URL), then flash it to the ESP32.
