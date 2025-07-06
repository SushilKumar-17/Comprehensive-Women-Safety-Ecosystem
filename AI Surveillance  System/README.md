# AI CCTV Surveillance System 

An intelligent, gender-aware CCTV surveillance system that integrates real-time object detection, gender classification, and strategic decision logic for SOS alerting and safety monitoring.

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white"/>
  <img src="https://img.shields.io/badge/YOLOv5-FFCC00?style=for-the-badge&logo=darkreader&logoColor=black"/>
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white"/>
  <img src="https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white"/>
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white"/>
  <img src="https://img.shields.io/badge/DeepSORT-0A192F?style=for-the-badge&logo=github&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-FA8C16?style=for-the-badge&logo=jupyter&logoColor=white"/>
</p>


##  Project Overview

This system leverages state-of-the-art computer vision and deep learning models to analyze CCTV footage and detect suspicious or critical patterns, especially focused on **women safety analytics**.

Key capabilities include:
- Real-time object detection using YOLOv5.
- Gender classification using a custom CNN model (`.h5`).
- Person tracking using Deep SORT.
- Context-aware logic for raising alerts (e.g., lone female at night, surrounded female, etc.).

---

## 📂 Directory Structure

```
AI_CCTV/<br>
├── CCTV Gender Classifier Dataset/ # Dataset used to train gender classification model<br>
├── Gender Classification Model/ `# Model training code and artifacts`<br>
├── SOS_Recordings/ `# Recordings triggered in SOS conditions`<br>
├── SOS_Videos/ `# Clips saved when a critical situation is detected`<br>
├── yolov5/ `# YOLOv5 source code and modifications`<br>
├── cctv_gender_classifier.h5 `# Trained gender classifier model`<br>
├── Main AiCCTV Pipeline.ipynb `# Main pipeline integrating all components`<br>
├── CCTV Working.mp4 `# Sample working demo of the system`<br>
└── README.md `# This file`<br>
```
---

## Pipeline Overview

## 1. Object Detection – YOLOv5
- **Model Used**: `yolov5s.pt` (can switch between `yolov5n`, `yolov5m`, `yolov5l` based on hardware constraints)
- **Purpose**: Detects persons in each CCTV frame
- **Framework**: PyTorch

## 2. Person Tracking – Deep SORT

- **Purpose**: Tracks individuals across video frames using unique IDs
- **Input**: Bounding boxes from YOLOv5 detection
- **Output**: Consistently tracked persons across frames
- **Method**: Deep SORT with appearance-based ReID (re-identification) features

---

## 3. Gender Classification – CNN

- **Model File**: `cctv_gender_classifier.h5`
- **Framework**: TensorFlow / Keras
- **Training Data**: Labeled cropped facial images (Male / Female)
- **Input**: 64x64 RGB face crop from detected person
- **Output**: Gender prediction (`Male` or `Female`)

## Logic Layer – Safety Event Detection

This layer applies safety logic using detection, tracking, and gender classification.

| **Scenario**             | **Condition**                                | **Action**                          |
|--------------------------|----------------------------------------------|-------------------------------------|
| Lone woman at night      | One female, no males nearby, during night    | Save video and trigger alert        |
| Surrounded female        | Female:Male ratio below defined threshold    | Start recording and raise alert     |
| Zone intrusion (optional)| Sudden entry into restricted zone            | Log event or trigger alert          |

## Demo
### CCTV-Based Threat Recognition Demo

<div align="center">
  <img src="assets/vid.gif" width="600" alt="Video">
</div>

## Screenshots
<div align="centre">
    <img src="SOS_Recordings/Screenshots/img (1).png" width="530" />
    <img src="SOS_Recordings/Screenshots/img (2).png" width="400" />
</div>

## Input and Output
**Input:** Live camera feed or recorded CCTV footage<br>
**Outputs:**
    - Annotated video with bounding boxes and gender labels<br>
    - Event-based video clips `(saved to SOS_Videos/)`<br>
    - Audio alerts `(saved to SOS_Recordings/)`<br>
    - Gender count statistics (optional logs)<br>



## Ethics and Privacy
- All video processing is done locally, ensuring privacy
- Designed for authorized safety use only
- Avoids cloud upload or third-party access

```
**Demo**
To see the system in action, watch the recorded video: `CCTV Working.mp4`
```
