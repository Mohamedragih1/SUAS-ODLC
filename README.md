# YOLO Shape and Color Recognition

This Python script utilizes machine learning and image processing techniques to identify and classify shapes and colors in images. The script is designed to work in a Google Colab environment and uses several Python libraries including pandas, numpy, joblib, easyocr, cv2, and ultralytics.

## Installation

The script requires the installation of two Python libraries: ultralytics and easyocr. These libraries can be installed using pip, the Python package installer. The following commands can be used to install these libraries:

```bash
!pip install ultralytics
!pip install easyocr
```

## Usage
The script is designed to work with a specific directory structure and file naming convention. The script expects to find a directory named 'MyDrive/Colab Data/' in the Google Drive mounted to the Colab environment. Within this directory, it expects to find a subdirectory named 'YOLO Shape Detector/runs/detect/train/weights/' that contains a file named 'best.pt'. This file is a pre-trained YOLO model used for shape detection.

The script also expects to find a file named 'random_forest_model.pkl' in a subdirectory named 'Color Classification/'. This file is a pre-trained Random Forest model used for color classification.

The script processes a series of images named 'image1.jpg', 'image2.jpg', ..., 'image20.jpg' located in a subdirectory named 'test imgs/'. For each image, it performs the following steps:

It uses the YOLO model to detect shapes in the image.
It uses the k-means clustering algorithm to separate the detected shapes into three clusters: the largest (background), the second largest, and the third largest.
It uses the EasyOCR library to recognize letters in the image.
It uses the Random Forest model to classify the colors of the shapes and letters.
The results are displayed in the Colab environment and include the predicted color and letter for each shape detected in the image.
