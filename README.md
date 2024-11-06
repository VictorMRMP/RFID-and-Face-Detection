# Raspberry Pi Security System with RFID and Camera Integration

## Project Members
- **Victor Marcelo Riverete Monteiro Padial** - 12547444
- **João Vitor Abreu e Oliveira** - 12624287

## Overview

This project implements a basic security system using a Raspberry Pi, integrating an RFID module (RC522) and a camera for facial recognition. The system controls access by reading RFID tags and identifying authorized faces. 

## Components

- **Raspberry Pi**
- **RFID-RC522 Module**
- **LEDs (Green and Red)**
- **Camera Module**

## RFID System

The RFID system is configured with the Raspberry Pi using the RFID-RC522 module. The SPI communication protocol was activated, and the RFID module's Python library was used to read and register the IDs of RFID tags.

- **Configuration**: 
  - The RFID module reads tag IDs, which are saved in the code for later comparison.
  - When a tag is presented to the reader, the system checks if the ID matches a pre-registered ID.
  
- **Access Control**: 
  - If the presented ID matches the registered ID, the green LED lights up, indicating access granted.
  - If the ID does not match, the red LED lights up, indicating access denied.

## Camera System

A camera module was integrated with the Raspberry Pi for facial detection using `libcamera-hello`. Facial detection was implemented using Haar Cascade with Python libraries OpenCV and PiCamera2.

- **Detection Setup**:
  - The system detects faces in real-time and displays them in a detection window.
  - The NUSP (student ID number) of the team members is displayed within the detection window.

## Additional Contributions

This project was completed with assistance from Giovane, who contributed to the NUSP display feature within the facial detection window.

---

## How to Run the Project

1. **RFID Setup**:
   - Connect the RFID-RC522 module to the Raspberry Pi and enable SPI communication.
   - Install the necessary Python libraries for RFID functionality.
   - Run the Python script to register a tag ID.

2. **Camera Setup**:
   - Connect the camera to the Raspberry Pi.
   - Use `libcamera-hello` to ensure the camera is correctly connected.
   - Run the facial detection script with OpenCV and PiCamera2 libraries installed.

## License

This project is licensed under the MIT License.

