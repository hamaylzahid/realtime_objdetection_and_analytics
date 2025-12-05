<br>
<h3 align="center">REAL-TIME OBJECT DETECTION, TRACKING & ANALYTICS</h3>
<br>

<p align="center">
A complete and production-ready pipeline for real-time object detection, multi-object tracking, and intelligent visitor analytics using YOLOv8 and the SORT tracking algorithm.  
The system delivers accurate tracking, meaningful analytics, and a user-friendly Gradio dashboard, and is optimized for execution on Google Colab, CPU-only machines, and lightweight deployment environments.
</p>

<br>

<p align="center">
  
<!-- Badges -->
<img src="https://img.shields.io/badge/Framework-PyTorch-blue">
<img src="https://img.shields.io/badge/Object%20Detection-YOLOv8-red">
<img src="https://img.shields.io/badge/Tracking-SORT-green">
<img src="https://img.shields.io/badge/Dashboard-Gradio-yellow">
<img src="https://img.shields.io/badge/Optimization-Colab%20%2F%20CPU-orange">
<img src="https://img.shields.io/badge/Python-3.10+-blueviolet">
<img src="https://img.shields.io/badge/Status-Active-success">

</p>

<br>
<h2 align="center">Table of Contents</h2>
<br>

- [Introduction](#introduction)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [How It Works](#how-it-works)
- [Installation](#installation)
- [Usage](#usage)
- [Gradio Dashboard](#gradio-dashboard)
- [Output & Analytics](#output--analytics)
- [Performance Optimization](#performance-optimization)
- [Folder Structure](#folder-structure)
- [Future Improvements](#future-improvements)
- [License](#license)

<br>
<h2 align="center" id="introduction">Introduction</h2>
<br>

This repository implements a **real-time intelligent vision system** with:

- **YOLOv8 object detection**
- **SORT-based multi-object tracking**
- **Analytics engine** (IN/OUT count, dwell-time, region activity)
- **Video processing pipeline**
- **Interactive Gradio dashboard**

Designed for:

- Retail analytics  
- Smart surveillance  
- People counting  
- Automated reporting  
- AI-based monitoring systems  

It runs smoothly in **Google Colab**, lightweight laptops, and CPU environments by using frame-skipping and optimized SORT tracking.

<br>
<h2 align="center" id="key-features">Key Features</h2>
<br>

### 🔹 **Object Detection**
- YOLOv8 (nano/small) for high-speed inference  
- Detects people and other objects  

### 🔹 **Tracking (SORT)**
- Kalman Filter for motion prediction  
- Hungarian Algorithm for ID assignment  
- Stable per-object ID retention  

### 🔹 **Analytics Engine**
- Line-crossing (IN / OUT)  
- Region occupancy  
- Dwell time per tracked object  
- Total visitors  
- Unique ID counting  

### 🔹 **Dashboard**
- Clean UI built with Gradio  
- Upload video → process → download output  
- View analytics instantly  

### 🔹 **Optimized Performance**
- Runs YOLO every 3 frames  
- CPU-friendly  
- Lower memory footprint  

<br>
<h2 align="center" id="tech-stack">Tech Stack</h2>
<br>

- **Python 3.10+**  
- **OpenCV 4+**  
- **PyTorch**  
- **Ultralytics YOLOv8**  
- **SORT Tracking Algorithm**  
- **NumPy / SciPy**  
- **Gradio**  
- **Google Colab optimized**  


<br>
<h2 align="center" id="how-it-works">How It Works</h2>
<br>

1. **YOLOv8 runs detection** every 3 frames for speed.  
2. **SORT tracker** predicts missing boxes and assigns stable IDs.  
3. **Analytics engine** monitors each tracked object:
   - Crossing the virtual counting line  
   - Time spent in region  
   - Entry & exit detection  
4. **Video renderer** draws:
   - Boxes  
   - Object IDs  
   - Dwell-timers  
   - Total visitor counts  
5. A clean Gradio UI displays:
   - Output video  
   - Analytics summary  
   - Download button  

<br>
<h2 align="center" id="installation">Installation</h2>
<br>

### Install dependencies:

```bash
pip install ultralytics opencv-python-headless gradio scipy numpy
```
For local GUI:
```
pip install opencv-python
```

<br>
<h2 align="center" id="usage">Usage</h2>
<br>

### Run in Google Colab

- Copy the full script into a Colab notebook  
- Run the dashboard using:  

```python
dashboard.launch(share=True)
```

-Processing a Video
-Upload .mp4

-System detects + tracks + counts

-Downloads processed output

<br>
<h2 align="center" id="gradio-dashboard">Gradio Dashboard</h2>
<br>

Features inside dashboard:

- Upload video  
- Start processing  
- Live analytics (IN / OUT)  
- Video preview  
- Download processed clip  
- Summary metrics  


<br>
<h2 align="center" id="output--analytics">Output & Analytics</h2>
<br>

You receive:

- Final processed video  
- Bounding boxes + IDs  
- Total visitors  
- Line-crossing counts (IN / OUT)  
- Dwell-time analysis  
- Unique object IDs  
- Processing FPS  
- Total frames processed  


<br>
<h2 align="center" id="performance-optimization">Performance Optimization</h2>
<br>

### To ensure smooth CPU performance:

- YOLO runs every **3 frames**  
- **SORT** handles intermediate tracking  
- Using lightweight model: **yolov8n.pt**  
- **Batch inference disabled** (real-time mode)  
- Frames resized to **640px**  
- **Headless mode** (no GUI windows)

### These optimizations make it suitable for:

- Laptops  
- Raspberry Pi  
- Google Colab  
- Browser-deployed dashboards  


<br>
<h2 align="center" id="future-improvements">Future Improvements</h2>
<br>

- Add heatmap-based region analytics  
- Add crowd density estimation  
- Add human-pose tracking  
- Add YOLOv9 support  
- Add tracking-by-ReID for stronger ID retention  
- Deploy dashboard as a web app  
- Add MongoDB logging for analytics storage

<br>
<h2 align="center">Contact & Contribution</h2>
<br>

<p align="center">
  Have feedback, want to collaborate, or want to extend this project?<br>
  <strong>Let’s connect and enhance real-time object detection and tracking systems together.</strong>
</p>

<p align="center">
  Email: <a href="mailto:maylzahid588@gmail.com">maylzahid588@gmail.com</a> &nbsp; | &nbsp;
  LinkedIn: <a href="https://www.linkedin.com/in/your-linkedin-profile">Profile</a> &nbsp; | &nbsp;
  GitHub Repo: <a href="https://github.com/hamaylzahid/Real-Time-Object-Detection-Tracking">Repository</a>
</p>

<p align="center">
  <a href="https://github.com/hamaylzahid/Real-Time-Object-Detection-Tracking/stargazers">
    <img src="https://img.shields.io/badge/Star%20This%20Project-Give%20a%20Star-yellow?style=for-the-badge&logo=github" alt="Star Badge">
  </a>
  <a href="https://github.com/hamaylzahid/Real-Time-Object-Detection-Tracking/pulls">
    <img src="https://img.shields.io/badge/Contribute-Pull%20Requests%20Welcome-2ea44f?style=for-the-badge&logo=github" alt="PR Badge">
  </a>
</p>

<p align="center">
  Found this project helpful? Give it a star.<br>
  Want to improve it? Submit a pull request and join the development.<br>
</p>

<br>
<h2 align="center">License</h2>
<br>

<p align="center">
  This project is licensed under the <strong>MIT License</strong> and is open for use, modification, and distribution.
</p>

>

<p align="center">
  <strong>Developed with computer vision principles and real-time tracking systems in mind.</strong>
</p>

<p align="center">
  <a href="https://github.com/hamaylzahid">
    <img src="https://img.shields.io/badge/GitHub-%40hamaylzahid-181717?style=flat-square&logo=github" alt="GitHub">
  </a>
  &nbsp;•&nbsp;
  <a href="mailto:maylzahid588@gmail.com">
    <img src="https://img.shields.io/badge/Email-Contact%20Me-red?style=flat-square&logo=gmail&logoColor=white" alt="Email">
  </a>
  &nbsp;•&nbsp;
  <a href="https://github.com/hamaylzahid/Real-Time-Object-Detection-Tracking">
    <img src="https://img.shields.io/badge/Repo-Link-blueviolet?style=flat-square&logo=github" alt="Repo">
  </a>
  <br>
  <a href="https://github.com/hamaylzahid/Real-Time-Object-Detection-Tracking/fork">
    <img src="https://img.shields.io/badge/Fork%20This%20Project-Contribute%20to%20CV-2ea44f?style=flat-square&logo=github" alt="Fork">
  </a>
</p>

<p align="center">
  <sub><i>Designed for real-time object detection, tracking, and analytics showcase.</i></sub>
</p>




