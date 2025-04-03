# Facial-authenticator

Face Verification with OpenCV and DeepFace

Overview

This project captures real-time video from a webcam and performs face verification using the DeepFace library. It compares each frame with a reference image and displays whether a match is found.

Requirements

Ensure you have the following installed:

Python 3.x

OpenCV (cv2)

DeepFace

Threading (built-in with Python)

You can install the required libraries using:

pip install opencv-python deepface

How It Works

Captures video from the webcam.

Loads a reference image (reference.jpg).

Every 30 frames, spawns a new thread to perform face verification.

Displays "It is a match" if the face in the frame matches the reference image, otherwise shows "No match".

Press 'q' to exit the application.

Usage

Place a reference image named reference.jpg in the working directory.

Run the script:

python face_verification.py

Ensure your webcam is functional.

Error Handling

If the webcam fails to open, the script exits with an error message.

If the reference image fails to load, the script exits with an error message.

Handles ValueError and general exceptions gracefully during face verification.

Customization

Modify capture.set(cv2.CAP_PROP_FRAME_WIDTH, 640) and capture.set(cv2.CAP_PROP_FRAME_HEIGHT, 480) to change video resolution.

Change counter%30==0 to adjust the frequency of face verification checks.

Notes

This script assumes the reference image is available in the same directory.

Face verification might take time depending on system performance and DeepFace model execution.

For better results, ensure the reference image is clear and well-lit.

License

This project is for educational purposes and is open for modification and improvement.

