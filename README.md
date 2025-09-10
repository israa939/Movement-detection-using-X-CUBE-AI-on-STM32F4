# Motion Detection Using X-Cube-AI on STM32F4

This project implements **motion detection** on the STM32F4 microcontroller using **X-Cube-AI** and an **MMA7600 accelerometer**. The system can detect three types of movements:

- **Up/Down movement**  
- **Rotation**  
- **Rest (no movement)**  

---

## Project Overview

The project leverages **machine learning inference** directly on the STM32F4 using X-Cube-AI. The accelerometer provides real-time motion data, which is processed to classify the current motion type.

---

## Dataset

- The dataset is provided in **`.h5` format**.  
- You must **download the dataset file** and use it to train or test the AI model before running the project.  

---

## Setup Instructions

1. **STM32CubeIDE Configuration**  
   - Open your project in **STM32CubeIDE**.  
   - Go to **Middleware > Software Packs**, and download **X-Cube-AI v6**.  

2. **Import the AI Model**  
   - Import your trained `.h5` model from your PC into the project using **X-Cube-AI** integration.  

3. **Build and Run**  
   - Compile and flash the project to your **STM32F4**.  
   - Open **Hercules UART Terminal** to monitor the output.  

4. **Testing Motion Detection**  
   - Move the accelerometer in different ways. Depending on the motion, one of the following messages will appear in the UART terminal:
     - **Rotation** → "ROTATION DETECTED"  
     - **Up/Down movement** → "UPDOWN DETECTED"  
     - **No movement** → "IDLE DETECTED"  
     - **Unrecognized motion** → "UNRECOGNIZED !!!"  

---

## Hardware Required

- **STM32F4 Discovery Board**  
- **MMA7600 Accelerometer**  
- **UART connection** for monitoring (e.g., Hercules terminal)

---

## Software Required

- **STM32CubeIDE**  
- **X-Cube-AI software pack**  
- **Hercules UART Terminal**  

---

## Notes

- Ensure the accelerometer is properly connected to the STM32 board.  
- Make sure your AI model is trained correctly on the `.h5` dataset.  
- The system classifies motion **in real-time** based on accelerometer readings.  
