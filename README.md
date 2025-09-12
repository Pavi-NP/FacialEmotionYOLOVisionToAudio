# People Detection and Facial Emotion Analysis with YOLOv8 & DeepFace in Google Colab

This project demonstrates how to detect people in an image using the YOLOv8 object detection model and analyze their facial expressions using DeepFace — all within Google Colab. The script displays the uploaded image, identifies people, detects facial emotions, and generates an audio description played inline.

---

## Features

- Upload and display an image in Colab
- Detect persons using YOLOv8
- Detect faces within detected persons
- Analyze facial emotions using DeepFace
- Generate and play a descriptive audio summary

---
### License
This project is for educational purposes. Feel free to modify and extend!

### Acknowledgements
    Ultralytics YOLOv8
    DeepFace
    gTTS

## Setup Instructions

### 1. Install dependencies

Run this cell in Colab to install necessary libraries:

```python
!pip install ultralytics deepface gtts opencv-python-headless numpy matplotlib
