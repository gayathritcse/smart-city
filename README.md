🌆 Automatic Street Light Fault Detection System

### Recognition

This project was recognized as a finalist in the Naan Mudhalvan Niral Thiruvizha-2024 Hackathon, executed with the support of Anna University and facilitated by TNSDC.


### Overview

Street lights are an essential part of our infrastructure, providing us with light at night and making our streets safer. However, street lights can malfunction, which can be a safety hazard. This project aims to address this issue by creating an automatic street light fault detection system.

### Project Description

The Automatic Street Light Fault Detection System uses a combination of hardware and software to ensure efficient street light management, proactive fault detection, and user convenience in urban environments.

### Key Components

- ESP8266: Receives data from the Light Dependent Resistor to determine ambient light levels and controls the LED street light accordingly.
- LDR (Light Dependent Resistor): Serves as a sensor, detecting changes in light intensity to signal whether it is daytime or nighttime. This data is processed by the Arduino.
- Arduino: Processes the data from the LDR and controls the street light based on the detected light levels.
- Blink App: Provides a user-friendly interface for monitoring and controlling the street light system remotely.

### Features

- Automatic Light Control:** The system automatically turns the street lights on or off based on ambient light levels detected by the LDR.
- Fault Detection: Identifies and reports malfunctions in street lights, ensuring timely maintenance and repair.
- Remote Monitoring and Control: Users can monitor and control the street lights remotely through the Blink app.
- User Convenience: The Blink app offers an intuitive interface for easy management of the street light system.

### System Architecture

1. Sensor Module: The LDR detects ambient light levels and sends the data to the Arduino.
2. Control Module: The Arduino processes the data and controls the LED street light based on the ambient light levels.
3. Communication Module: The ESP8266 module transmits data between the Arduino and the Blink app.
4. User Interface: The Blink app provides users with remote monitoring and control capabilities.

## Installation

### Hardware Setup

1. Connect the LDR to the Arduino.
2. Connect the LED street light to the Arduino.
3. Connect the ESP8266 to the Arduino for Wi-Fi communication.

### Software Setup

1. Install the Arduino IDE and upload the code to the Arduino.
2. Set up the Blink app and create a new project for the street light system.

## Usage

1. Power on the system.
2. Use the Blink app to monitor and control the street lights.
3. The system will automatically manage the street lights based on ambient light levels and notify users of any faults.

## Future Enhancements

- Advanced Fault Detection: Implement more sophisticated algorithms for fault detection and diagnosis.
- Energy Management: Incorporate features for optimizing energy usage based on real-time data.
- Expanded Coverage: Extend the system to cover more street lights and integrate with city-wide smart city initiatives.

## Contributing

Contributions are welcome! Please feel free to submit issues, fork the repository, and send pull requests.

---

Thank you for your interest in the Automatic Street Light Fault Detection System. Together, we can create safer and more efficient urban environments.
