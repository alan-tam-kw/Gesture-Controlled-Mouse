# Hand-Gesture-Controlled-Cursor

Interactively control your laptop's cursor through hand gestures via the webcam.

**Take a look! (Add Picture and Youtube Link)**


## Built With
* [Python3](https://www.python.org/) - Programming Language
* [OpenCV](https://opencv.org/) - Computer vision and image processing library
* [NumPy](https://numpy.org/) - Scientific computation library
* [PyAutoGUI](https://pyautogui.readthedocs.io/en/latest/) - GUI automation library

## Getting Started

These instructions will get you a copy of the project up and running on your local machine. 

### Prerequisites

Before proceeding, create a virtual environment to store all project files and the following dependencies.

Install OpenCV, NumPy, and PyAutoGUI libraries using pip:

```
pip install opencv-python
```

```
pip install numpy
```

```
pip install PyAutoGUI
```

## Implementation
1. Created a video capture object to access the builtin/external webcam's video stream. 
2. Performed colorspace conversion from BGR (the default colorspace in OpenCV) to grayscale. 
3. Convolved blurring kernel over the images to reduce background noise. 
4. Thresholded pixel intensity values to obtain a binary image. 
5. Obtained the contour of the user's hand by processing all contours in the image and selecting the contour with the largest 
   area. 
6. Obtained the convexl hull of hand's contour.
7. Recorded and stored the total number and coordinates of convexity defects in the contour. 
8. Utilized PyAutoGUI to access and manipulate the cursor based on the total number and coordinates of the convexity defects.
