# 💊 Medicine Reminder System using LPC2148

This is an embedded system project built on the **LPC2148 ARM7 microcontroller** to act as a programmable medicine reminder system. It uses a Real-Time Clock (RTC), 20x4 LCD, keypad, and buzzer to display time/date, set medicine alarm timings, and alert users.

---

## 🚀 Features

- ⏰ Real-time clock display (HH:MM:SS and DD/MM/YYYY)
- 📆 Editable RTC (time/date) via keypad
- ⏳ Two separate programmable medicine reminders
- 🔔 Buzzer alarm for alerting medicine time
- 🧠 Easy-to-navigate user interface using keypad and LCD

---

## 🛠️ Requirements

### Hardware

- LPC2148 Microcontroller (ARM7TDMI)
- 20x4 Character LCD Display
- 4x4 Matrix Keypad
- 2 Push Button Switches
- Buzzer
- Jumper Wires
- Breadboard or PCB

### Software

- Keil uVision (for coding and compiling)
- Flash Magic (for uploading hex file to LPC2148)
- Proteus (optional for simulation)

---

## 🧰 Pin Connections

| Component | LPC2148 Pin |
|----------|--------------|
| LCD      | PORT1 (as per `lcd.h`) |
| Keypad   | PORT0 (custom mapping in `keypad.h`) |
| Buzzer   | P0.0         |
| Switch 1 (Edit) | P0.22  |
| Switch 2 (Stop) | P0.23  |

> **Note:** RTC is internal to LPC2148; no external RTC IC needed.

---

## 📂 Project Structure

MedicineReminder/
├── lcd.h              // 🖥️ Header file for LCD control functions
├── keypad.h           // ⌨️ Header file for 4x4 matrix keypad interfacing
├── delay.h            // ⏱️ Custom delay utilities for timing operations
├── lcd_defines.h      // 🧾 Macro definitions for LCD command/data settings
├── main.c             // 💡 Core embedded C program for RTC, alarms, and interaction
├── README.md          // 📘 Project documentation and usage guide
└── requirements.txt   // 📦 List of required tools, hardware, and software


---

## 📝 How to Use

1. Power up the LPC2148 board.
2. Use Switch 1 to enter edit mode.
3. Choose between RTC edit or Medicine alarm edit using the keypad.
4. Enter the desired time/date or alarm timings.
5. Buzzer will sound at the alarm time until Switch 2 is pressed.

---

## 📌 Notes

- Ensure RTC oscillator is properly configured on LPC2148 board.
- Do not set invalid date/time values; the software handles basic validations.

---

## 🙋‍♂️ Author

- **P.Teja Anand**
- Embedded Systems Developer | Hobbyist | Tech Enthusiast
