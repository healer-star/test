Text Detection using EAST Model and Tesseract OCR
This Python script uses the EAST text detection model and Tesseract OCR to detect and extract text from an image. The EAST model is a deep learning-based text detector that localizes text in scenes with minimal reliance on language-specific character models. Tesseract OCR is an optical character recognition engine for various languages.

Prerequisites
OpenCV: A library used for image processing and computer vision tasks.
NumPy: A library for the numerical operations.
Matplotlib: A library for creating static, interactive, and animated visualizations in Python.
PyTesseract: A Python wrapper for Google's Tesseract-OCR Engine.
TensorFlow: An open-source machine learning framework.
Tesseract-OCR: An optical character recognition engine.
Installation
Before running the script, ensure you have installed the required libraries:

bash
pip install opencv-python numpy matplotlib pytesseract tensorflow
Additionally, you need to install Tesseract-OCR and set its path in the script.

Download and install Tesseract-OCR from https://github.com/tesseract-ocr/tesseract
Set the path to the tesseract.exe in the script.
Usage
Place the frozen_east_text_detection.pb model file in the same directory as the script.
Place the image file you want to process in the same directory and name it img5.jpg.
Run the script.
The script will perform the following steps:

Load the EAST text detection model.
Read the input image.
Convert the image to grayscale and apply thresholding, blurring, and edge detection.
Perform text detection using the EAST model.
Apply Non-Max Suppression (NMS) to filter out overlapping bounding boxes.
For each detected text region, use Tesseract OCR to extract the text.
Display the original image and the image with detected text regions.
Notes
The script assumes that the input image contains readable text.
The frozen_east_text_detection.pb model file should be downloaded from a reliable source.
Adjust the tesseract_cmd and tessdata_dir_config paths according to your Tesseract-OCR installation.
The script uses matplotlib to display the images. If you prefer to save the images instead, you can use cv2.imwrite() function.
License
This script is provided for educational purposes. The EAST model and Tesseract-OCR have their respective licenses. Ensure you comply with their terms of use.
