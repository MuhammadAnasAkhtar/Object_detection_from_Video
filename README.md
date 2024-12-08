Video Object Detection Application
# Overview
The Video Object Detection Application is a tool for detecting and tracking objects in videos. Using a pre-trained object detection model, the application processes each frame of an uploaded video to identify objects, draw bounding boxes, and display labels along with confidence scores. It then outputs the processed video with all the visual annotations.

This project is part of the @GenAILearniverse initiative, focusing on practical AI applications.

# Features
Object Detection in Videos: Processes each frame to detect objects.
Bounding Boxes: Draws bounding boxes around detected objects.
Labels and Confidence Scores: Displays object names and their detection confidence directly on the video frames.
Multi-Codec Support: Handles video encoding with multiple codecs for compatibility.
# How It Works
Upload a Video: Users upload a video in supported formats (e.g., MP4, AVI).
Process Video: The application uses the facebook/detr-resnet-50 model to detect objects frame by frame.
Output Processed Video: Returns the processed video with annotated frames, ready for download or preview.
# Installation and Setup
To run the application locally:

Clone the Repository:

bash
Copy code
git clone https://github.com/yourusername/video-object-detection.git
cd video-object-detection
Install Dependencies: Create a virtual environment and install the required packages:

bash
Copy code
pip install -r requirements.txt
Run the Application:

bash
Copy code
python app.py
Access the Interface: Open your browser and navigate to http://localhost:7860 to interact with the application.

Usage
Upload Video:

Use the "Upload Video" button to select a video file.
Process Video:

Click "Submit" to start processing the video. Progress will be displayed in real-time.
Download/Preview Processed Video:

Once processing is complete, the annotated video will be available for download or preview.
# Dependencies
Gradio: For creating the web-based user interface.
Transformers: For utilizing the pre-trained facebook/detr-resnet-50 model.
OpenCV: For video processing, including reading, writing, and handling frames.
Pillow: For image manipulation and drawing bounding boxes.
Install all dependencies with:

bash
Copy code
pip install -r requirements.txt
# File Structure
php
Copy code
video-object-detection/
│
├── app.py                # Main application script
├── requirements.txt      # Python dependencies
├── README.md             # Documentation
├── example_videos/       # Folder for example videos (optional)
└── output_videos/        # Folder for processed videos (optional, dynamically created)
Example
Input:
A video file showing street scenes with pedestrians, vehicles, and other objects.

Output:
The same video with:

Bounding boxes around detected objects.
Labels such as "Car" or "Person" with detection confidence scores (e.g., 0.95).
# Model Details
Model Used: facebook/detr-resnet-50
Purpose: Object detection using a transformer-based approach.
Source: Hugging Face Transformers library.
# Limitations
Processing Time: Long videos may take considerable time to process.
Codec Support: Some video formats might not be supported due to codec issues. Use MP4 or AVI for best results.
# Future Enhancements
Add real-time video processing via webcam.
Optimize processing speed for larger videos.
Expand support for additional video formats and codecs.
# Contributing
Contributions are welcome! Please fork the repository, make your changes, and submit a pull request.

