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

Servos: LX-224 (20kg), LX-16A (17kg)

Servos are controlled from half-duplex UART

## Current Status
- A PCB has been sent for fabrication.
	- 06 May edit: PCB did not meet trace width clearance requirement. Current rerouting the board.
	- 13 May edit: PCB design has been changed to seperate motor driver and controller on two different PCBs
- A rough sketch of the robotic arm (minus the gripper) has been completed and 3D printed.
	- Improve on current arm design, add second servo to lower joints for higher carrying capacity.
![CAD Render](https://raw.githubusercontent.com/isaacwkz/Robotic-Arm-with-Moving-Platform/master/Pictures/Mech-2020-05-04.jpg)
- PCB has arrived and assembled - both controller and ESC
	- A minor issue, wrong decoupling capacitor footprint was use. The 0402 footprint used is 0402M and not 0402 imperial
- Next step is to write the drivers for the various peripherals on STM32 before moving on to wireless PC communication via ESP32
