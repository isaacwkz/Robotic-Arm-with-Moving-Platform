# A Robot With Arms

# Work in Progress!

## Design Goal
Design a robot on an omnidirectional moving platform and a minimum of 6 DOF robotic arm.

## Parts
MCUs: STM32F373, ESP32

STM32 will be running real time movements and computations while ESP32 runs external communications
Communications will be done over UART

Sensor: MPU6050 I2C, SRF02 I2C sonar
(To consider, 3D vision)

Main motor drivers: DRV8843S (10A peak)

Motors: LX-224 (20kg), LX-16A (17kg)
Servos are controlled from half-duplex UART

## Current Status
- A PCB has been sent for fabrication.
- A rough sketch of the robotic arm (minus the gripper) has been completed and 3D printed.
	- Improve on current arm design, add second servo to lower joints for higher carrying capacity.
