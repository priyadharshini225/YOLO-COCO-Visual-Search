# YOLOv11 Visual Search Application

Fast, Accurate, and Intelligent Image Search using YOLOv11 + Streamlit

# Abstract / Introduction

This project presents an intelligent visual search system built using YOLOv11 and Streamlit, designed to perform fast object detection and metadata-driven search across image collections.
The system processes raw images, runs YOLOv11 inference, extracts detections, generates metadata, and provides a powerful search interface using class-based and count-based filtering with logical AND / OR operations.

The application is optimized for deployment in VS Code using a Conda environment, supporting both CPU and GPU execution modes, and offers a clean, user-friendly interface for real-time visualization and search.

## Features

⚡ YOLOv11 Object Detection

High-speed, high-accuracy detection,
Runs on CPU or GPU,
Saves metadata for fast reload

📦 Metadata Creation

Stores per-image JSON files
Includes counts, class names, bounding boxes, etc.

🔍 Smart Search Engine

Supports:

Class-based search,
Object count thresholds,
AND / OR logic,
Instant metadata-based search

🖼️ Output Visualization

Bounding box overlay,
Confidence scores,
3-column image grid,
Detected object summary

```
# Project Structure
Yolo_11/
├── app.py
├── configs/
│   └── default.yaml
├── src/
│   ├── inference.py
│   ├── config.py
│   └── utils.py
├── data/
│   ├── raw/
│   └── processed/
└── test/
```
## Environment Setup (Conda)

The project must be executed locally using VS Code + Conda environment.

Create Conda Environment
```
conda create -n yolo11env python=3.10 -y
conda activate yolo11env
```
Install Dependencies
```
pip install -r requirements.txt
```
## GPU Installation Steps

(For NVIDIA CUDA systems)

1️⃣ Install PyTorch GPU version
```
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
```

2️⃣ Install YOLOv11 + remaining libraries
```
pip install ultralytics streamlit opencv-python pillow pyyaml
```

## How to Run in VS Code Using Conda

1. Open project in VS Code

2. Select the Conda environment:

3. Activate terminal:

4. conda activate yolo11env

5. Run the application:
```
streamlit run app.py
```
## Deployment Using Streamlit

Once executed, Streamlit launches automatically at:

### http://localhost:8501/

## Application Snapshots

### Main Screen
<img width="1786" height="637" alt="image" src="https://github.com/user-attachments/assets/5e34a57b-2663-4698-9ede-43b0d5079bb3" />

### Processing Images
<img width="1825" height="734" alt="image" src="https://github.com/user-attachments/assets/bd6ac76e-ae50-4355-a596-795a7d0482e7" />

### Search Interface
<img width="1813" height="611" alt="image" src="https://github.com/user-attachments/assets/97feb2fc-175d-49b1-963d-5cbf11fb7bff" />

### Search Results
<img width="1810" height="613" alt="image" src="https://github.com/user-attachments/assets/5ecd7e43-8ef0-4f5f-be6f-b27260f5557f" />
<img width="1780" height="816" alt="image" src="https://github.com/user-attachments/assets/3b306145-d8f5-4261-9a1c-94d23505ed39" />
<img width="1868" height="903" alt="image" src="https://github.com/user-attachments/assets/fc50fd58-a75c-4505-8e45-07532031196a" />

## How It Works
1. Object Detection :-
   Processes images and runs YOLOv11 inference
   Extracts classes, confidence scores, and bounding boxes
   Counts objects per class

2. Metadata Creation :-
   Saves results in data/processed/.../metadata.json
   Enables very fast future searches

3. Smart Search System
   
   Supports:
   Class-based search,
   Count thresholds (1, 2, 5, or any),
   AND / OR logic.

5. Visual Output :-
  
3-column image grid,
Class labels + confidence,
Color-coded bounding boxes,
List of detected objects,

## Technologies Used

YOLOv11 (Ultralytics)

Streamlit

OpenCV

Pillow

PyYAML

## Dataset
The dataset used in this project is not included in the repository due to size limitations.  
You can access all raw images and processed metadata from the link below:

👉 **[Click Here to View/Download the Dataset](https://drive.google.com/drive/folders/1Q2x7sDBjj1cfqVx9DakbuRDo0TaDATTR?usp=drive_link)**

This folder contains:

- Raw Images (used for detection)  
- Processed Metadata (JSON files generated after YOLOv11 inference)  
- Sample Outputs  

Sample Outputs
## License

All Rights Reserved
Unauthorized copying, modification, or redistribution of this project is prohibited.

