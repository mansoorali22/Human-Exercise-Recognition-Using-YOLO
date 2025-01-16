# Human-Exercise-Recognition-Using-YOLO
## Exercise Recognition Pipeline

This project focuses on building an exercise recognition pipeline that integrates object detection, 3D pose estimation, and classification using deep learning techniques. The pipeline leverages YOLO for detecting the bounding box around a person, a pretrained model for estimating 3D body landmarks, and a custom CNN for exercise classification based on the 3D landmark data. The final output includes a visualization of the detected 3D landmarks on the original image along with the predicted exercise.

## Objective

To develop a robust pipeline that can detect, estimate, and classify exercises performed by a person using advanced deep learning models and techniques.

## Dataset

- The dataset contains data for various exercise types, including annotated 3D landmark positions and other features.
- It represents 10 different physical poses that distinguish 5 exercises: Push-up, Pull-up, Sit-up, Jumping Jack, and Squat.
- Each exercise has 2 classes representing its terminal positions (e.g., "up" and "down" positions for push-ups).

## Tasks

1. **Image Acquisition**  
   - Capture an image or frame from a video of a person performing an exercise.  
   - The input image should clearly show a person performing one of the five exercises.

2. **Bounding Box Detection Using YOLO**  
   - Use a pretrained YOLO model to detect and localize the person in the image.

3. **3D Pose Estimation Using a Pretrained Model**  
   - Crop the image based on the bounding box detected by YOLO.  
   - Use a pretrained model (e.g., MediaPipe with 33 landmarks) to estimate 3D body landmarks.  
   - Predict 3D landmark coordinates (x, y, z) for key body points (e.g., shoulders, elbows, knees).  
   - Visualize the detected 3D landmarks on the original input image.

4. **Custom CNN for Exercise Classification**  
   - Build a custom Convolutional Neural Network (CNN) to classify exercises based on the 3D landmark data.  
   - Train the CNN using the dataset to ensure it generalizes well to different examples.  
   - Evaluate the CNN's performance using metrics such as accuracy, precision, recall, and F1-score.

5. **Mapping and Visualization**  
   - Overlay the detected 3D landmarks and the predicted exercise label on the original image for visual clarity.
