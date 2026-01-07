# ✋ Hand Recognition — Control Your Mouse & Keyboard with Hand Gestures

This project uses **OpenCV**, **MediaPipe**, and **PyAutoGUI** to track your hands through a webcam and convert gestures into **mouse** and **keyboard actions** — all in real-time.

It detects hand landmarks and maps your gestures to system input, making it great for accessibility tools, presentations, fun experiments, and automation.

---

## 🚀 Features

✔ Real-time hand-tracking using MediaPipe  
✔ **Left hand → mouse control**  
✔ **Right hand → keyboard swipe gestures**  
✔ “Rock” gesture (thumb touches pinky) → **Spacebar press**  
✔ Simple + lightweight  
✔ Works offline  

---

## 🖐 Hand Gestures and Actions

### 🖱 Left Hand (Mouse Control)

- Move your **left hand** to control the mouse cursor.
- When the **index finger tip goes below the index finger middle joint**, it simulates a **left-click**.

So:
- 🖐 Cursor movement = moving your hand  
- 👆 Index finger down = mouse click  

---

### ⌨ Right Hand (Keyboard Control)

Move your **right hand** to trigger keyboard keys using swipe gestures:

| Gesture | Action |
|--------|--------|
| Swipe Right | `→` Right Arrow |
| Swipe Left | `←` Left Arrow |
| Swipe Up | `↑` Up Arrow |
| Swipe Down | `↓` Down Arrow |

Swipes are detected using the **Index Finger Tip movement**.

---

### 🎸 Rock Gesture (Space Key)

If your **thumb tip touches the pinky MCP joint**, the program interprets this as a **Spacebar** press.

---

## 📂 Project Structure
Gesture-Recognition/
├── .venv/ # Virtual environment
├── main.py # Mouse + Keyboard gesture controller
├── keyboardtest.py # Keyboard-only gesture controller
└── README.md


---

## ⚙️ Requirements

- Python **3.11** (recommended)
- Webcam
- Windows / macOS / Linux

---

## 📦 Installation

### 1️⃣ Create & activate virtual environment (Windows + Git Bash)

```bash
py -3.11 -m venv .venv
source .venv/Scripts/activate

2️⃣ Install dependencies
pip install mediapipe==0.10.11 opencv-python pyautogui

▶️ Run the Program
python main.py


or for keyboard-only gestures:

python keyboardtest.py


Press Q in the camera window to quit.
