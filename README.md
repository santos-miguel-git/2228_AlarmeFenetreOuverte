# Window Open Detection System

## Project Report 🇫🇷
You can find the full project report [here](./doc/3_Rendu-final/2228_AlarmeFenetreOuverte_MSS_RapportFinal.pdf).

## Overview
This project is a **window open detection system** designed to monitor the status of windows in a room and send alerts when a window is left open during specific hours. The system is energy efficient and operates autonomously, using solar cells as the primary power source with supercapacitors for energy storage and AAA batteries for backup.

Each window is equipped with a **transmitter** that communicates the window's status to a **receiver** located in each room. The transmitters do not continuously monitor the windows but check their status only at specific times, such as the end of the day. The system is built around the NRF52840 microcontroller, which handles communication via Bluetooth Low Energy (BLE) and controls the Hall-effect sensors used for window detection. The system sends email alerts when a window is detected as open during predefined times.

## Features
- **Autonomous Operation**: Powered by solar cells with supercapacitor energy storage and AAA battery backup.
- **Window Open Detection**: Uses Hall-effect sensors to determine whether a window is open or closed.
- **Transmitter and Receiver Setup**: Each window has a transmitter that sends data to a room-based receiver at specific times.
- **Scheduled Monitoring**: Transmitters check window status only at certain hours (e.g., end of the day).
- **Alerts**: Sends email notifications if a window is open during specific times.
- **Low Power Consumption**: Optimized for energy efficiency, ensuring long-term operation without intervention.
- **BLE Communication**: Allows communication and status updates via Bluetooth Low Energy (BLE).

## Components
- **Microcontroller**: NRF52840 (handles BLE communication and sensor data).
- **Power Supply**: Solar cells, supercapacitors, and two AAA batteries as backup.
- **Communication**: Bluetooth Low Energy (BLE) for transmitting data and alerts.
- **Sensors**: Hall-effect sensors for window state detection (open/closed).

## How It Works
1. Each window is equipped with a transmitter that monitors the window's status using Hall-effect sensors at specific times (e.g., end of the day).
2. The transmitter sends data to a receiver installed in the room.
3. When a window is detected as open during certain hours, the system triggers an email alert.
4. Power is primarily supplied through solar cells, with supercapacitors storing the energy. If the solar power is insufficient, the backup AAA batteries ensure uninterrupted operation.
