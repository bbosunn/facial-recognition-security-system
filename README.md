# 👁️🔐 Facial Recognition Security System

This project combines **Arduino**, **Python**, and **Teachable Machine** to create a facial recognition security system. If a recognized face is detected, a green light turns on. If not, a password must be entered — or a buzzer will sound on failure.

---

## 📦 Features

- ✅ Face detection using Teachable Machine (TensorFlow/Keras).
- 🟢 Green LED for recognized faces.
- 🔐 Keypad for password entry if face is not recognized.
- 🚨 Buzzer/Red LED on wrong password.
- 🔄 Arduino ↔ Python serial communication.

---

## 🧠 AI Model

- Built using [Teachable Machine](https://teachablemachine.withgoogle.com/)
- Labels:
  - `0 Accepted Faces`
  - `1 Not Accepted Faces`

The trained model is included:
- `labels.txt`

---

## 🛠️ Hardware Requirements

- Arduino Mega 2560
- Keypad (4x3)
- LEDs: Red, Green, Yellow, White
- Buzzer (Optional)
- Webcam
- USB connection to computer

---

## 🧾 Arduino Code

Saved as `ArduinoCode.ino`. It controls the LED logic and keypad input based on serial input from Python.

---

## 🐍 Python Code

Run `WorkingFacialRecognition.py` to:
- Use webcam and run image through the Teachable Machine model.
- Communicate with Arduino over serial.
- Send `"MATCH"` or `"NO_MATCH"` based on prediction.

Make sure to install requirements:

```bash
pip install tensorflow keras opencv-python pyserial numpy
