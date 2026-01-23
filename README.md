#  An 8-bit Breadboard Computer-Project

A fully functional 8-bit breadboard computer built using discrete TTL logic, inspired by Ben Eater’s series, demonstrating the fundamentals of computer architecture and digital system design.

---

## 📌 Overview

This project presents a working 8-bit CPU that can run basic programs using a self-designed instruction set.
All functional units, including registers, ALU, control circuitry, and memory, are implemented using 74xx series TTL logic ICs, without relying on any microcontroller or programmable device.

🎯 Objectives

The main purpose of this project is to develop practical understanding of:

- Hardware-level operation of a computer system  
- Movement of data and execution control inside a CPU  
- Timing behavior of clock-driven digital circuits  
- Instruction processing and micro-level control actions  
- Communication between modules using a shared data bus  

---

## 🧠 System Architecture

The computer follows a **bus-based architecture** where all modules communicate using a shared 8-bit data bus.

###  Major Modules

- **Clock Module**  
  Provides adjustable clock pulses for manual (step-by-step) and automatic execution.

- **Bus System**  
  Shared 8-bit data bus connecting all modules with LED indicators for visualization.

- **Registers**
  - A Register
  - B Register
  - Instruction Register (IR)
  - Output Register

- **Arithmetic Logic Unit (ALU)**  
  Performs 8-bit addition and subtraction and generates Carry and Zero flags.

- **Program Counter (PC)**  
  Tracks the address of the next instruction.

- **Memory Address Register (MAR)**  
  Stores memory address for RAM access.

- **RAM Module**  
  Stores program instructions and data.

- **Control Unit**  
  Generates control signals using combinational logic and microcode stored in EEPROM.

---

## 🧩 Complete Parts List

### Integrated Circuits 

- 74LS173 – 4-bit registers  
- 74LS161 – Counters (PC)  
- 74LS245 – Bus transceivers  
- 74LS08 – AND gates  
- 74LS32 – OR gates  
- 74LS04 – NOT gates  
- 74LS138 – Instruction decoder  
- AT28C256 – EEPROM for microcode  
- RAM IC (e.g., 6116 or equivalent)  

### Other Components

- Breadboards (multiple)  
- Jumper wires (solid core)  
- LEDs for bus and registers  
- Resistors (220Ω, 330Ω)  
- Capacitors (0.1µF decoupling per IC)  
- Push buttons (clock, reset)  
- Toggle switches  
- 5V regulated power supply  

---

## ✅ Verification and Testing

To ensure correct operation, the system was verified using both **module-level testing** and **system-level testing**.

### 🔍 Module-Level Verification

Each module was tested independently before full system integration:

- ✔ Clock pulses verified using LED and manual stepping  
- ✔ Registers tested by loading and outputting known data values  
- ✔ ALU tested for correct addition and subtraction results  
- ✔ RAM tested for correct read and write operations  
- ✔ Instruction register and decoder verified using opcode observation  

### 🧪 System-Level Verification

After integration, full programs were executed using step-by-step clock pulses:

- Load and Output instruction test  
- Addition program execution  
- Jump instruction verification  
- Conditional branching using Zero and Carry flags  

LED indicators were used to monitor:
- Bus values  
- Register contents  
- Instruction execution steps  

Correct execution of micro-operations confirmed proper control signal timing and data flow.

---

## 📚 References

- Ben Eater — *Build an 8-bit computer from scratch*  
  https://eater.net/8bit  

- Digital Logic Design and Computer Architecture textbooks  

- Texas Instruments 74LS Series TTL Datasheets  

- AT28C256 EEPROM Datasheet  

---

## Acknowledgment

This project was inspired by Ben Eater’s educational series, which provides an excellent hands-on approach to understanding how computers work at the hardware level.
