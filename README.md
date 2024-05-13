# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import cv2 and matplotlib.pyplot
<br>

### Step2:
Read and display the input images
<br>

### Step3:
Calculate the Histogram Values using calcHist()
<br>

### Step4:
Display the histograms
<br>

### Step5:
Calculate and display the equalized image using equalizeHist()
<br>

## Program:
```
# Developed By: Bairav skandan Loha
# Register Number: 212222230110

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("ajith 2.jpg")
color_image = cv2.imread("thalapathy-vijay.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

import cv2
Gray_image = cv2.imread("ajith 2.jpg")
Color_image = cv2.imread("thalapathy-vijay.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()

plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)

import cv2
gray_image = cv2.imread("ajith 2.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image
Gray Scale Image
![gray scale img1.jpg](https://github.com/Bairav-2003/Histogram-of-an-images/blob/main/gray%20scale%20img.jpg)

Color Image
![color img.jpg](https://github.com/Bairav-2003/Histogram-of-an-images/blob/main/color%20img.jpg)

<br>

### Histogram of Grayscale Image and any channel of Color Image
Gray Scale Image
![histogram.png](https://github.com/Bairav-2003/Histogram-of-an-images/blob/main/histogram.png)

Color Image
![color scale.png](https://github.com/Bairav-2003/Histogram-of-an-images/blob/main/color%20scale.png)

<br>

### Histogram Equalization of Grayscale Image

Original Image

![gray scale img1.jpg](https://github.com/Bairav-2003/Histogram-of-an-images/blob/main/gray%20scale%20img1.jpg)

Equalized Image

![eq gray img.jpg](https://github.com/Bairav-2003/Histogram-of-an-images/blob/main/eq%20gray%20img.jpg)

<br>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
