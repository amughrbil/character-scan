# 🎨 Air Canvas Drawing Engine

A bare-metal, native HTML/JS drawing engine using Google MediaPipe. This allows users to draw on the screen using real-time hand tracking and computer vision, with zero external UI frameworks (no React, no extra dependencies).

## 🚀 How to Run
1. Simply double-click `index.html` to open it in any modern web browser.
2. Accept the camera permissions when prompted.
3. Step back so your hands and face are clearly visible in the camera frame.
4. Hit `F11` (or `Fn + F11`) for the full-screen immersive experience.

## 🎮 Gesture Controls
This engine uses a strict 1:1 screen mapping and custom "bone measurement" math to prevent accidental ghost triggers. 

* 🎯 **Left Hand (Index Finger):** Acts as your laser pointer / cursor.
* 🤏 **Right Hand (Pinch):** Draw on the canvas or click UI buttons.
* ✋ **Right Hand (Open Palm):** Acts as a radius eraser. Swipe over lines to delete them.
* ✌️ **Right Hand (Peace Sign):** Toggles the screen lock. Hold for 5 frames to lock your drawing surface to your face movement.
* ↩️ **Undo Button:** Hover and pinch to delete your last drawn stroke.
* 🎨 **Color Wheel:** Hover to preview a color, pinch to lock it in.

## 🛠️ Technical Details
* Built using `@mediapipe/hands` and `@mediapipe/face_mesh`.
* Includes a `OneEuroFilter` for highly stabilized, jitter-free cursor tracking.
* Features a custom smart-undo history stack.
