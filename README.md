# Smart Water Quality Monitoring System

The Smart Water Quality Monitoring System is a project that utilizes an ESP32 microcontroller to monitor the real-time values of pH, turbidity, temperature, and humidity of water. The system displays these measurements on an LCD screen and sends the data to the ThingSpeak IoT platform for further analysis and visualization.

## Table of Contents
1. [Introduction](#introduction)
2. [Features](#features)
3. [Hardware Requirements](#hardware-requirements)
4. [Software Requirements](#software-requirements)
5. [Installation](#installation)
6. [Usage](#usage)
7. [Contributing](#contributing)
8. [License](#license)

## Introduction

The Smart Water Quality Monitoring System provides a reliable and efficient solution for monitoring essential parameters of water quality. By utilizing an ESP32 microcontroller, this project enables real-time data acquisition, display, and remote monitoring of pH, turbidity, temperature, and humidity values. The collected data is transmitted to the ThingSpeak platform, allowing users to analyze and visualize the information conveniently.

## Features

- Real-time monitoring of water pH, turbidity, temperature, and humidity.
- LCD display for easy visualization of sensor readings.
- Integration with the ThingSpeak IoT platform for data analysis and visualization.
- Customizable threshold alerts for abnormal water quality conditions.
- Expandable and adaptable for additional sensors or functionality.

## Hardware Requirements

To build the Smart Water Quality Monitoring System, you will need the following components:

- ESP32 development board (e.g., ESP32 NodeMCU)
- pH sensor
- Turbidity sensor
- Temperature and humidity sensor (e.g., DHT11 or DHT22)
- 16x2 LCD display
- Breadboard or perfboard
- Jumper wires
- Power supply

## Software Requirements

The following software tools are required for setting up the project:

- Arduino IDE (Integrated Development Environment)
- LiquidCrystal library for Arduino
- DHT library for Arduino
- ThingSpeak account (for data visualization and analysis)

## Installation

1. Connect the components according to the circuit diagram provided.
2. Install the Arduino IDE by following the official instructions for your operating system.
3. Install the required libraries in the Arduino IDE:
   - Open the Arduino IDE.
   - Navigate to **Sketch > Include Library > Manage Libraries**.
   - Search for "LiquidCrystal" and install the LiquidCrystal library.
   - Search for "DHT" and install the DHT library.
4. Clone or download the project code from the repository.
   - If using Git, run the following command:
     ```
     git clone <repository-url>
     ```
   - Alternatively, download the code as a ZIP file and extract it to a local directory.

## Usage

1. Open the Arduino IDE and navigate to the project folder.
2. Open the `Water_Quality_Monitoring.ino` file.
3. Set up your ThingSpeak account and obtain the necessary API keys.
4. Replace the placeholders in the code with your Wi-Fi credentials and ThingSpeak API keys.
5. Verify and upload the sketch to the ESP32 board.
6. Connect the sensors and LCD display to the appropriate pins on the ESP32 board.
7. Power on the system and observe the LCD display for real-time readings.
8. The data will also be sent to the ThingSpeak platform for further analysis and visualization.

## Contributing

Contributions to this project are welcome! If you find any issues or have ideas for improvements, please submit an issue or a pull request in the project's repository.

## License

The Smart Water Quality Monitoring System is licensed under the [MIT License](https://opensource.org/licenses/MIT). Please refer to the `LICENSE` file for more information.
