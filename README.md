# Real-Time Vehicle Accident Detection

**ESP32-S3 | TinyML | GPS | SIM800L | MQTT | OpenStreetMap**

An IoT-based vehicle accident detection and emergency notification system using embedded sensors, on-device machine learning, GPS tracking, and a real-time web dashboard.

## Project Overview

Real-Time Vehicle Accident Detection is an embedded IoT project designed to identify potential vehicle accidents using an ESP32-S3 microcontroller and multiple sensors.

The system combines TinyML-based classification with rule-based detection to identify potential accident conditions. When an accident is detected, the system can send SMS notifications to registered emergency contacts through a SIM800L GSM module and publish real-time information to a web dashboard using MQTT.

The dashboard provides vehicle location tracking, accident alerts, GPS coordinates, and nearby hospital locations through OpenStreetMap.

## Key Features

- **Real-Time Accident Detection:** Combines sensor-based rules and TinyML classification.
- **TinyML AI Classification:** On-device TensorFlow Lite Micro model with YES/NO output.
- **GPS Tracking:** Real-time vehicle location monitoring.
- **SMS Emergency Alerts:** Sends accident notifications through SIM800L.
- **MQTT Communication:** Transfers vehicle data and accident alerts.
- **Live Dashboard:** Displays vehicle status, sensor readings, and accident information.
- **OpenStreetMap Integration:** Shows vehicle position, accident location, route history, and nearby hospitals.
- **False Alarm Cancellation:** Allows cancellation through the ESP32-S3 BOOT button.

## Hardware Components

| Component | Purpose |
|---|---|
| ESP32-S3 | Main microcontroller |
| MPU6050 | Acceleration and gyroscope data |
| DS18B20 | Temperature monitoring |
| Vibration Sensor | Vibration detection |
| GPS Module | Vehicle location |
| SIM800L | GSM and SMS communication |

## Software and Technologies

- PlatformIO
- Arduino Framework
- Embedded C/C++
- TensorFlow Lite for Microcontrollers
- Python (model training)
- MQTT
- HTML, CSS, JavaScript
- OpenStreetMap

## System Architecture

1. Sensors collect vehicle motion, vibration, and temperature data.
2. ESP32-S3 processes the sensor readings.
3. TinyML and rule-based logic evaluate potential accident conditions.
4. GPS provides the vehicle's current location.
5. SIM800L sends SMS alerts when enabled.
6. MQTT publishes system data and accident alerts.
7. The web dashboard displays real-time vehicle information and map locations.

## Repository Structure

- `firmware/` – ESP32-S3 firmware source code.
- `tinyml/` – Model training resources and trained model.
- `hardware/` – Circuit diagrams and hardware documentation.
- `dashboard/` – Web-based monitoring dashboard.
- `docs/` – Technical documentation and system architecture.
- `examples/` – Demonstration files and sample data.

## Getting Started

1. Clone this repository.
2. Install Visual Studio Code and PlatformIO.
3. Open the `firmware/` directory.
4. Configure hardware pins and communication settings.
5. Configure Wi-Fi, MQTT, GPS, and emergency contact settings.
6. Build and upload the firmware to the ESP32-S3.
7. Open the dashboard and configure the MQTT connection.

Refer to the documentation in each directory for detailed setup instructions.

## Development and Contributions

This repository contains the publicly released version of the project.

Development, experimentation, and research activities are maintained separately in a private repository. Only reviewed and approved implementations are transferred to this public repository.

Contributions are welcome through GitHub Issues and Pull Requests. Please read the project documentation before submitting changes.

## Safety Disclaimer

This project is an experimental prototype for research and educational purposes. It is not a certified automotive safety system and should not be relied upon as the sole method of accident detection or emergency notification.

## License

See the `LICENSE` file for usage, modification, and distribution permissions.

## Acknowledgements

Developed as an embedded systems, IoT, and TinyML research project.