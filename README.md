# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import cv2 and save and image as filename.jpg

### Step2:
Use imread(filename, flags) to read the file

### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:
Split and merge the image using cv2.split and cv2.merge commands.

### Step5:
End the program and close the output image windows.

## Program:
```python
# Developed By:Suji.G
# Register Number:212222230152

# i) Convert BGR and RGB to HSV and GRAY

import cv2
rick_color_image = cv2.imread('download.jpeg')
hsv_image = cv2.cvtColor(rick_color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV' ,hsv_image )
hsv_imagel = cv2.cvtColor(rick_color_image, cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV' , hsv_imagel)
gray_image = cv2.cvtColor(rick_color_image, cv2.COLOR_BGR2GRAY)
cv2.imshow( 'BGR2GRAY', gray_image)
gray_image1 = cv2.cvtColor (rick_color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()



# ii)Convert HSV to RGB and BGR

import cv2
rick_HSV_image = cv2.imread('download.jpeg')
RGB_image = cv2.cvtColor(rick_HSV_image,cv2.COLOR_HSV2RGB)
cv2.imshow('HSV to RGB',RGB_image )
BGR_image = cv2.cvtColor(rick_HSV_image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV to BGR',BGR_image)
cv2.waitKey(0)
cv2.destroyAllWindows()




# iii)Convert RGB and BGR to YCrCb

import cv2
rick_color_image = cv2.imread('download.jpeg')
YCrCb_image = cv2.cvtColor(rick_color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(rick_color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()


# iv)Split and Merge RGB Image

import cv2
image = cv2.imread('download.jpeg')
blue=image[:,:,0]
green=image[:,:,1]
red=image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()



# v) Split and merge HSV Image

import cv2
image=cv2.imread('download.jpeg')
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h,s,v=cv2.split(hsv)
cv2.imshow("Hue-image",h)
cv2.imshow("Saturation-image",s)
cv2.imshow("gray-image",v)
Merged_HSV=cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()



```
## Output:
### i) BGR and RGB to HSV and GRAY
![Screenshot from 2023-03-23 14-39-21](https://user-images.githubusercontent.com/119559822/227157567-7c485387-c96f-4fb8-93ca-e986de8450b7.png)

### ii) HSV to RGB and BGR
![Screenshot from 2023-03-23 14-38-11](https://user-images.githubusercontent.com/119559822/227157654-8ff78e46-25dc-4666-9479-cba490f17b95.png)


### iii) RGB and BGR to file:

![Screenshot from 2023-03-2 file:///home/sec/Pictures/Screenshots/Screenshot%20from%202023-03-23%2014-41-16.png


### iv) Split and merge RGB Image

![Screenshot from 2023-03-23 14-41-16](https://user-images.githubusercontent.com/119559822/227158018-cb7905f1-b49f-48aa-8de1-cb53186e2441.png)

### v) Split and merge HSV Image

![Screenshot from 2023-03-23 14-42-42](https://user-images.githubusercontent.com/119559822/227158099-51678c8d-8599-494b-9f1f-377ae46a1a37.png)

## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
