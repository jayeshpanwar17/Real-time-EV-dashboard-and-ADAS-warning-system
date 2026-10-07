# EV ADAS System – Real-Time Electric Vehicle Dashboard

An automotive embedded systems project developed during an **Automotive Embedded Systems Internship**.

The system uses an **STM32F103C8T6 (Blue Pill)** with **PICSimLab** to simulate a real-time Electric Vehicle (EV) controller with basic **Advanced Driver Assistance System (ADAS)** features.

## Features

* Real-time EV parameter monitoring
* Speed, battery SOC, torque, power and range estimation
* Forward collision warning
* Left and right blind-spot detection
* Vehicle state machine
* Fault detection and safe-state handling
* UART-based telemetry
* Python-based real-time dashboard
* Alarm and warning system

## Hardware / Simulation

* STM32F103C8T6 Blue Pill
* 3 × HC-SR04 ultrasonic sensors
* PICSimLab
* Potentiometers for simulated EV inputs
* LEDs and buzzer for alerts

## Software & Technologies

* Embedded C
* STM32 HAL
* STM32CubeIDE
* UART
* DMA / Interrupt-based communication
* Python
* PySerial
* Matplotlib

## System Architecture

The STM32 handles sensor acquisition, EV calculations, ADAS logic, vehicle state management and fault handling. Telemetry is transmitted over UART to a Python dashboard, which displays EV parameters and ADAS alerts in real time.

The system operates with a vehicle state machine consisting of:

`PARKED → READY → DRIVING → REGEN → FAULT`

## ADAS Functions

The system uses three ultrasonic sensors for:

* Front obstacle detection
* Left blind-spot detection
* Right blind-spot detection

The front sensor is used for collision warning based on distance and Time to Collision (TTC), while the side sensors are used for blind-spot detection.

## Communication

UART is used to transmit EV metrics and ADAS alert packets between the STM32 and Python dashboard at **115200 bps**.

## Project Context

This project was developed as part of an **Automotive Embedded Systems Internship** and focused on understanding embedded firmware architecture, real-time processing, sensor interfacing, communication and automotive safety concepts.
