# 🔧 LED & Fan Control Using Timer2 in Arduino (Register-Level) – Proteus Simulation

This project simulates an LED and fan control system using an Arduino and Timer2 overflow interrupts, developed with register-level programming. Designed and tested using Proteus, it demonstrates precise timing and manual override control via buttons.

## 🚀 Features

- Toggle 3 LEDs and 1 Fan every ~1 second using Timer2 overflow.
- Manual ON/OFF control using push buttons.
- Register-level programming without using delay() or Arduino timers.
- Real-time control override and toggling using interrupts.

## 📁 Files Included

- `Timer2_LED_FAN.ino`: Main Arduino code.
- Proteus simulation file (`.pdsprj`, if available – add it here).
- Schematic diagram (optional: image or Proteus file).

## 🔌 Hardware Pin Mapping

| Component     | Arduino Pin | Register Port |
|---------------|-------------|----------------|
| LED 1         | 13 (PB5)    | `PORTB5`       |
| LED 2         | 8  (PB0)    | `PORTB0`       |
| LED 3         | 9  (PB1)    | `PORTB1`       |
| Fan (Motor)   | 12 (PB4)    | `PORTB4`       |
| Button LED 1  | 2           | Input Pull-up  |
| Button LED 2  | 4           | Input Pull-up  |
| Button LED 3  | 5           | Input Pull-up  |
| Button Fan    | 3           | Input Pull-up  |

## 🧠 How It Works

- **Timer2** is configured in **Normal Mode** with a **1024 prescaler**.
- On every **overflow (~16ms)**, a counter is incremented.
- After ~61 overflows (~1 second), the toggle state changes.
- Each output (LED/Fan) is toggled unless its button is manually pressed.
- Button input overrides the toggling and sets the state HIGH/LOW manually.

## ⚙️ Tools & Technologies

- Arduino UNO (Register-level C++)
- Proteus Design Suite (Simulation)
- Timer2, Interrupts, Direct Register Access

## 📸 Preview (Add if available)

![Simulation Screenshot](path/to/screenshot.png)

## 📌 Usage

1. Load the `.ino` file to Arduino UNO in Proteus.
2. Connect the components as per the pin mapping.
3. Run the simulation.
4. Observe auto toggling and test manual control using buttons.



🔗 Connect with me on [LinkedIn](www.linkedin.com/in/prilectro1809)
