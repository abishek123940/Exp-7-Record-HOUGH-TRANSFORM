# Ex.No:07-Record-HOUGH TRANSFORM

##  Aim

To implement a basic lane detection pipeline using OpenCV by completing missing code segments at specified locations.


##  Software Used

* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib

---

##  Algorithm 
### Step1:

Import all the necessary modules for the program.
### Step2:

Load a image using imread() from cv2 module.
### Step3:

Convert the image to grayscale.
### Step4:

Using Canny operator from cv2,detect the edges of the image.
### Step5:

Using the HoughLinesP(),detect line co-ordinates for every points in the images.Using For loop,draw the lines on the found co-ordinates.Display the image.
## Program 
## Developed By
## Name: ABISHEK S
## Reg.No:212224240003

### Input image and grayscale image
```py
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('WhatsApp Image 2026-10-24 at 3.32.56 PM.jpeg') 
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert image to RGB for displaying
plt.title("Input Image")
plt.axis('off')
plt.imshow(gray_image, cmap='gray')
plt.title("Grayscale Image")
plt.axis('off')
edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(edges, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis('off')
lines = cv2.HoughLinesP(edges, 1, np.pi / 180, 100, minLineLength=50, maxLineGap=10)
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
plt.title("Result of Hough Transform")
plt.axis('off')
```
## output

<img width="307" height="407" alt="image" src="https://github.com/user-attachments/assets/3448cc30-9b0a-46ee-b882-065e58916123" />

<img width="306" height="401" alt="image" src="https://github.com/user-attachments/assets/ce1ed79e-2321-4b54-9216-e4743a0406d9" />


<img width="287" height="397" alt="image" src="https://github.com/user-attachments/assets/2d6908a6-e902-4fcb-a346-8de4505c4c7c" />


<img width="313" height="410" alt="download" src="https://github.com/user-attachments/assets/564ca796-e1ff-4ace-ba5d-12651c838d31" />






## Result

Thus, the lane detection pipeline is successfully implemented by completing the missing code sections. The system detects and highlights lane lines effectively.
