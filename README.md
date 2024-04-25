# EDGE-DETECTION
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
## PROGRAM:
```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("bouq.png",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```

## SOBEL EDGE DETECTOR
## i) SOBEL X AXIS
```python
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```

## ii) SOBEL Y AXIS
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
## iii) SOBEL XY AXIS
```python
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```

### LAPLACIAN EDGE DETECTOR
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```

### CANNY EDGE DETECTOR
```python
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## Output:
### SOBEL EDGE DETECTOR
## i) SOBEL X AXIS

<img width="305" alt="image" src="https://github.com/TejaswiniGugananthan/EDGE-DETECTION/assets/121222763/f7a8bf7e-ba27-4ad8-985c-ee2b19507491">


## ii) SOBEL Y AXIS

<img width="305" alt="image" src="https://github.com/TejaswiniGugananthan/EDGE-DETECTION/assets/121222763/cd86e549-4474-4387-bede-55e54ceef952">


## iii) SOBEL XY AXIS

<img width="301" alt="image" src="https://github.com/TejaswiniGugananthan/EDGE-DETECTION/assets/121222763/1f91ab8e-e0cd-4397-94ac-22df1d8cb93a">


### LAPLACIAN EDGE DETECTOR

<img width="301" alt="image" src="https://github.com/TejaswiniGugananthan/EDGE-DETECTION/assets/121222763/c1115a4d-0cdf-4d59-93fb-1da2495447f9">


### CANNY EDGE DETECTOR

<img width="301" alt="image" src="https://github.com/TejaswiniGugananthan/EDGE-DETECTION/assets/121222763/744c32d9-1e23-4ea1-8d06-988d5779fcdd">


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
