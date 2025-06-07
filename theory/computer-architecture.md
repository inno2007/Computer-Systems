# Computer Architecture, Hardware & Memory

This file summarizes the essential components of computer architecture based on UTS coursework. It explains how computers are structured, how they process data, and how memory is organized.

---

## The CPU: Central Processing Unit

The CPU is the heart of a computer. It processes all instructions and consists of:

- **Registers**: Small, fast memory within the CPU. Temporarily store data and instructions.
- **Control Unit (CU)**: Decodes instructions and controls the flow of data between registers, RAM, and ALU.
- **Arithmetic Logic Unit (ALU)**: Performs arithmetic (add, subtract, etc.) and logic (AND, OR, NOT) operations.

---

## Types of Memory

### 1. Registers  
- Located inside the CPU  
- Fastest but lowest capacity  
- Temporarily stores values during computation

### 2. RAM (Random Access Memory)  
- Volatile memory: loses content when power is off  
- Stores running programs and active data

### 3. ROM (Read-Only Memory)  
- Non-volatile: stores firmware (startup instructions)  
- Cannot be modified by the user during runtime

### Comparison:
| Memory Type | Volatile? | Speed     | Editable | Location    |
|-------------|-----------|-----------|----------|-------------|
| Register     | No        | Fastest   | Yes      | Inside CPU  |
| RAM          | Yes       | Fast      | Yes      | Motherboard |
| ROM          | No        | Medium    | No       | Motherboard |

---

## Binary & Software

All digital computers operate using **binary code** (1s and 0s).

### ASCII:
- Each character (e.g., "A", "1", "!") is encoded as a 7- or 8-bit binary number
- "hello" in ASCII binary:  
  `1101000, 1100101, 1101100, 1101100, 1101111`

---

## Secondary Storage

Used for long-term storage of data and programs. It is **non-volatile**.

### 3 Common Types:

| Storage Type   | Description                              | Examples              |
|----------------|------------------------------------------|------------------------|
| Magnetic Disk  | Stores data using magnetized patterns    | HDD, backup tapes     |
| Optical Disk   | Burned with lasers                       | CD, DVD, BluRay       |
| SSD (Solid-State)| Uses flash memory, no moving parts      | SSDs, USB drives      |

---

## Comparison of Storage Technologies

| Type     | Speed    | Cost   | Durability | Portability |
|----------|----------|--------|------------|-------------|
| HDD      | Medium   | Low    | Low        | Low         |
| SSD      | Fast     | High   | High       | Medium      |
| Optical  | Slow     | Cheap  | Medium     | High        |

---

## Software Overview

Software is a set of instructions that tell the hardware what to do. There are two types:

### 1. System Software
- Controls hardware and provides a platform for applications
- Examples: Windows, Linux, macOS, Java JDK

### 2. Application Software
- Designed for end users to perform tasks
- Examples: MS Word, Google Chrome, Zoom

---

## Summary

- The **CPU** processes all tasks using registers, control units, and ALUs.
- **RAM** is fast but volatile, while **ROM** is permanent and stores firmware.
- Storage types vary in speed, cost, and reliability.
- **System software** runs the machine, **application software** helps users perform tasks.
