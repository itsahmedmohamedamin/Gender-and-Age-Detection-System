# Gender-and-Age-Detection-System
This project includes a Python script designed to perform face detection and analysis on images, providing insights into the number of faces detected, their age ranges, and genders. It utilizes `RetinaFace` for face detection and `DeepFace` for analysis.

## Installation

Before running the script, ensure you have all the necessary libraries installed. Run the following commands in your terminal:

```bash
pip install retina-face
pip install deepface
```
## Usage
The project consists of a FaceProcessor class that handles face detection and analysis, and a process_directory function to process all images within a specified directory.

## Processing a Single Image
To analyze a single image:
```bash
img_path = '/path/to/your/image.jpg'
face_processor = FaceProcessor(img_path=img_path)
face_processor.process()
```

## Processing Images in a Directory
To analyze all images in a directory:

```bash
directory_path = '/path/to/your/directory'
process_directory(directory_path)
```

## Features
* `Face Detection`: Identifies faces in an image using RetinaFace.
* `Face Analysis`: Analyzes detected faces to estimate age range and gender using DeepFace.
* `Batch Processing`: Ability to process multiple images in a directory.
* `Image Resizing`: Resizes detected face images to 244x244 pixels for consistent display.

## Methods
* `get_age_range(age)`: Categorizes the exact age into predefined age ranges.
* `detect_faces()`: Detects faces in the provided image and crops them.
* `analyze_faces()`: Analyzes cropped faces to determine age range and gender.
* `process()`: Runs both detection and analysis on the provided image or images in the specified directory.

## Requirements
* Python 3.x
* OpenCV (cv2)
* RetinaFace
* DeepFace
* tempfile (standard library)
* os (standard library)
* Google Colab environment for cv2_imshow (if not using Colab, replace cv2_imshow with cv2.imshow)

## Note
This script is designed to work in a Google Colab environment. If you are using a different environment, make sure to adjust the cv2_imshow import accordingly.
