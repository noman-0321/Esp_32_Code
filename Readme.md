# Arduino Sensor Module

This module runs on an Arduino-compatible board to read pulse and oxygen data using the MAX30102 sensor.

## Setup Instructions

1. **Install Arduino IDE**: [Download](https://www.arduino.cc/en/software)
2. **Install Required Drivers** (CH340/CP2102 if needed)
3. **Connect Hardware**:
   - VCC → 3.3V
   - GND → GND
   - SDA → A4 (Uno) / GPIO21 (ESP32)
   - SCL → A5 (Uno) / GPIO22 (ESP32)
4. **Load Code**:
   - Open `Max_30102.ino` in Arduino IDE
   - Select correct board and COM port from Tools menu
   - Install `SparkFun MAX3010x` library via Library Manager
   - Click Upload
5. **Monitor Output**: Open Serial Monitor (Ctrl+Shift+M)

## Output
- Serial output with heart rate and oxygen data
