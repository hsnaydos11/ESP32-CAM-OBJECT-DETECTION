# ESP-32 CAM Object Detection with MobileNet

This project aims to classify images uploaded by users automatically using TensorFlow.js and the MobileNet model. The technology allows computers and smart devices to recognize and understand visual data, offering significant advantages across various sectors.

## Table of Contents
- [Introduction](#introduction)
- [Project Description and Purpose](#project-description-and-purpose)
- [Materials and Requirements](#materials-and-requirements)
- [Circuit Design and Schematic](#circuit-design-and-schematic)
- [Code](#code)
- [Usage](#usage)
- [Conclusion](#conclusion)

## Introduction
The objective of this project is to create a web application that classifies images uploaded by users using TensorFlow.js and the MobileNet model. This model is optimized for mobile devices and embedded systems, enabling high accuracy in image classification even with limited hardware resources. 

## Project Description and Purpose
This project is a web application that uses TensorFlow.js and the MobileNet model to automatically classify images uploaded by users. The primary goals are:
1. **User-Friendly Interface:** Create a simple and intuitive interface for users to upload images and view results.
2. **High Accuracy:** Ensure the accurate classification of uploaded images using the MobileNet model.
3. **Fast and Efficient Processing:** Provide quick processing of images and immediate results to users.
4. **Wide Application Range:** Demonstrate the applicability of image classification technology in various fields such as healthcare, security, e-commerce, and social media.

## Materials and Requirements
### Hardware:
- ESP32-CAM
- FTDI Programmer
- Breadboard
- Cables
- Type-mini-B Cable
- Computer
- Memory Card (4-8 GB)

### Software:
- Arduino IDE
- TensorFlow.js
- MobileNet Model

## Circuit Design and Schematic
To upload codes to the ESP32-CAM module, it must be correctly connected to the FTDI programmer. The connections are as follows:
- ESP32-CAM GND -> FTDI PROGRAMMER GND
- ESP32-CAM 5V -> FTDI PROGRAMMER VCC
- ESP32-CAM UOT -> FTDI PROGRAMMER RX
- ESP32-CAM UOR -> FTDI PROGRAMMER TX

> Note: The model must be connected at 5.5V. If connected at 3.3V, the system will not work due to insufficient current for the camera or WiFi.

## Code
### Arduino IDE Setup
1. Open Arduino IDE.
2. Select the appropriate board and port (`Al Thinker ESP-32 CAM`).
3. Load the `cameraWebServer` example from `File > Examples > ESP32 > Camera`.
4. Update the WiFi SSID and password in the code:
    ```cpp
    const char *ssid = "your_ssid";
    const char *password = "your_password";
    ```
5. Ensure the correct camera model is selected:
    ```cpp
    #define CAMERA_MODEL_AI_THINKER
    ```

### HTML Page
The `camera_index.h` file contains the hex representation of an HTML page. Design your HTML using VS Code, convert it to hex, and update the file accordingly.

## Usage
1. Upload the code to the ESP32-CAM.
2. Connect to the WiFi network specified in the code.
3. Access the camera stream via the IP address displayed in the Serial Monitor.

## Conclusion
This project demonstrates the use of TensorFlow.js and the MobileNet model to classify images on an ESP32-CAM. The system is designed to be user-friendly, accurate, and efficient, showcasing the broad applicability of image classification technologies.

## Author
**Hasan Aydos**
- Recep Tayyip Erdogan University, Faculty of Engineering and Architecture, Computer Engineering Department
- Academic Year: 2023-2024


