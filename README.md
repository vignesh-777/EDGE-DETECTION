# EDGE-DETECTION
### Name : vignesh R
### Reg No:212223240177
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## Program
```py
import cv2
import matplotlib.pyplot as plt

# READ THE IMAGE USING IMREAD
img = cv2.imread("tokyo.jpg")  # Replace with your image path

# CONVERT THE COLOR TO GRAY
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
gray = cv2.GaussianBlur(gray, (3, 3), 0)
```

```py


# SOBEL X
sobelx = cv2.Sobel(gray, cv2.CV_64F, 1, 0, ksize=5)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobelx, cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()

# SOBEL Y
sobely = cv2.Sobel(gray, cv2.CV_64F, 0, 1, ksize=5)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobely, cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()


# SOBEL XY
sobelxy = cv2.Sobel(gray, cv2.CV_64F, 1, 1, ksize=5)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobelxy, cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()

```
```py

# LAPLACIAN
lap = cv2.Laplacian(gray, cv2.CV_64F)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(lap, cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()

```
```

# CANNY EDGE DETECTOR
canny = cv2.Canny(gray, 120, 150)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(canny, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()

```
## Output:
### SOBEL EDGE DETECTOR
<img width="742" height="251" alt="image" src="https://github.com/user-attachments/assets/802ff997-6acf-46d7-ab73-48ae18fb65dc" />
<img width="735" height="264" alt="image" src="https://github.com/user-attachments/assets/b81b4cd6-c846-43d7-91a3-5c80cb49c2f3" />
<img width="733" height="253" alt="image" src="https://github.com/user-attachments/assets/390d5203-1445-46d6-9f9d-f75c796f76d6" />


### LAPLACIAN EDGE DETECTOR
<img width="744" height="253" alt="image" src="https://github.com/user-attachments/assets/1f418380-5a1a-4801-bcdc-fe22f6cf85de" />



### CANNY EDGE DETECTOR
<img width="775" height="275" alt="image" src="https://github.com/user-attachments/assets/aec54ee2-54b8-44d3-ac47-453910681788" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
