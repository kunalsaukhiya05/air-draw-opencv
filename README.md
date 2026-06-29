# Air Draw ✍️

![Python](https://img.shields.io/badge/Python-3.9+-blue?style=for-the-badge&logo=python)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-green?style=for-the-badge&logo=opencv)
![MediaPipe](https://img.shields.io/badge/MediaPipe-Hand%20Tracking-orange?style=for-the-badge)
![NumPy](https://img.shields.io/badge/NumPy-Array%20Processing-lightblue?style=for-the-badge&logo=numpy)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

A touchless drawing app that turns your webcam into a canvas — just move your index finger in the air and watch it draw on screen in real time.

---

## 🚀 Features

- Real-time hand detection from webcam feed
- Drawing controlled entirely by index finger movement
- Continuous, smooth strokes (no shaky/broken lines)
- One-key canvas reset
- Runs fast enough for live use, no lag

---

## 🧠 How It Works

- Reads frames continuously from the webcam using OpenCV
- Runs each frame through MediaPipe's hand landmark model
- Picks out landmark 8 (the index fingertip) from the 21 detected points
- Converts the fingertip's pixel coordinates into draw points each frame
- Draws those points onto a separate canvas layer, then blends it with the live video feed

---

## 🛠️ Tech Stack

- Python
- OpenCV
- MediaPipe
- NumPy

---

## 📦 Installation

1. Clone the repository
```bash
git clone https://github.com/kunalsaukhiya05/air-draw-opencv.git
cd air-draw-opencv
```

2. Install dependencies
```bash
pip install opencv-python mediapipe numpy
```

3. Download the model file
Place [hand_landmarker.task](https://storage.googleapis.com/mediapipe-models/hand_landmarker/hand_landmarker/float16/latest/hand_landmarker.task) in the project directory.

## ▶️ Usage

Run the script:
```bash
python air_draw.py
```

#### 🎮 Controls
- Press `c` → Clear canvas
- Press `q` → Quit

#### 📸 Output
- Webcam window opens on launch
- Index finger acts as the pen
- Strokes appear on screen as you move your finger

#### 🔮 Future Improvements
- Gesture-based color switching
- Eraser mode
- Adjustable brush thickness
- On-screen buttons controlled by gestures
- Export/save drawing as an image

#### 🤝 Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you'd like to change.

#### 📄 License
This project is open-source and available under the MIT License.

#### ⭐ Support
If you found this useful, consider giving it a star ⭐
