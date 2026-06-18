# PIC18F4580 DC Motor Control Using L293D and LCD

## 💡 Project Description

This project demonstrates controlling two DC motors using a PIC18F4580 microcontroller and an L293D motor driver IC. A 16x2 LCD display is used to indicate the current motor operation status. The motors can rotate in either forward or reverse direction based on button inputs connected to PORTB.

This project is useful for learning DC motor interfacing, LCD communication, and embedded system control using PIC microcontrollers.

---

## 🛠️ Hardware Components

* PIC18F4580 Microcontroller
* L293D Motor Driver IC
* 2 × DC Motors
* 16x2 LCD Display (LM016L or equivalent)
* 2 × Push Buttons
* 5V Power Supply
* Breadboard and Connecting Wires

---

## ⚙️ Circuit Connections

### L293D Motor Driver

| L293D Pin | PIC18F4580 Pin | Description     |
| --------- | -------------- | --------------- |
| IN1       | RD0            | Motor 1 Control |
| IN2       | RD1            | Motor 1 Control |
| IN3       | RD2            | Motor 2 Control |
| IN4       | RD3            | Motor 2 Control |
| EN1       | VCC            | Enable Motor 1  |
| EN2       | VCC            | Enable Motor 2  |

### Motor Connections

| L293D Output | Connection |
| ------------ | ---------- |
| OUT1 & OUT2  | DC Motor 1 |
| OUT3 & OUT4  | DC Motor 2 |

---

## 🗺️ LCD Connections

| LCD Pin | PIC18F4580 Pin      | Description     |
| ------- | ------------------- | --------------- |
| RS      | RA0                 | Register Select |
| RW      | RA1                 | Read / Write    |
| E       | Controlled via Code | Enable          |
| D0-D7   | RC0-RC7             | Data Lines      |

---

## 💻 Software Requirements

* MPLAB X IDE
* XC8 Compiler
* PIC18F4580 Header File (`<pic18.h>`)
* Proteus Design Suite (Optional)

---

## 🚀 Working Principle

The microcontroller continuously monitors two push buttons connected to PORTB.

### Button Functions

| Button | Action                |
| ------ | --------------------- |
| RB0    | Motors Rotate Forward |
| RB1    | Motors Rotate Reverse |

### LCD Messages

| Motor State | LCD Display |
| ----------- | ----------- |
| Forward     | FORWARD     |
| Reverse     | REVERSE     |
| Stop        | LCD Cleared |

When a button is pressed:

1. The corresponding motor direction is selected.
2. The motor driver receives control signals through PORTD.
3. The LCD displays the current operating mode.
4. After a delay, the motors stop automatically.

---

## ✨ Features

* Dual DC Motor Control
* LCD Status Display
* Forward and Reverse Rotation
* L293D Motor Driver Interface
* Beginner-Friendly Embedded C Program


## ▶️ Steps to Use

1. Create a new MPLAB X project.
2. Select PIC18F4580 as the target device.
3. Choose XC8 Compiler.
4. Add the source code.
5. Build the project.
6. Generate the HEX file.
7. Program the PIC18F4580.
8. Connect the hardware according to the schematic.
9. Power the circuit.
10. Press the control buttons and observe motor operation and LCD messages.

---

## 🧪 Simulation (Proteus)

### Required Components

* PIC18F4580
* L293D Motor Driver
* 2 DC Motors
* 16x2 LCD
* Push Buttons
* Crystal Oscillator
* Power Supply

### Simulation Procedure

1. Create a new Proteus project.
2. Place all required components.
3. Connect the circuit according to the schematic.
4. Load the generated HEX file into the PIC.
5. Set the clock frequency correctly.
6. Run the simulation.
7. Press RB0 and RB1 buttons to test motor directions.

---

## 🔧 Hardware Implementation

1. Program the PIC using PICkit 3 or PICkit 4.
2. Assemble the circuit on a breadboard or PCB.
3. Connect the motors to the L293D outputs.
4. Power the circuit using a regulated supply.
5. Verify LCD messages and motor rotation directions.

---

## 🛠 Future Enhancements

* PWM-Based Speed Control
* Motor Direction Indicators
* Additional Motion Modes
* Obstacle Detection Sensors
* Bluetooth or Wireless Control
* Menu-Based LCD Interface

---

## 📸 Circuit Diagram
![image alt](https://github.com/manubraj/PIC-Microcontroller-Dual-Motor-Control-with-LCD/blob/6d602f6486cffdbcbf68a82ea574db20558f3499/motorLCD.png)


---

## ⚠️ Notes

* Ensure adequate motor power supply.
* Common ground must be shared between PIC and L293D.
* LCD timing may require adjustment depending on oscillator frequency.
* Motors may draw high current during startup.

---

## 📚 Applications

* Robot Vehicle Control
* Industrial Motor Demonstrations
* Educational Embedded Projects
* Motor Driver Interfacing Experiments
* Automation Systems

---

## 📄 License

This project is intended for educational and learning purposes. Users are free to modify and improve the project for academic and personal use.

---

## 🙏 Acknowledgements

Developed and tested using:

* PIC18F4580 Microcontroller
* MPLAB X IDE
* XC8 Compiler
* L293D Motor Driver IC
* 16x2 LCD Module
* Proteus Design Suite
