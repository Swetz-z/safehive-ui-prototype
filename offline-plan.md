# 📡 SafeHive Offline Emergency Alert Plan

This document outlines how the **offline emergency alert system** will work in the SafeHive mobile app. The goal is to **send emergency alerts and share the user’s location even when there is no mobile network or internet connection**.

---

## 🎯 Objective

Create a peer-to-peer emergency alert system that works **without relying on mobile data**, using:

- 📍 On-device GPS
- 📡 Bluetooth or Wi-Fi Direct
- 🔊 Text-to-Speech Voice Alerts

---

## 🔁 Offline Emergency Flow (Step-by-Step)

1. **User Triggers Emergency**
   - User taps the emergency button in the app.
   - App switches to emergency mode.

2. **Location Access**
   - Phone's built-in GPS is used to get current latitude and longitude.
   - No internet is required for GPS.

3. **Create Alert Message**
   - App generates a local alert like:
     ```
     "Emergency Alert! Medical help needed at Latitude 13.0827, Longitude 80.2707."
     ```

4. **Voice Alert Activation**
   - The alert message is converted to audio using on-device **Text-to-Speech**.
   - It plays loudly to attract attention nearby (offline voice alert).

5. **Broadcast via Bluetooth**
   - The same alert is **broadcast using Bluetooth** to other nearby devices with SafeHive installed (within ~5 km).
   - These nearby devices receive the alert and:
     - Display the emergency type and location.
     - Optionally store the message to forward it later when they’re online.

---

## 🔧 Technologies Used

| Function                   | Tool / Method                 | Works Offline? |
|----------------------------|-------------------------------|----------------|
| UI                         | FlutterFlow                   | ✅              |
| GPS                        | On-device GPS                 | ✅              |
| Voice Alert                | Text-to-Speech (TTS)          | ✅              |
| Alert Sharing              | Bluetooth / Wi-Fi Direct      | ✅              |
| Auth / Data Backup (Future)| Firebase                      | ❌ (online only)|

---

## 🔐 Privacy & Safety

- Data is shared **locally only**, unless internet is available.
- No personal information is broadcast — only the alert and location.
- Device permissions are requested transparently.

---

## 📌 Future Ideas (Post Hackathon)
- Offline mesh networking using **Bluetooth Low Energy (BLE)**
- Auto-connection with volunteers nearby
- Sync to cloud once internet is back

---

## 💡 Why This Matters

Even in areas with **zero signal**, victims can still ask for help — and nearby people can still respond. SafeHive ensures **you’re never alone**, even offline.

