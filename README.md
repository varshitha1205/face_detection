# face_detection_using_opencv
Project Overview:

The application displays an input image, its grayscale version, and the result after detecting faces. The face detection is performed using OpenCV's Haar Cascade Classifier, which is a popular method for object detection, particularly for identifying human faces. The detected faces are highlighted with green rectangles.

Key Components:

GUI Layout:

The application uses Tkinter to create a window with a size of 900x500 pixels. The window is titled "Multiple face detection using opencv" and has a cyan background. Three images are displayed side by side: the original image, its grayscale version, and the image with detected faces marked. Labels are used to provide descriptions for each image ("Input Image," "Grayscale Image," and "Output Image").

Image Handling:

The image fam.jpg is loaded using OpenCV (cv2.imread). OpenCV reads images in BGR format, but since Tkinter's image display expects RGB format, the color channels are split and merged in RGB order. The image is resized to 240x240 pixels and displayed in the GUI using Pillow's ImageTk.

Grayscale Conversion:

The input image is converted to grayscale using OpenCV’s cv2.cvtColor function. The grayscale image is resized and displayed in the second section of the window. Face Detection:

The Haar Cascade Classifier (haarcascade_frontalface_default.xml) is used to detect faces within the grayscale image. Detected faces are enclosed in green rectangles using cv2.rectangle.

The result is converted back to RGB format and displayed as the third image in the GUI. Face Detection Process:

The cv2.CascadeClassifier.detectMultiScale method is used to locate faces in the grayscale image. For each detected face, the coordinates (x, y) and dimensions (w, h) are used to draw a rectangle around the face on the original image.

Output:

The program creates a window that shows three images:

Input Image: The original loaded image (fam.jpg).

Grayscale Image: A grayscale version of the input image.

Output Image: The input image with green rectangles drawn around detected faces.
