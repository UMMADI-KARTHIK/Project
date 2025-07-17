# 🔢 Calculator Using Arduino

This project demonstrates how to build a **basic calculator using Arduino** that can perform arithmetic operations like **addition, subtraction, multiplication, and division** using a **4x4 matrix keypad** and a **16x2 LCD display**.

---

## 📌 Features

- Takes two numbers and an operator as input via keypad
- Displays input and result on 16x2 LCD
- Supports basic operations: `+`, `-`, `*`, `/`
- Handles invalid inputs (e.g., divide by zero)
- Compact and user-friendly hardware interface

---

## 🛠️ Components Used

| Component         | Quantity | Description                        |
|------------------|----------|------------------------------------|
| Arduino UNO/Nano | 1        | Main microcontroller               |
| 4x4 Keypad        | 1        | For numeric and operator input     |
| 16x2 LCD (I2C)    | 1        | Displays input and result          |
| Jumper Wires      | -        | For connections                    |
| Breadboard        | 1        | For circuit assembly               |
| Potentiometer     | 1        | (Optional) Contrast for LCD        |

---

## 🔧 Circuit Connections

### Keypad to Arduino

| Keypad Pin | Arduino Pin |
|------------|-------------|
| R1         | D9          |
| R2         | D8          |
| R3         | D7          |
| R4         | D6          |
| C1         | D5          |
| C2         | D4          |
| C3         | D3          |
| C4         | D2          |

### LCD (I2C) to Arduino

| I2C Pin | Arduino Pin |
|---------|-------------|
| SDA     | A4          |
| SCL     | A5          |
| VCC     | 5V          |
| GND     | GND         |

> *If you're not using I2C LCD, use digital pins and `LiquidCrystal` library instead.*

---

## 👨‍💻 Arduino Code Overview

- Uses **Keypad.h** to interface with 4x4 keypad
- Uses **LiquidCrystal_I2C.h** (or LiquidCrystal.h) to interface with LCD
- Accepts input in form: `Number` → `Operator` → `Number` → `=`  
- Displays the result on LCD

### Example:
