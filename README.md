# 4th Year Project: AI Fitness Assistant 

An AI-based fitness tracking system developed as part of my final year project. This application uses real-time pose detection to monitor exercises, count repetitions, and provide visual feedback — all running locally on the user's machine.

---

## 🎓 Project Overview

This project focuses on applying computer vision techniques to fitness tracking. Using pose estimation, the system analyzes human body movements and determines exercise repetitions without requiring wearable devices.

The goal is to build a lightweight, privacy-focused, and extensible fitness assistant that works in real time using a standard webcam.

---

## ✨ Key Features

* **Real-time Exercise Tracking**
  Automatically detects and counts repetitions.

* **Multiple Exercise Support**
  Includes squats, push-ups, sit-ups, curls, etc.

* **Pose Detection (RTMPose)**
  Efficient and accurate human pose estimation.

* **Visual Feedback System**
  Displays skeleton overlays and joint angles.

* **Custom Exercise Configuration**
  Add new exercises easily via JSON.

* **Local Processing**
  No cloud usage — ensures full privacy.

* **Cross-platform Compatibility**
  Works on Linux, Windows, and macOS.

---

## 🆕 Project Improvements

* Simplified architecture by removing YOLO dependency
* Fully CPU-compatible using RTMPose
* Improved repetition counting logic
* Modular exercise system using `exercises.json`

---

## 🛠️ Tech Stack

* Python
* OpenCV
* RTMPose (ONNX Runtime)
* PyQt5

---

## 📦 Installation

```bash
git clone https://github.com/0xamitr/4th-year.git
cd 4th-year

python -m venv venv
source venv/bin/activate   # Linux/Mac
# or
venv\Scripts\activate      # Windows

pip install -r requirements.txt
```

---

## ▶️ Run the Project

```bash
python run.py
```

---

## 🎯 Custom Exercise Support

All exercise configurations are stored in:

```
data/exercises.json
```

You can define new exercises by specifying:

* Angle thresholds (`up_angle`, `down_angle`)
* Keypoints for joint tracking
* Exercise type

Example:

```json
"custom_exercise": {
  "name_en": "Custom Exercise",
  "down_angle": 120,
  "up_angle": 170,
  "keypoints": {
    "left": [5, 7, 9],
    "right": [6, 8, 10]
  },
  "is_leg_exercise": false
}
```

---

## 🧠 Working Principle

1. Captures video input from webcam
2. Detects human pose using RTMPose
3. Computes joint angles
4. Applies thresholds to count repetitions

---

## 🔮 Future Scope

* Motion correction feedback
* Voice-based guidance
* Enhanced accuracy and tracking
* Expanded exercise library

---

## 📄 License

MIT License

---

## 🙌 Acknowledgement

Pose estimation powered by RTMPose.
