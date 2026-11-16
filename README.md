# The-CNC-system-utilizes-a-Mitsubishi-Q-series-PLC-MR-J3-servos-and-image-processing.
# Mitsubishi Q-Series CNC Vision Control

A PLC-based CNC machine control system integrating **Mitsubishi MELSEC-Q PLC**, **MELSERVO MR-J3 servo drives**, and **computer vision** for automated positioning and machine operation.

## Overview

This project focuses on developing a CNC machine control system using Mitsubishi industrial automation hardware combined with an image-processing system.

The PLC handles machine control and motion coordination, while the servo drives provide precise positioning for the machine axes. The vision system processes image data to support visual inspection and positioning tasks.

## System Architecture

```text
       Camera / Vision System
                |
                v
       Image Processing
                |
                v
         Position Data
                |
                v
       Mitsubishi Q PLC
                |
         Motion Control
                |
          MR-J3 Servo
                |
                v
          CNC Machine
```

## Hardware

| Component | Description |
|---|---|
| PLC | Mitsubishi MELSEC-Q Series |
| Servo Amplifier | Mitsubishi MELSERVO MR-J3 |
| Motion System | Servo-driven linear axes |
| Vision System | Camera-based image processing |
| Mechanical System | CNC linear motion mechanism |

## Motion Control

The system uses servo-driven linear axes for CNC positioning.

### Axis Configuration

| Axis | Screw Lead | Positioning Unit |
|---|---:|---|
| Axis 1 | 20 mm/rev | mm |
| Axis 2 | 10 mm/rev | mm |

Motion control functions include:

- Absolute positioning
- Relative positioning
- Jog operation
- Homing and origin return
- CW/CCW pulse output
- Start/Stop control
- Servo status and error monitoring

Position commands are handled by the PLC and converted into motion commands for the servo system.

## Computer Vision

The image-processing subsystem is designed to support machine positioning and visual processing tasks.

Main processing workflow:

1. Acquire images from the camera.
2. Process image data.
3. Extract relevant visual information.
4. Determine the required position data.
5. Transfer position information to the PLC for machine operation.

**Vision algorithm:** To be documented.

**Camera model:** To be documented.

## PLC Programming

PLC programming is developed using Mitsubishi GX Works2.

Main control functions:

- Machine sequence control
- Servo positioning management
- Homing sequence
- Manual and automatic operation
- Motion status monitoring
- Alarm and error handling
- Communication with the vision system

## Software & Development Tools

- Mitsubishi GX Works2
- Mitsubishi PLC programming environment
- Camera image-processing software
- PC-based vision processing

## Repository Structure

```text
Mitsubishi-Q-CNC-Vision-Control/
│
├── PLC/
│   ├── Program/
│   ├── Motion_Control/
│   └── Sequence_Control/
│
├── Vision/
│   ├── Image_Processing/
│   ├── Camera_Calibration/
│   └── Position_Detection/
│
├── Documentation/
│   ├── System_Architecture/
│   ├── Electrical_Diagrams/
│   └── Motion_Configuration/
│
├── Images/
│
└── README.md
```

## Project Objectives

- Develop a PLC-based CNC control system.
- Implement servo-based positioning and motion control.
- Integrate computer vision into the machine control workflow.
- Improve positioning accuracy and automation capabilities.
- Build practical experience with industrial automation hardware and software.

## Safety Notice

This project involves industrial motion-control equipment and servo drives.

Always verify electrical wiring, grounding, emergency-stop circuits, servo parameters, and motion limits before operating the machine.

## Project Status

**Development in progress.**

More implementation details, system diagrams, control logic, and experimental results will be added as the project develops.

## Author

Developed as an industrial automation and CNC control engineering project.
