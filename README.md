# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import the necessary libraries and read two images, Color image and Gray Scale image.
### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.
### Step3:
Display the histograms with their respective images.
### Step4:

Equalize the grayscale image.
### Step5:
Display the grayscale image.

## Program:
```python
# Developed By: Sri Harish M
# Register Number:212220230047



# Write your code to find the histogram of gray scale image and color image channels.

import cv2
import matplotlib.pyplot as plt
Gray_image= cv2.imread('li.jpg')

Color_image= cv2.imread('li2.jpg') 
re=cv2.resize(Color_image,(280,175))
cv2.imshow('Gray image',Gray_image)

cv2.imshow ('colour image',re)
cv2.waitKey()



# Display the histogram of gray scale image and any one channel histogram from color image

hist  = cv2.calcHist([Gray_image], [0], None, [256], [0,256]) 
histl=cv2.calcHist([Color_image], [1], None, [256], [0,256]) 
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.title("grey image")
plt.show()

plt.stem(histl)
plt.title("color image")
plt.show()

# Write the code to perform histogram equalization of the image. 


import cv2
Gray_image=cv2.imread('li.jpg',0)
equ=cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()






```
## Output:
### Input Grayscale Image and Color Image


![k1](https://user-images.githubusercontent.com/75241366/165504061-3df8ecd6-ba53-4171-8417-07f9a2a31783.jpg)



### Histogram of Grayscale Image and any channel of Color Image

![k2](https://user-images.githubusercontent.com/75241366/165504079-f408072f-2b5f-4a08-981f-7136801c6f4f.jpg)

### Histogram Equalization of Grayscale Image
![k3](https://user-images.githubusercontent.com/75241366/165504101-7d2db662-64ed-4b06-a0c6-5c4b7e6d29e3.jpg)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
