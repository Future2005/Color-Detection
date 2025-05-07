# Color Detection Using OpenCV

This project is a real-time color detection system built using OpenCV and Python. It captures live video from the webcam, detects specific colors (blue, green, yellow), highlights them with bounding boxes, and labels each detected color in the video feed. The goal is to demonstrate how to detect and track predefined color ranges in live video using image processing techniques.

Key Features:

* Real-time detection of specific colors (blue, yellow, green).
* Automatically adjusts brightness to enhance visibility in low-light conditions.
* Uses adaptive thresholding and morphological operations for better mask quality.
* Draws bounding boxes and displays the detected color name over the object.
* Mirrors the webcam feed to act like a mirror for intuitive tracking.
* Simple instruction display with an ESC key shortcut to exit.

Technologies Used:

* Python
* OpenCV (cv2)
* NumPy
* HSV Color Space for color filtering

How It Works:

1. The webcam captures a live video stream.
2. The frame is flipped horizontally for a natural mirror effect.
3. The brightness of the frame is increased for better clarity.
4. The frame is converted from BGR to HSV color space.
5. For each defined color, a mask is created using HSV lower and upper bounds.
6. Morphological operations (closing) and adaptive thresholding are applied to clean up the mask.
7. Contours are detected, and bounding boxes are drawn around the colored areas.
8. Labels are added to indicate which color is detected.

Requirements:

Install the following Python libraries:

pip install opencv-python numpy

How to Run:

1. Clone the repository.
2. Run the main script using:

python main.py

3. A webcam window will open.
4. Move colored objects in front of the camera to see real-time detection.
5. Press the ESC key to close the application.

File Structure:

* main.py: Main script that handles the webcam feed, detection, and display.
* util.py: Contains utility functions such as color limits for different color names.
* README.md: Project description and usage guide.

Notes:

* The color ranges are defined in the HSV space and can be modified in `util.py` to add more colors.
* You can improve detection accuracy by adjusting the HSV ranges or adding support for more colors.
* Make sure your environment has proper lighting for best results.

This project demonstrates basic but powerful computer vision techniques to detect and label colors in real time, useful for applications like gesture recognition, object tracking, and educational tools.
