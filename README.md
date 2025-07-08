**Smart Product Traceability Station**

An end-to-end IoT-based system designed to automate the verification, classification, and traceability of products in a manufacturing setup. The solution leverages an ESP32-CAM to scan QR codes, a Python backend to validate the data in real time via Google Sheets, and a second ESP32 board to deliver physical feedback using actuators and displays.

This low-cost, modular system ensures product compliance and streamlines inspection by integrating cloud validation, real-time control, and intuitive feedback mechanisms including an OLED screen, LCD display, RGB LED, buzzer, and servo motor.

Built with:

🔧 ESP32-CAM for scanning

💻 Python + Google Sheets for verification

🤖 ESP32 actuator module for feedback

**📌 Project Outcomes**

✅ Real-time QR scanning using ESP32-CAM and Python (pyzbar)

✅ Cloud verification via Google Sheets API (gspread) using OAuth 2.0

✅ Physical feedback system using:

- 📟 **OLED and LCD**: Display metadata (Device ID, Batch, RoHS, etc.)

- 🔊 **Buzzer** + 🎨 **RGB LED**: Auditory and visual status indication

- 🤖 **Servo motor**: Physical actuation to sort accepted/rejected products


✅ Auto-logging scan results to Google Sheets with timestamps

✅ Modular, low-cost setup ideal for lab demos or small-scale industry use

**⚠️ Limitations**

❌ Only supports QR codes (no text-based OCR yet)

❌ Cloud latency may delay feedback in high-speed use

❌ No encryption (data sent via plain HTTP over Wi-Fi)

❌ Manual OAuth setup needed for Google Sheets API

❌ Currently single-scan processing only (no batching or queuing)

**🚀 Future Scope**

🔎 Add OCR-based label validation (e.g., expiry dates, text recognition)

🧠 Use Edge AI (TFLite, Edge Impulse on ESP32-S3) for local inference

🔐 Upgrade to secure communication (HTTPS or MQTT over TLS)

📊 Build a web dashboard for batch/scan analytics and trend monitoring

🏭 Extend to multi-device or parallel scan support for production lines
