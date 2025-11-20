Hand-Based Sound Controller

This project provides a real-time hand-gesture sound controller using Python, OpenCV, and MediaPipe. By tracking the distance between the thumb and index finger, the system dynamically adjusts the computer’s volume. It is designed for simple, hands-free interaction and works on Windows.

⸻

Features
	•	Real-time hand tracking using MediaPipe
	•	Volume adjustment based on thumb–index finger distance
	•	Visual feedback through on-screen markers and lines
	•	Cross-platform support (Windows with Pycaw; macOS/Linux via native volume commands)
	•	Clean, lightweight, and customizable codebase

⸻

Requirements
	•	Python 3.8 or later
	•	Webcam
	•	Dependencies:
	•	opencv-python
	•	mediapipe
	•	numpy
	•	pycaw (Windows only)

Install dependencies:

pip install opencv-python mediapipe numpy
pip install pycaw   # Windows only


⸻

Usage
	1.	Connect a webcam.
	2.	Clone or download the project.
	3.	Run the script:

python main.py

	4.	A window will appear displaying the camera feed.
	5.	Bring the thumb and index finger together or pull them apart to decrease or increase the volume.
	6.	Press Esc to exit.

⸻

How It Works

The script uses MediaPipe’s hand-landmark detection to identify and track 21 key points on the hand.
Two of these points (landmarks 4 and 8) represent the thumb tip and index finger tip.

The Euclidean distance between these two points is computed each frame.
This distance is linearly mapped to the system’s volume range:
	•	Smaller distance → lower volume
	•	Larger distance → higher volume

The mapping uses interpolation to provide smooth volume transitions.

⸻

Platform Notes

Windows

Uses the Pycaw library to control system volume.
No additional configuration is required beyond installation.

Customization

You can extend the controller by:
	•	Adding gesture-based play/pause or media navigation
	•	Incorporating multiple hands
	•	Modifying sensitivity and distance-to-volume mapping
	•	Integrating with custom audio engines or applications

If you want additional gestures or features, they can be incorporated easily.

⸻

License

This project is released under the MIT License. Use and modify the code freely for personal or commercial purposes.

⸻
