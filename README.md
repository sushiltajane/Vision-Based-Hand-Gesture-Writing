# Vision-Based-Hand-Gesture-Writing

(Python, OpenCV, MediaPipe)
📌 Overview

This project enables air-writing using hand gestures detected through a webcam. Using MediaPipe Hands, the system tracks the index finger tip and maps its movement onto a digital canvas. Users can draw, switch colors, and clear the canvas — all using gesture-based controls.

✨ Features

Real-time hand landmark detection

Draw using index-finger tracking

Color selection: White, Green, Red, Black

Gesture-based CLEAR button

Dynamic stroke segmentation using deque

Dual output windows:

Frame View (hand + drawing + controls)

Paint Canvas

🛠️ Technologies Used

Python

OpenCV

NumPy

MediaPipe Hands

Deque (collections)

▶️ How It Works

The webcam continuously captures frames.

MediaPipe detects the hand and extracts key landmark points.

The system tracks landmark 8 (index-finger tip) as the drawing point.

If the finger is inside the top panel, the system detects button selections:

CLEAR

WHITE

GREEN

RED

BLACK

If the finger is in the drawing area, strokes are added to the corresponding color deque.

All stored strokes are rendered on both windows.



🚀 How to Run
pip install opencv-python mediapipe numpy
python main.py


Ensure your webcam is connected.

📁 Project Structure
project/
│── main.py
│── README.md