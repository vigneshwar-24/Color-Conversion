# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
STEP1:</br>
Read an image using imread() and Convert BGR and RGB to HSV and GRAY
using:
cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)

STEP2:</br>
Convert HSV to RGB and BGR
using:
cv2.cvtColor(image,cv2.COLOR_HSV2RGB)
cv2.cvtColor(image,cv2.COLOR_HSV2BGR)

STEP3:</br>
Convert RGB and BGR to YCrCb
using:
cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)

STEP4:</br>
Split and Merge RGB Image
using:
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.merge((blue,green,red))

STEP5:</br>
Split and merge HSV Image
using:
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)
cv2.merge((h,s,v))

## Program:
```python
# Developed By: Vigneshwar S
# Register Number: 212220230058

# i) Convert BGR and RGB to HSV and GRAY

import cv2
image=cv2.imread("rgb.jpg")
cv2.imshow("ORIGINAL IMAGE",image)
RGB_HSV=cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow("RGB_HSV_IMAGE",RGB_HSV)
RGB_GRAY=cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow("RGB_GRAY_IMAGE",RGB_GRAY)
BGR_HSV=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("BGR_HSV_IMAGE",BGR_HSV)
BGR_GRAY=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
cv2.imshow("BGR_GRAY_IMAGE",BGR_GRAY)
cv2.waitKey(0)


# ii)Convert HSV to RGB and BGR

hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("HSV_IMAGE",hsv)
HSV_RGB=cv2.cvtColor(hsv,cv2.COLOR_HSV2RGB)
cv2.imshow("HSV_RGB_IMAGE",HSV_RGB)
HSV_BGR=cv2.cvtColor(hsv,cv2.COLOR_HSV2BGR)
cv2.imshow("HSV_BGR_IMAGE",HSV_BGR)
cv2.waitKey(0)


# iii)Convert RGB and BGR to YCrCb

RGB_YCrCb=cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.imshow("RGB_YCrCb_IMAGE",RGB_YCrCb)
BGR_YCrCb=cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR_YCrCb_IMAGE",BGR_YCrCb)
cv2.waitKey(0)


# iv)Split and Merge RGB Image

blue = image[:,:,0]
cv2.imshow("blue",blue)
green = image[:,:,1]
cv2.imshow("green",green)
red = image[:,:,2]
cv2.imshow("red",red)
merged=cv2.merge((blue,green,red))
cv2.imshow("merged",merged)
cv2.waitKey(0)


# v) Split and merge HSV Image

hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("ORIGINAL HSV_IMAGE",hsv)
h, s, v = cv2.split(hsv)
cv2.imshow('h_plane', h)
cv2.imshow('s_plane', s)
cv2.imshow('v_plane', v)
mergedhsv=cv2.merge((h,s,v))
cv2.imshow('merged',mergedhsv)
cv2.waitKey(0)

```
## Output:
### i) BGR and RGB to HSV and GRAY
<img width="653" alt="1" src="https://user-images.githubusercontent.com/77089276/162581121-949c12a7-2f4b-488b-a9b9-882449bda508.PNG">

### ii) HSV to RGB and BGR
<img width="645" alt="2" src="https://user-images.githubusercontent.com/77089276/162581137-f5658745-ec8f-402d-815b-76a59d6e72a8.PNG">


### iii) RGB and BGR to YCrCb
<img width="450" alt="3" src="https://user-images.githubusercontent.com/77089276/162581143-cd951574-15ef-47c6-8df0-b2bb51d93f30.PNG">


### iv) Split and merge RGB Image
<img width="736" alt="4" src="https://user-images.githubusercontent.com/77089276/162581145-f23b6643-a6a3-4820-b862-340022936194.PNG">


### v) Split and merge HSV Image
<img width="678" alt="5" src="https://user-images.githubusercontent.com/77089276/162581151-dae40e63-3219-4b57-b4ce-8657f4a75ae3.PNG">



## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
