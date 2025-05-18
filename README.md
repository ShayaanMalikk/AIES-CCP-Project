# AIES-CCP-Project
A real-time object detection and distance estimation system for visually impaired users using YOLO and OpenCV. Provides audio feedback on nearby objects, their positions, distances, and movement direction via text-to-speech.



Real-Time Object Detection for Visually Impaired People
This project is a prototype assistive system that uses computer vision to help visually impaired individuals detect objects and estimate their distances in real-time. It provides spatial awareness through audio feedback, allowing users to be informed if objects are approaching, moving away, or nearby.

Overview
1. Detects objects in real-time using the YOLOv8 model.

2. Estimates object distance from the camera using object size heuristics.

3. Determines the object's position (left, center, right) in the frame.

4. Provides audio alerts using text-to-speech, describing what the object is, where it is, how far it is, and whether it's moving toward or away.

5. Protects privacy by blurring detected persons in the video.

6. Designed as a proof-of-concept for smart assistive devices.
   


Technologies Used
1. YOLO (You Only Look Once) — Real-time object detection model.

2. OpenCV — Video processing and image manipulation.

3. pyttsx3 — Offline text-to-speech engine.

4. NumPy — Numerical operations and geometry calculations.

5. threading & queue — For asynchronous speech delivery.

6. Python — Core language used for implementation.




How It Works
1. Frame Capture

  Reads frames from webcam or video file using OpenCV.

2. Object Detection

  YOLO model identifies objects like people, cars, traffic signs, etc.

3. Distance Estimation

  Calculates distance from camera based on bounding box size.

4. Position Detection

  Classifies each object’s location: left, center, or right.

5. Motion Analysis

  Determines whether an object is approaching, going away, or static.

6. Speech Queue System

  Sends messages to a TTS thread with cooldowns to avoid repetition.
