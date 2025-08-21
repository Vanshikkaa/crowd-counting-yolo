👥# Crowd Counting Yolo

A real-time people counting system using YOLO (You Only Look Once) for object detection and SORT (Simple Online and Realtime Tracking) for tracking. Counts people moving upwards and downwards in a video stream, with live visualizations!

🚩 Overview
This project leverages YOLO to detect persons within a video stream and combines it with SORT to track movement and assign unique IDs. It provides real-time counts for both directions (up/down) within user-defined Regions of Interest (ROIs), displaying ongoing results visually on the video.

✨ Key Features
1.Object Detection: Detects people using the YOLO model.
2.Real-time Counting: Counts people moving up/down in real-time.
3.Object Tracking: Follows each person with a unique ID using SORT.
4.Automatic Confidence Filtering: Only counts detections above a set confidence threshold.
5.Live Visualization: Draws bounding boxes and updates up/down counts directly on the video feed.

🛠️ How it Works
1. Initialization
Loads YOLO with pre-trained weights.
Defines two ROIs: one for upward movement, one for downward.
Initializes the SORT tracker (customizable parameters for age, hits, IOU threshold).

2. Object Detection
Continuously grabs video frames.
Applies a mask to focus on the ROIs.
Runs YOLO detection within those ROIs.
Selects bounding boxes and confidence scores for "person" objects.
Applies a configurable threshold to exclude weak detections.

3. Object Tracking
Uses SORT to match objects across frames, giving every person a unique ID.
Continuously updates locations and IDs.

4. Counting & Visualization
Draws boxes around tracked individuals.
Counts people moving up/down each time they cross designated lines in their respective ROIs.

Overlays current up/down counts on the video.

