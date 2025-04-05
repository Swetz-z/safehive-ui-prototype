# 📡 SafeHive – Offline Emergency Response Plan with AI Integration

## 🔍 Overview

This document outlines the strategy behind SafeHive’s offline emergency alert system and how AI technologies are planned to be integrated. The objective is to ensure personal safety in no-network zones while leveraging on-device intelligence for enhanced threat response.

---

## 🎯 Objective

To enable emergency distress signals and location alerts **without requiring mobile data or internet**, by using:

- 📍 On-device GPS
- 📡 Bluetooth (or Wi-Fi Direct)
- 🔊 Text-to-Speech (TTS)
- 🤖 AI-based emergency classification (future)
- 🎤 Sensor-based threat detection (planned)

---

## 🔁 Step-by-Step Offline Emergency Flow

1. **Emergency Triggered by User**
   - A dedicated SOS button in the app is tapped.

2. **GPS Location Capture**
   - On-device GPS captures the user's current coordinates.
   - This does not require internet access.

3. **Alert Message Generation**
   - A local alert is created, e.g.:
     ```
     "Emergency Alert! I need help at Latitude 13.0827, Longitude 80.2707."
     ```

4. **Text-to-Speech Voice Playback**
   - The alert is converted to audio and played using **Text-to-Speech (TTS)**.
   - The loud voice alert draws attention from nearby individuals.

5. **Bluetooth Alert Broadcast**
   - The same alert (text + location) is shared via **Bluetooth** or **Wi-Fi Direct** to nearby users who have SafeHive installed.
   - If the recipient device has an internet connection, it can relay the message further.

---

## 🤖 Planned AI Integration

Though full AI functionality requires data access, we are working towards **on-device AI models** for:

### 1. **Emergency Type Prediction (Future AI)**
   - AI analyzes background sounds (e.g., car crash, shouting, glass breaking).
   - Based on this, it categorizes the emergency (medical, assault, accident).
   - The type is included in the Bluetooth alert.

### 2. **Voice/Text Self-Defense Coaching**
   - On-device voice assistant provides calming instructions like:
     - "Try to stay calm. Help is being notified."
     - "Look for safe nearby spaces."
   - All generated using on-device text-to-speech.

### 3. **Threat Detection (Future with TensorFlow Lite)**
   - Detect sharp objects (e.g., knife), aggressive motion or loud sounds.
   - Uses microphone and camera sensors.
   - Could work partially offline using TensorFlow Lite models.

---

## 🔐 Privacy & Safety Considerations

- All data shared offline is **anonymized**.
- No user IDs or personal info are sent over Bluetooth.
- App requests only essential permissions (location, Bluetooth, TTS).

---

## 📦 Tools Used (Offline-Capable)

| Tool                      | Purpose                            | Offline Support |
|---------------------------|------------------------------------|------------------|
| On-device GPS             | Location detection                 | ✅ Yes           |
| Text-to-Speech (TTS)      | Voice alert output                 | ✅ Yes           |
| Bluetooth / Wi-Fi Direct  | Nearby user broadcast              | ✅ Yes           |
| FlutterFlow               | UI building                        | ✅ Partial       |
| Firebase (online only)    | Auth, cloud backup (future use)    | ❌ No            |
| TensorFlow Lite (future)  | AI-based sound/image detection     | ✅ Partial       |

---

## 📈 Future Scope

- Add **BLE Mesh Networking** to create a volunteer alert grid.
- Sync emergency data to cloud once the internet is back.
- Offline AI emergency classification refined using training datasets.

---

## 🧠 Why This is Important

In many parts of India, mobile signal is unreliable. But emergencies don’t wait. SafeHive ensures that **a lack of signal doesn't mean a lack of help**.

Offline alerts + AI = Safety without boundaries.

---
