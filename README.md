📷 ESP8266 Web Camera System (ArduCAM + Motion Detection)

📌 Overview
This project is a lightweight and modular web-connected camera system built around the ESP8266. It uses an ArduCAM module to capture images and provides a web-based interface for live viewing. Optionally, it supports motion detection using a PIR sensor and can upload captured frames to a remote server for archiving.

It serves as a flexible foundation for more advanced IoT surveillance and smart monitoring systems.

🚀 Key Features
📡 ESP8266-based wireless camera system
📷 Live web interface for real-time image viewing
🧠 Compatible with ArduCAM (2MP / 5MP modules)
🚶 Optional motion detection using HC-SR501 sensor
☁️ Frame upload to remote server on motion trigger
🔁 Configurable WiFi mode (Access Point or client mode)
🗂️ Server-side storage and frame archiving system
🌐 Web viewer for browsing recorded images
🧰 Hardware Requirements
ESP8266 (Wemos D1 Mini or equivalent)
ArduCAM Mini 2MP (5MP optional)
HC-SR501 PIR Motion Sensor (optional)
3.3V / 5V power supply depending on module
🔌 Wiring Overview
📷 ArduCAM → ESP8266
CS → D3
MOSI → D7
MISO → D6
SCK → D5
GND → GND
VCC → 3.3V
SDA → D2
SCL → D1
🚶 Motion Sensor (HC-SR501)
VCC → 5V
GND → GND
OUT → D0
💻 Software Structure
📁 ESP8266 Firmware
Connects to WiFi or creates Access Point
Streams camera frames via web server
Detects motion and triggers image capture
Sends frames to remote server via TCP socket (netcat-based protocol)
🖥️ Server-Side System
📡 Frame Receiver (Bash + Netcat)
Receives raw image streams from ESP8266
Stores frames locally
Uses ImageMagick (optional) for processing
🌐 Web Viewer (Node.js + Express)
Displays stored images in browser
Basic authentication system
Simple file-based archive browsing
⚠️ Important Notes
Server address is hardcoded in firmware and must be changed before deployment
Current communication uses raw TCP (not HTTP)
System assumes trusted network (no encryption/authentication by default)
Designed as a prototype / experimental IoT framework
💡 Future Improvements
🔐 Secure HTTP/MQTT communication
☁️ Cloud storage integration (AWS / Firebase)
📱 Mobile app monitoring dashboard
🤖 AI-based motion detection filtering
🧠 Multi-device network (camera nodes system)
🔒 User authentication & encrypted uploads
📌 Summary

This project provides a simple yet powerful IoT camera system using ESP8266 and ArduCAM, combining live streaming, motion detection, and server-side image archiving. It is ideal as a base for smart surveillance, home security, or IoT research projects.
