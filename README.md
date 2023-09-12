# Finger-detection

# Finger Detection and Gesture Control

This project demonstrates real-time finger detection using the OpenCV library and hand gesture recognition. It captures video from a webcam and detects hand gestures, allowing you to control a serial device (e.g., Arduino) based on the detected finger positions.

## Table of Contents

- [Introduction](#introduction)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Customization](#customization)
- [Contributing](#contributing)
- [Problems](# Problems I have encountered)

## Introduction

This project aims to showcase hand gesture recognition and control using computer vision techniques. It uses the `cvzone` library, which provides tools for hand tracking, and the OpenCV library for image processing. The program captures video frames from the webcam, detects hand gestures, and translates them into control signals that can be sent to a connected serial device.

## Requirements

To run this project, you need:

- Python (version 3.11 recommended)
- OpenCV (cv2) library
- `cvzone` library
- A webcam
- A serial device (e.g., Arduino) for receiving control signals

## Installation

1. Clone or download this repository to your local machine.

2. Install the required Python packages using pip:

   ```bash
   pip install opencv-python-headless cvzone pyserial
   ```

## Usage

1. Connect your serial device (e.g., Arduino) to the appropriate COM port.

2. Run the `finger_detection.py` script:

   ```bash
   python finger_detection.py
   ```

3. A window will open displaying the webcam feed. Hold your hand in front of the camera, and the program will detect your hand and fingers.

4. Perform specific finger gestures to control the serial device. By default, the following gestures are recognized:
   - Thumb, index finger down, and middle finger down: Send '1'
   - Thumb, index finger up, middle finger down: Send '2'
   - Thumb, index finger up, middle finger up, ring finger down: Send '3'
   - Thumb, index finger up, middle finger up, ring finger up, little finger down: Send '4'
   - All fingers up: Send '5'
   - Other configurations: Send '0'

5. Press 'q' to exit the program.

## Customization

You can customize the program by modifying the `finger_detection.py` script. You can change the gestures and control signals by adjusting the `finger` lists in the `detect` function.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, feel free to open an issue or create a pull request.

## Problems I have encountered
I encountered several challenges while developing this code and seeking inspiration from the work of others. Frequently, the available resources I found were based on earlier versions of Python. However, due to the incompatibilities between these older resources and the newer versions of Python, a choice often needs to be made between downgrading Python or comprehensively modifying the code. For instance, certain functions like getargspec, which were available in previous versions, are no longer accessible in the newer ones.

The code presented in this repository has been crafted to be compatible with Python 3.11, ensuring a smooth execution. Should you opt to download and reinstall a previous Python version, it is crucial to pay careful attention when updating the system's PATH variable to accommodate the new version.

Additionally, there are instances when a "Port cannot be used" error arises. This issue commonly occurs when the serial monitor in Arduino is open. To resolve this, it's necessary to close the serial
monitor and then relaunch the program.

Wishing you a productive and enjoyable programming experience!


![IMG_7691](https://github.com/meliikaa/Finger-detection/assets/111120849/50806ee3-85e6-4a0d-aec9-951378838377)

