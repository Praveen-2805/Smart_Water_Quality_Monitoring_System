# Smart Water Monitoring System

The Smart Water Monitoring System is a project that utilizes an ESP32 controller to monitor the real-time values of pH, turbidity, temperature, and humidity of water. The system displays these measurements on an LCD screen and sends the data to the ThingSpeak IoT platform for further analysis and visualization.

## Table of Contents
1. [Introduction](#introduction)
2. [Hardware Requirements](#hardware-requirements)
3. [Software Requirements](#software-requirements)
4. [Circuit Diagram](#circuit-diagram)
5. [Installation](#installation)
6. [Usage](#usage)
7. [Contributing](#contributing)

## Introduction

The Smart Water Monitoring System provides a reliable and efficient solution for monitoring essential parameters of water quality. By utilizing the ESP32 controller, this project enables real-time data acquisition, display, and remote monitoring of pH, turbidity, temperature, and humidity values. The collected data is transmitted to the ThingSpeak platform, allowing users to analyze and visualize the information conveniently.

## Hardware Requirements

To build the Smart Water Monitoring System, you will need the following components:

- ESP32 development board
- pH sensor
- Turbidity sensor
- DHT11 temperature and humidity sensor
- 16x2 LCD display
- Breadboard or perfboard
- Resistors (220Ω and 10kΩ)
- Jumper wires

## Software Requirements

The following software tools are required for setting up the project:

- Arduino IDE (Integrated Development Environment)
- ESP32 board support package for Arduino IDE
- ThingSpeak account (for data visualization and analysis)
- DHT library for Arduino
- LiquidCrystal library for Arduino
- [Optional] Git (for version control)

## Circuit Diagram

Insert a detailed circuit diagram illustrating the connections between the components. Clearly indicate the pin assignments for the ESP32 board, pH sensor, turbidity sensor, DHT11 sensor, and LCD display. You may use software like Fritzing or draw the circuit diagram manually.

## Installation

1. Connect the components according to the circuit diagram.
2. Install the Arduino IDE by following the official instructions for your operating system.
3. Install the ESP32 board support package in the Arduino IDE:
   - Open the Arduino IDE.
   - Navigate to **File > Preferences**.
   - In the "Additional Boards Manager URLs" field, enter the following URL:
     ```
     https://dl.espressif.com/dl/package_esp32_index.json
     ```
   - Click the "OK" button to save the preferences.
   - Navigate to **Tools > Board > Boards Manager**.
   - Search for "esp32" and click on the board package from Espressif Systems.
   - Click the "Install" button to install the package.
4. Install the required libraries in the Arduino IDE:
   - Navigate to **Sketch > Include Library > Manage Libraries**.
   - Search for "DHT" and install the DHT library.
   - Search for "LiquidCrystal" and install the LiquidCrystal library.

## Usage

1. Open the Arduino IDE and navigate to the project folder.
2. Open the `Water_Monitoring_System.ino` file.
3. Set up your ThingSpeak account and obtain the necessary API keys.
4. Replace the placeholders in the code with your Wi-Fi credentials and ThingSpeak API keys.
5. Verify and upload the sketch to the
