# Soldier Health and Position Tracking System

## Overview
The **Soldier Health and Position Tracking System** is an Arduino-based safety system designed to monitor a soldier's location and basic health parameters during field operations. It uses GPS for location tracking, GSM for SMS communication, sensors for temperature and heartbeat-related readings, and an LCD display to show system status.

The system can send the soldier's location and health readings to a predefined mobile number when an emergency button is activated or when a location request message is received.

## Features
- GPS-based location tracking
- Temperature monitoring
- Heartbeat-related reading through a sensor
- Emergency alert through SMS
- Location request using SMS
- Google Maps location link in SMS
- LCD display for status updates
- GSM-based communication with the base station

## Hardware Components
- Arduino board
- GPS module
- GSM module (SIM900 compatible)
- Temperature sensor
- LDR / heartbeat sensor input
- Emergency button or digital trigger
- 16×2 LCD with I2C interface
- Connecting wires
- Power supply

## Software and Libraries
- Arduino IDE
- TinyGPS library
- SoftwareSerial library
- Wire library
- LiquidCrystal_I2C library

## Pin Connections

| Component | Arduino Pin |
|---|---|
| Emergency trigger | Digital Pin 6 |
| GSM Module TX/RX | Pins 7 and 8 |
| GPS Module TX/RX | Pins 9 and 10 |
| Temperature Sensor | Analog Pin A1 |
| LDR / Heartbeat Sensor | Analog Pin A0 |
| LCD Display | I2C |

## Working Principle
1. The Arduino initializes the GPS, GSM, sensors, and LCD.
2. The GPS module receives location coordinates.
3. The temperature sensor provides a temperature-related reading.
4. The LDR/sensor input provides a heartbeat-related reading.
5. The LCD displays the tracking system status.
6. When the emergency trigger is activated, an SMS alert containing the location and sensor readings is sent to the configured phone number.
7. When an SMS containing the keyword **LOCAL** is received, the system responds by sending the location and readings.
8. The location is shared through a Google Maps link.

## SMS Alert
The alert message contains:
- Soldier identification details
- Temperature reading
- Heartbeat-related reading
- GPS coordinates
- Google Maps location link

## Setup
1. Install the Arduino IDE.
2. Install the required Arduino libraries.
3. Connect the GPS, GSM, sensors, LCD, and emergency trigger according to the pin configuration.
4. Update the destination phone number in the Arduino code.
5. Upload the sketch to the Arduino board.
6. Power the system and wait for GPS and GSM connectivity.
7. Test the emergency trigger and SMS location request.

## Project Objective
To provide a simple safety and monitoring system that can help communicate a soldier's location and basic health-related readings during field operations, enabling faster assistance in emergency situations.

## Future Enhancements
- Integration with a real-time monitoring dashboard
- Improved medical-grade heartbeat monitoring
- More accurate sensor calibration
- Battery-level monitoring
- Multiple soldier tracking
- Secure communication and authentication

## Disclaimer
This is an educational prototype. Sensor readings and communication reliability depend on the hardware, calibration, GPS signal, GSM network coverage, and power supply. It is not intended to replace professional military or medical equipment.
