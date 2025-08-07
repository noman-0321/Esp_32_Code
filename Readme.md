# 🩺 ESP32-Based Health Monitoring System (MAX30102 + Firebase)

A real-time health monitoring project using **ESP32**, **MAX30102 pulse oximeter**, and **Firebase Realtime Database**. It measures **heart rate**, **SpO2**, and **temperature**, and uploads the data to Firebase for remote access.

---

## 🔧 Components Used

- ESP32 Dev Board  
- MAX30102 Pulse Oximeter Sensor  
- MPS20N0040D Pressure Sensor (optional – code included but commented)  
- Firebase Realtime Database  
- Arduino IDE  

---

## 📦 Libraries Required

Before uploading the code, make sure to install these libraries via the **Arduino Library Manager** or manually:

| Library Name              | Install from Library Manager |
|---------------------------|------------------------------|
| MAX30105 by SparkFun     | ✅                           |
| FirebaseESP32 by Mobizt  | ✅                           |
| Q2HX711                   | ✅ (for pressure sensor, optional) |

---

## 📲 Firebase Setup

1. Create a project on [Firebase Console](https://console.firebase.google.com/).
2. Go to **Realtime Database** > **Create Database**.
3. In **Project Settings > Service Accounts > Database Secrets**, get your:
   - `FIREBASE_HOST`
   - `FIREBASE_AUTH_KEY` (a legacy key used in this code)
4. Replace the following placeholders in the code:
   ```cpp
   #define FIREBASE_HOST "your-project.firebaseio.com"
   #define FIREBASE_Authorization_key "your-secret-key"
   #define WIFI_SSID "your-wifi-name"
   #define WIFI_PASSWORD "your-wifi-password"

## ⚙️ Sensor Configuration (MAX30102)
byte ledBrightness = 60;   // LED intensity (0–255)
byte sampleAverage = 4;    // Averages: 1, 2, 4, 8, 16, 32
byte ledMode = 2;          // 1 = Red only, 2 = Red + IR, 3 = Red + IR + Green
byte sampleRate = 100;     // Sample rate (Hz)
int pulseWidth = 411;      // Pulse width: 69–411
int adcRange = 4096;       // ADC range: 2048–16384

## 🚀 Uploading the Code

Open Arduino IDE.
Install ESP32 board support from Boards Manager if not done yet.
Select your board:
Tools > Board > ESP32 Dev Module
Choose the correct COM port.
Paste the provided code into Arduino IDE.
Replace WiFi and Firebase credentials.
Click Upload.

## Viola, It will take soe time to upload the code

