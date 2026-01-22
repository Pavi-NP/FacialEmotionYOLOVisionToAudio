# People Detection and Facial Emotion Analysis with YOLOv8 & DeepFace in Google Colab

This project demonstrates how to detect people in an image using the YOLOv8 object detection model and analyze their facial expressions using DeepFace — all within Google Colab. The script displays the uploaded image, identifies people, detects facial emotions, and generates an audio description played inline.

Key highlights:
- Detects multiple people in an image using **YOLOv8**
- Analyzes facial emotions with **DeepFace**
- Generates **text summaries** of detected persons and emotions
- Converts text summaries to **audio** using **gTTS**
- Modular and scalable pipeline suitable for **research and government applications**

---

## Features

- Upload and display images in **Google Colab**
- Detect people in images using **YOLOv8**
- Detect faces within detected persons
- Classify facial emotions (angry, happy, sad, neutral, surprise) using **DeepFace**
- Generate and play descriptive audio summaries
- Fast inference (~230ms per image)
- Error-handling and fallback logic for missing or unclear faces

---
## Architecture


<img width="1536" height="1024" alt="ChatGPT Image Jan 23, 2026 at 12_31_10 AM" src="https://github.com/user-attachments/assets/f07d2139-ebb3-4f80-8a39-c747cd8f1211" />

The system consists of the following modules:

1. **Image Upload**
   - User uploads an image via Colab
2. **Preprocessing**
   - Image loaded with OpenCV
   - ROI extraction for detected persons
3. **People Detection**
   - YOLOv8 detects all persons and outputs bounding boxes
4. **Facial Emotion Analysis**
   - DeepFace predicts dominant emotions per person
5. **Summary Generation**
   - Compiles person counts and emotion statistics into text
6. **Audio Output**
   - gTTS converts text summaries into audio
   - Audio is played inline in Colab

---

### Display the image
<img width="401" height="397" alt="Screenshot 2025-09-12 at 10 58 53 pm" src="https://github.com/user-attachments/assets/42d5b5a6-e5e1-485a-8fb4-768e6c3d4efe" />

image credit: https://stock.adobe.com/search?k=multiple+face+emotions&asset_id=618892328

---
### Result as an audio 

0: 608x640 9 persons, 230.1ms
Speed: 8.2ms preprocess, 230.1ms inference, 3.6ms postprocess per image at shape (1, 3, 608, 640)

I detected 9 persons. Facial expressions include: 3 angry, 2 neutral, 2 surprise, 1 happy, 1 sad

Playing audio...

[download.mp3](https://github.com/user-attachments/files/22298585/download.mp3)

---
### License
This project is for educational purposes. Feel free to modify and extend!

### Acknowledgements
    Ultralytics YOLOv8
    DeepFace
    gTTS

## Setup Instructions

### Install dependencies

Run this cell in Colab to install necessary libraries:

```python
!pip install ultralytics deepface gtts opencv-python-headless numpy matplotlib
---
