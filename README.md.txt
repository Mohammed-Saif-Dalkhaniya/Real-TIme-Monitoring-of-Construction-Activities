Real-Time Monitoring of Construction Activities

This project uses computer vision and deep learning to monitor and analyze different stages of construction, providing insights on progress, detected objects, and stage validation. It utilizes a convolutional neural network (CNN) and YOLO (You Only Look Once) object detection model.

Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [File Structure](#file-structure)
- [Technologies Used](#technologies-used)
- [Results](#results)
- [Acknowledgments](#acknowledgments)

Project Overview

The goal of this project is to automate construction site monitoring using image recognition and object detection. The project identifies various construction stages (e.g., foundation, framework) and detects objects like equipment or workers in images from the site.

Features
- Stage Prediction: Classifies images to detect the current construction stage.
- Object Detection: Uses YOLO to detect objects like scaffolding, tools, or vehicles in the images.
- Progress Tracking: Compares images to determine changes in construction stages.
- Error Handling: Validates image stages to prevent incorrect stage assessments.
- Report Generation: Creates a PDF report summarizing the findings.

Setup and Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/YourGitHubUsername/your-repo-name.git
   ```

2. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up the YOLO model files:
   - Download `yolov3.weights` and `yolov3.cfg` files and save them in the `yolo` directory.
   - Make sure `coco.names` is also available in the same directory.

Usage

1. Data Collection: Store images in the `construction image` folder, organized by stage.

2. Train the Model:
   - Run the training script to initialize the CNN for classification.
   - Adjust the hyperparameters as needed.

3. Run Object Detection:
   - Use the `detect_objects` function to detect items in uploaded images.

4. Generate Reports:
   - The `generate_report` function creates a PDF with construction details, predictions, and detected objects.

## File Structure

```
.
├── construction image          # Folder with images organized by stage
├── yolo
│   ├── coco.names              # COCO classes file
│   ├── yolov3.cfg              # YOLO config file
│   └── yolov3.weights          # YOLO weights file
├── requirements.txt            # List of required libraries
└── main.py                     # Main Python script for running the project
```

Technologies Used
- Python: Programming language.
- OpenCV: For image processing and object detection.
- TensorFlow: For building and training the CNN.
- FPDF: For generating PDF reports.

Results

The model provides an accuracy of approximately **XX%** in stage classification and effectively detects key construction objects in images.

