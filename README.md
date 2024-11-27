# Object Detection and Tracking with YOLOv5 and DeepSORT

This project implements **real-time object detection and tracking** using the YOLOv5 model and **DeepSORT**. The goal is to detect and track multiple objects (e.g., people, bottles, etc.) in a video stream (live camera feed or pre-recorded video). The system uses YOLOv5 for object detection and DeepSORT for tracking detected objects over time.

## Features
- **Object Detection**: Uses YOLOv5 to detect multiple objects in real time.
- **Object Tracking**: Tracks objects across frames using DeepSORT.
- **Real-Time Processing**: Displays live object detection and tracking results from the webcam or a video file.
- **Works with Various Objects**: Capable of detecting common objects like people, bottles, knives, and books.

## Installation

To get started, follow the steps below to set up the environment:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/object-detection-tracking.git
   cd object-detection-tracking
### Install dependencies:
pip install -r requirements.txt

### Requirements
This project may require high system specifications for smooth operation, especially when using the DeepSORT tracker alongside YOLOv5. GPU support is recommended for faster processing and to avoid lags.

Operating System: Windows/Linux/MacOS
Python Version: 3.7+
Libraries:
torch (PyTorch for YOLOv5)
opencv-python (for video processing)
deep_sort_realtime (for object tracking)

### For GPU support (recommended for real-time processing):

CUDA-enabled GPU (NVIDIA)
PyTorch installed with CUDA support (GPU version)

## How It Works
### Object Detection with YOLOv5:

### 1. YOLOv5 is used to detect various objects in the frame. The model classifies the objects and assigns confidence scores for each detection.
### 2. Objects detected with a confidence score higher than 30% (configurable) are passed on to the tracking algorithm.

### Object Tracking with DeepSORT:

### 1. Once YOLOv5 detects the objects, DeepSORT tracks those objects across frames. The tracker assigns unique IDs to each object and follows their movements in real-time.
### 2. Tracked objects are shown with their bounding boxes, class names, and unique IDs.

## Performance Considerations:

### 1. High PC compatibility is recommended. The system may experience lag or slower performance on devices with low CPU/GPU performance.
### 3. If you experience lag, try lowering the video resolution or use a lighter YOLOv5 model (like yolov5n).

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements
YOLOv5: https://github.com/ultralytics/yolov5
DeepSORT: https://github.com/nwojke/deep_sort
