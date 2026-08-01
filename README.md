# 🚦 Traffic Light Simulation using Arduino Uno

A complete and professional smart traffic light system simulation built using **Arduino Uno**, combining hardware schematic validation and interactive browser-based simulation.

---

## 🛠️ Project Overview
This project demonstrates a timed traffic light controller implemented in C++ for Arduino. It sequences through Red, Yellow, and Green lights with precise timing delays, mimicking a real-world intersection traffic signal.

### Tools & Technologies Used:
* **Arduino IDE / C++:** For writing and compiling the microcontroller code.
* **Wokwi Simulator:** For real-time, browser-based hardware simulation.
* **Proteus Professional:** For advanced schematic layout and electronic validation.

---

## 📂 Project Repository Files
* `sketch.ino` - The core Arduino C++ source code.
* `diagram.json` - Wokwi wiring configuration layout.
* `proteus-circuit.png` - Circuit schematic visualization from Proteus.
* `wokwi-simulation.png` - Live execution screenshot from the Wokwi simulator.

---

## 💻 Arduino Source Code (`sketch.ino`)
```cpp
const int redPin = 10;
const int yellowPin = 9;
const int greenPin = 8;

void setup() {
  pinMode(redPin, OUTPUT);
  pinMode(yellowPin, OUTPUT);
  pinMode(greenPin, OUTPUT);
}

void loop() {
  // Red Light ON for 3 seconds
  digitalWrite(redPin, HIGH);
  digitalWrite(yellowPin, LOW);
  digitalWrite(greenPin, LOW);
  delay(3000);

  // Yellow Light ON for 1 second
  digitalWrite(redPin, LOW);
  digitalWrite(yellowPin, HIGH);
  digitalWrite(greenPin, LOW);
  delay(1000);

  // Green Light ON for 3 seconds
  digitalWrite(redPin, LOW);
  digitalWrite(yellowPin, LOW);
  digitalWrite(greenPin, HIGH);
  delay(3000);
}
