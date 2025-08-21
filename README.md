# 👥 Crowd Counting with YOLO + SORT

A **real-time people counting system** built using **YOLO (You Only Look Once)** for object detection and **SORT (Simple Online and Realtime Tracking)** for tracking.
It counts people moving **upwards** and **downwards** in a video stream, with **live visualizations** and real-time updates!

## 🚩 Overview

This project combines **YOLO’s object detection** capabilities with **SORT’s tracking algorithm** to:

* Detect and track individuals across frames.
* Assign **unique IDs** to each detected person.
* Count the number of people crossing user-defined **Regions of Interest (ROIs)** in **upward and downward directions**.
* Display results directly on the video with bounding boxes, IDs, and real-time counts.


## ✨ Key Features

✔️ **Object Detection** – Detects people using YOLO (pre-trained weights).

✔️ **Real-time Counting** – Counts upward/downward movements live.

✔️ **Object Tracking** – Tracks each person across frames with SORT and assigns unique IDs.

✔️ **Confidence Filtering** – Excludes weak detections below a configurable confidence threshold.

✔️ **Live Visualization** – Displays bounding boxes, IDs, and ongoing counts on the video feed.


## 🛠️ How it Works

### 1. **Initialization**

* Loads YOLO with pre-trained weights.
* Defines **two ROIs**: upward and downward movement zones.
* Initializes the SORT tracker (with customizable parameters: age, hits, IOU threshold).

### 2. **Object Detection**

* Continuously processes video frames.
* Applies a **mask** to focus only on ROIs.
* Runs YOLO detection for `person` class.
* Filters results based on confidence threshold.

### 3. **Object Tracking**

* Uses SORT to **match objects across frames**.
* Assigns a **unique ID** to each detected person.
* Updates positions in real-time.

### 4. **Counting & Visualization**

* Draws bounding boxes + IDs around tracked individuals.
* Detects **line crossings** within ROIs.
* Updates **up/down counters** each time a person crosses.
* Overlays counts on the video feed in real time.



## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/crowd-counting-yolo.git
cd crowd-counting-yolo
```

### 2. Install Requirements

```bash
pip install -r requirements.txt
```

### 3. Run the Script

```bash
python crowd_count.py --video input.mp4
```

(Replace `input.mp4` with webcam feed or another video path.)

---

## ⚙️ Configuration

* **Confidence Threshold**: Adjust in `config.py` to filter weak detections.
* **ROIs & Line Positions**: Modify coordinates in the script to suit your video.
* **Tracker Parameters**: SORT hyperparameters can be tuned (age, IOU threshold, hits).


## 📚 Tech Stack

* **YOLO** (You Only Look Once) – Object Detection
* **SORT** – Real-time Object Tracking
* **OpenCV** – Video processing & visualization
* **Python** – Backend logic


## 🤝 Contributing

Contributions are welcome!

* Fork the repo
* Create a new branch (`feature-xyz`)
* Submit a Pull Request 🚀



## 📜 License

This project is licensed under the **MIT License** – feel free to use and modify.


Would you like me to also **add installation instructions for YOLO weights (like YOLOv5/YOLOv8 setup)** so people can run it directly after cloning?
