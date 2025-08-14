# NBA


## **README.md**

# Out of Bounds & Last Touch Detection using Hybrid Sensor + Video Data

🚧 **Status:** *Work in Progress* – This is my current active project.

## **Overview**

This project aims to automate **out-of-bounds** and **last-touch detection** in basketball using a **hybrid approach** that combines:

* **Sensor data** (RSSI or positional data)
* **Video footage** (computer vision-based analysis)

The goal is to create a robust, real-time system that can assist referees by detecting when the ball or player steps out of bounds, and determining which player touched the ball last before it went out.

---

## **Motivation**

Manual referee calls in basketball are often made at high speed and can be prone to error—especially in **fast break** or **crowded corner** situations. This project focuses on leveraging **AI, deep learning, and sensor fusion** to increase decision accuracy and reduce human error.

---

## **Approach**

### 1. **Data Sources**

* **Video Data** – Extracted frames from basketball game footage using OpenCV.
* **Sensor Data** – Player and ball positional signals (RSSI or tracking beacons).

### 2. **Computer Vision (CV)**

* **YOLOv8** for player and ball detection.
* **Hough Transform** for detecting court lines and boundaries.
* **Frame-level tracking** to maintain player and ball identities over time.

### 3. **Sensor Fusion**

* Merge positional data from sensors with video detections for better accuracy.
* Use a Kalman Filter to smooth positional tracking and handle occlusion cases.

### 4. **Last-Touch Detection**

* Track ball trajectory + proximity of players to determine last contact before an out-of-bounds event.

---

## **Current Progress**

✅ Frame extraction from video
✅ Object detection (players & ball) using YOLOv8
✅ Court line detection using Hough Transform
✅ Basic out-of-bounds detection logic implemented

🔄 **In Progress:**

* Integrating sensor data with CV outputs
* Implementing last-touch detection logic
* Adding real-time inference pipeline

---

## **Tech Stack**

* **Python**
* **OpenCV**
* **YOLOv8** (Ultralytics)
* **NumPy / Pandas** for data handling
* **Matplotlib** for visualization
* **Sensor data parsing** modules (custom)

---

## **Future Work**

* Improve robustness under occlusion and fast motion
* Deploy as a real-time referee-assist system
* Add multi-angle camera integration
* Expand detection for other sports

---

## **Author**

**Onkar Kunte**
AI Engineer | Computer Vision & NLP Enthusiast


---

Do you want me to also **add a “Demo” section with sample output images** from your notebook so the GitHub page looks more visually appealing? That will make a big difference for recruiters clicking your repo.
