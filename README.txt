# STM32 G474 + HSS86 + NEMA 34 Stepper Motor Control
-By SIRANJEEVI A
## Overview

This project demonstrates precise stepper motor control using the **STM32 Nucleo-G474RE**, **HSS86 stepper driver**, and **NEMA 34 stepper motor**. The system integrates a **Raspberry Pi 4B** with a **10-inch display** for user interface and command transmission, while a **75V battery supply** powers the system via appropriate DC-DC step-down converters.

The project was developed and tested at **Jedlik** for learning and practical implementation of advanced motor control and embedded system integration.

## System Architecture

![System Block Diagram](attach your diagram image here or use the one above)

**Main components:**
- **Display (10 inch):** User interface for selecting motor commands.
- **Raspberry Pi 4B:** Receives user commands and communicates with STM32.
- **STM32 Nucleo-G474RE:** Generates control signals for the HSS86 driver.
- **HSS86 Stepper Driver:** Drives the NEMA 34 stepper motor with high precision.
- **NEMA 34 Stepper Motor:** Executes the movements commanded via the system.
- **75V Battery with step-down converters:** Powers Raspberry Pi, STM32, and the driver reliably.

## Features

✅ Smooth and precise control of a high-torque NEMA 34 stepper motor.  
✅ Raspberry Pi-based UI for easy motor direction and speed selection.  
✅ Integration of a 75V battery system with step-down for embedded control.  
✅ Uses STM32 advanced timers for accurate pulse and direction generation.  
✅ Modular and scalable for robotic and mechatronic applications.

## Applications

- Electric vehicle steering actuation (steer-by-wire test benches).
- Robotics and automation requiring high-torque stepper control.
- Research on motor control and embedded system integration.
- Educational lab projects for embedded motor control.

## Repository Structure

```
/src
  ├── stm32_motor_control/         # STM32 firmware for motor pulse generation
  ├── raspberry_pi_ui/             # Python scripts for GUI and command sending
  ├── hardware_schematics/         # Block diagrams and wiring schematics
/docs                               # Technical documentation and setup guide
README.md
```

## Getting Started

1. **Hardware Connections:**
   - Connect the STM32 pulse and direction pins to the HSS86 driver.
   - Connect the NEMA 34 stepper motor to the HSS86 output.
   - Connect the Raspberry Pi to the STM32 via UART or GPIO for command transmission.
   - Power the system using a 75V battery with appropriate step-down converters for Raspberry Pi and STM32.

2. **Flashing STM32:**
   - Clone this repository:
     ```
     git clone https://github.com/yourusername/yourprojectname.git
     ```
   - Open `stm32_motor_control` in STM32CubeIDE.
   - Compile and flash the firmware to the Nucleo-G474RE.

3. **Running the UI:**
   - Navigate to `raspberry_pi_ui` on your Pi.
   - Run the GUI:
     ```
     python3 main.py
     ```
   - Select your desired motor direction and speed.

4. **Observing Motor Response:**
   - The NEMA 34 stepper will rotate according to the selected direction and speed on your display.

## Future Improvements

- Add feedback using an encoder for closed-loop position control.
- Implement advanced trajectory generation on STM32.
- Integrate ROS for high-level robotic applications.

## License

This project is open-source under the MIT License.

## Acknowledgments

Developed and tested at **Jedlik** for advanced embedded system training and project development.
