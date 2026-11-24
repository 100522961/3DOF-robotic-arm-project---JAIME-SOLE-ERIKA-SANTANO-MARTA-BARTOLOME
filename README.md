# 3DOF robotic arm project - JAIME SOLE, ERIKA SANTANO, MARTA BARTOLOME:
Project for uc3m of Madrid by students for the class "Robot Control Arquitecture" in Robotics Ingeneering Degree of 4th year.


This repository documents a low-cost robotic arm developed as a final project for "Robot Control Arquitecture". The project combines 3D-printed mechanical parts, DC motors with encoder feedback, a servo-operated gripper, and a joystick-based control system.

The arm is designed to pick up and stack cubes. It is controlled manually by an operator using a three-axis joystick. The project was developed as a practical exercise in mechanical design, electronics, embedded programming, and feedback control.

## Project Overview

The arm has three main degrees of freedom for positioning the end effector. Three DC gear motors drive the base, shoulder, and elbow joints. A separate servo motor operates the gripper so that the arm can grasp and release objects.

The joystick’s X and Y axes control the active pair of motors. Pressing the joystick’s Z control switches the control mode so that X and Y operate the other motors. The exact motor-to-axis assignment is described in the control code.

## Project Overview

The arm has three main degrees of freedom for positioning the end effector. Three DC gear motors drive the base, shoulder, and elbow joints. A separate servo motor operates the gripper so that the arm can grasp and release objects.

The joystick’s X and Y axes control the active pair of motors. Pressing the joystick’s Z control switches the control mode so that X and Y operate the other motors. The exact motor-to-axis assignment is described in the control code.

## Hardware

The main components used in the prototype are:

Arduino Mega 2560 R3 microcontroller board

Three SPG30E DC gear motors with encoders

L298N motor driver modules

SG90 360-degree servo motor for the gripper

Three-axis joystick

12 V DC power supply

3D-printed structural and mechanical parts

The encoders provide relative position feedback for the DC motors. They measure changes in motor position, so the arm’s position is determined from movement rather than from an absolute position reading.

## Mechanical Design

The CAD models were based on parts from the 3DOF-RoboticArm-SPG30E repository. We modified the reference designs in Fusion 360 to suit our motors and assembly requirements. Changes included resizing parts, adapting motor mounts, adding openings for cable routing, and adjusting clearances to improve the fit between components.

The parts used in the assembled arm were 3D printed in PLA. The STL files are available in the 3D Parts branch.

## Control and Software

The control software was written in C using Microchip Studio. The program is organised around a main function that calls smaller functions for the different control and system tasks. The source files are available in the C Code branch.

The DC motors use encoder feedback as part of a closed-loop control system. PID control is used to regulate motor movement. PID tuning and performance evaluation are still in progress; controller gains and test results should be added here once they have been measured and confirmed.

## Repository Contents

The project files are organised across the following branches:

Main — this README and the demonstration video.

3D Parts — STL files for the printed parts.

C Code — the project source code.


## Demonstration Video

The video below shows the robotic arm in operation, including its joystick control and gripper.
