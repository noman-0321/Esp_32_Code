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
