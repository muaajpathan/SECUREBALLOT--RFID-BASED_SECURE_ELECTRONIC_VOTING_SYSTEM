# 🎓 Smart Exam Hall Monitoring & Management System

**An embedded system for secure, automated, and real-time examination hall management using LPC2129 ARM7 and Embedded C.**

[![Platform](https://img.shields.io/badge/Platform-LPC2129%20ARM7-blue?style=for-the-badge)](https://www.nxp.com/)
[![Language](https://img.shields.io/badge/Language-Embedded%20C-brightgreen?style=for-the-badge&logo=c)](https://en.wikipedia.org/wiki/Embedded_C)
[![IDE](https://img.shields.io/badge/IDE-Keil%20%C2%B5Vision-orange?style=for-the-badge)](https://www.keil.com/)
![Architecture](https://img.shields.io/badge/Architecture-ARM7-red?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

---

## 📌 Overview

The **Smart Exam Hall Monitoring & Management System** is an embedded system developed using the **LPC2129 ARM7 microcontroller** and **Embedded C**.

The project integrates multiple peripherals and hardware modules to provide a structured solution for examination time management, user interaction, temperature monitoring, and alert generation.

The system provides:

- 🔐 Password-protected access to settings
- 📅 RTC-based date and time management
- ⏰ Programmable examination start time
- ⏳ Programmable examination duration
- 🔢 Remaining-time display using a multiplexed 7-segment display
- ⏸️ Exam pause and resume functionality
- 🌡️ Temperature monitoring using LM35
- 🖥️ LCD-based user interface
- ⌨️ 4×4 matrix keypad for user input
- 💡 LED status indication
- 🔊 Buzzer alert
- ⚡ Timer-based operations
- ⚡ External interrupt-based control

> 💡 **The main objective of this project is to automate important examination hall timing and monitoring functions using an embedded microcontroller-based system.**

---

## ✨ Features

| Feature | Description |
|---|---|
| 🔐 **Password Protection** | Protects access to system settings |
| 📅 **RTC Management** | Maintains and displays real-time date and time |
| ⏰ **Exam Scheduling** | Allows examination start time to be configured |
| ⏳ **Exam Duration** | Allows examination duration to be configured |
| 🔢 **Countdown Display** | Displays remaining examination time using a 7-segment display |
| ⏸️ **Pause / Resume** | Allows examination timing to be paused and resumed |
| 🌡️ **Temperature Monitoring** | Measures temperature using an LM35 sensor through ADC |
| 🖥️ **LCD Interface** | Displays system information and examination status |
| ⌨️ **4×4 Keypad** | Used for password entry and system configuration |
| 💡 **LED Indication** | Provides visual status indication |
| 🔊 **Buzzer Alert** | Provides audible alert indication |
| ⚡ **Interrupt Handling** | Handles important external events |
| ⏱️ **Timer Operation** | Provides periodic timing and display control |

---

## 🏗️ System Architecture

The **LPC2129 ARM7 microcontroller** acts as the central controller of the system.

```text
                         ┌──────────────────────┐
                         │      LPC2129         │
                         │      ARM7 MCU        │
                         └──────────┬───────────┘
                                    │
              ┌─────────────────────┼─────────────────────┐
              │                     │                     │
              ▼                     ▼                     ▼
       ┌────────────┐        ┌────────────┐        ┌────────────┐
       │    LCD     │        │   Keypad   │        │    RTC     │
       │ Interface  │        │    4×4     │        │ Time/Date  │
       └────────────┘        └────────────┘        └────────────┘
              │                     │                     │
              └─────────────────────┼─────────────────────┘
                                    │
              ┌─────────────────────┼─────────────────────┐
              │                     │                     │
              ▼                     ▼                     ▼
       ┌────────────┐        ┌────────────┐        ┌────────────┐
       │ 7-Segment  │        │    LM35    │        │ LEDs /     │
       │ Countdown  │        │ Temperature│        │  Buzzer    │
       └────────────┘        └─────┬──────┘        └────────────┘
                                   │
                                   ▼
                              ┌──────────┐
                              │   ADC    │
                              └──────────┘
