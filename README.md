# Hand Gesture Based Vaccum Cleaner

This project demonstrates how to build an Arduino-based gesture-controlled car using the **HC-05 Bluetooth module** and **MPU-6050 sensor**. The car is controlled wirelessly by hand gestures without requiring a smartphone app. The MPU-6050 sensor detects motion and orientation from the hand, and the data is transmitted via Bluetooth to the car, allowing it to move forward, backward, left, or right.


![Image](https://github.com/user-attachments/assets/b38d2305-1957-43cc-92c8-3e87431d5a41)


## 📦 Components Required

### Hardware
- **Arduino UNO and nano** – One for gesture control, one for car control
- **HC-05 Bluetooth Module (2 units)** – For wireless communication
- **MPU-6050** – Motion sensor to detect gestures
- **L298N Motor Driver** – To control motor direction and speed
- **DC Motors (4 units)** – For driving the wheels
- **Wheels (4 units)** – For movement
- **Battery Pack** – Power supply
- **Jumper Wires** – For connections
- **Chassis** – Base for mounting components

### Software
- **Arduino IDE** – For programming the Arduino boards

## ⚙ System Description

The system is composed of two units:

1. **Gesture Control Unit (Transmitter)**
   - Mounted on the hand or wrist
   - Reads orientation and motion data from the MPU-6050
   - Sends movement commands wirelessly via the HC-05 Bluetooth module

2. **Car Control Unit (Receiver)**
   - Mounted on the robot car chassis
   - Receives gesture commands from the HC-05 module
   - Controls the DC motors via the L298N motor driver accordingly

## 🔌 Wiring Overview

### Gesture Control Unit
- MPU-6050 connected to Arduino using I2C
- HC-05 module connected to Arduino’s RX/TX pins
- Power supply connected to Arduino

### Car Control Unit
- L298N motor driver connected to Arduino and DC motors
- HC-05 connected to Arduino’s RX/TX pins
- Power supply connected to Arduino and motors


## 📋 Working Principle

1. The MPU-6050 detects hand gestures such as tilting forward, backward, left, or right.
2. These gestures are processed by the Arduino and encoded into movement commands.
3. The commands are transmitted through the HC-05 Bluetooth module to the car.
4. The car’s Arduino receives the commands and actuates the motors to move in the desired direction.

## 🚀 How to Run

1. Upload the **gesture detection code** to the Arduino connected with the MPU-6050.
2. Upload the **motor control code** to the Arduino on the car.
3. Pair the two HC-05 modules as master and slave.
4. Power both units.
5. Perform gestures with your hand to control the car’s movement in real-time.

