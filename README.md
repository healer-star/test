# Text Detection using EAST Model and Tesseract OCR
This Python script uses the EAST text detection model and Tesseract OCR to detect and extract text from an image. The EAST model is a deep learning-based text detector that localizes text in scenes with minimal reliance on language-specific character models. Tesseract OCR is an optical character recognition engine for various languages.

## Prerequisites
__OpenCV__: A library used for image processing and computer vision tasks.  
__NumPy__: A library for the numerical operations.  
__Matplotlib__: A library for creating static, interactive, and animated visualizations in Python.  
__PyTesseract__: A Python wrapper for Google's Tesseract-OCR Engine.  
__TensorFlow__: An open-source machine learning framework.  
__Tesseract-OCR__: An optical character recognition engine.  

## Installation
Before running the script, ensure you have installed the required libraries:

```
pip install opencv-python
pip install numpy
pip install matplotlib
pip install pytesseract
pip install tensorflow
```

Additionally, you need to install _Tesseract-OCR_ and set its path in the script.

Download and install Tesseract-OCR from _https://digi.bib.uni-mannheim.de/tesseract/_  
Set the path to the _tesseract.exe_ in the script.

## Usage
Place the __frozen_east_text_detection.pb__(https://github.com/oyyd/frozen_east_text_detection.pb) model file in the same directory as the script.  
Place the image file you want to process in the same directory and name it like img5.jpg.  
Run the script __asg_1.ipynb__.  
The script will perform the following steps:

1.Load the EAST text detection model.  
2.Read the input image.  
3.Convert the image to grayscale and apply thresholding, blurring, and edge detection.  
4.Perform text detection using the EAST model.  
5.Apply Non-Max Suppression (NMS) to filter out overlapping bounding boxes.  
6.For each detected text region, use Tesseract OCR to extract the text.  
7.Display the original image and the image with detected text regions.

## Notes
The script assumes that the input image contains readable text.  
The frozen_east_text_detection.pb model file should be downloaded from a reliable source.  
Adjust the tesseract_cmd and tessdata_dir_config paths according to your Tesseract-OCR installation.  
The script uses matplotlib to display the images. If you prefer to save the images instead, you can use cv2.imwrite() function.

## License
This script is provided for educational purposes. The EAST model and Tesseract-OCR have their respective licenses. Ensure you comply with their terms of use.
