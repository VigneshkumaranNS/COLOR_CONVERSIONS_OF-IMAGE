# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.
# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By:Vignesh Kumaran N S
### Register Number: 212222230171



### i) Read and display the image
```python
import cv2
import numpy as np
img=cv2.imread("spider.jpg")
cv2.imshow("window",img)
cv2.waitKey(0)
```
## Output:
<img src="https://github.com/VigneshkumaranNS/COLOR_CONVERSIONS_OF-IMAGE/assets/119484483/9886dc44-d7da-44cf-a0a3-026738bfd27f" width="300">
<br>
<br>

### ii)Write the image
```python
import cv2
img=cv2.imread('spider.jpg')
cv2.imwrite('noir.jpg',img)
```
## Output:
![2](https://github.com/VigneshkumaranNS/COLOR_CONVERSIONS_OF-IMAGE/assets/119484483/65fc5dfb-f889-4254-b194-49450e1a95cd)
<br>
<br>

### iii)Shape of the Image
```python
import cv2
img=cv2.imread('spider.jpg')
print(img.shape)
```
## Output:
![3](https://github.com/VigneshkumaranNS/COLOR_CONVERSIONS_OF-IMAGE/assets/119484483/b23c7c89-6292-456f-9fbd-bbdec58b9e02)
<br>
<br>

### iv)Access rows and columns
```python
import cv2
import random
img=cv2.imread('spider.jpg')
for i in range(150,200):
    for j in range(img.shape[1]):
        img[i][j]=[random.randint(0,255),
                  random.randint(0,255),
                  random.randint(0,255)]
cv2.imshow('img',img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
<img src="https://github.com/VigneshkumaranNS/COLOR_CONVERSIONS_OF-IMAGE/assets/119484483/cb809174-ebfd-45d4-81ca-3e398ab00b0a" width="300">
<br>
<br>

### v)Cut and paste portion of image
```python
import cv2
img=cv2.imread('spider.jpg')
tag=img[150:200,110:160]
img[110:160,150:200]=tag
cv2.imshow('noir1',img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
<img src="https://github.com/VigneshkumaranNS/COLOR_CONVERSIONS_OF-IMAGE/assets/119484483/3dbf19d2-3324-4867-882b-34d07dd55a10" width="300">
<br>
<br>

### vi) BGR and RGB to HSV and GRAY
```python
import cv2
img = cv2.imread('spider.jpg',1)
cv2.imshow('noir2',img)

hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)

gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)

gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
<img src="https://github.com/VigneshkumaranNS/COLOR_CONVERSIONS_OF-IMAGE/assets/119484483/07c0e96c-057b-4311-8efb-404abac71bdb" width="300">
<br>
<br>

### vii) HSV to RGB and BGR
```python
import cv2
img = cv2.imread('spider.jpg')

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![c2](https://github.com/VigneshkumaranNS/COLOR_CONVERSIONS_OF-IMAGE/assets/119484483/bb5bf2ec-e1d7-4366-b2b5-c8eb2a212a0b)
<br>
<br>

### viii) RGB and BGR to YCrCb
```python
import cv2
img = cv2.imread('spider.jpg')

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![c3](https://github.com/VigneshkumaranNS/COLOR_CONVERSIONS_OF-IMAGE/assets/119484483/3c476695-fd86-4efe-8616-3d306f2530ea)
<br>
<br>

### ix) Split and merge RGB Image
```python
import cv2
img = cv2.imread('spider.jpg')

R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
<img src="https://github.com/VigneshkumaranNS/COLOR_CONVERSIONS_OF-IMAGE/assets/119484483/63d5629f-5cc8-42fb-8efa-16d5e228fa4f" width="300">
<br>
<br>

### x) Split and merge HSV Image
```python
import cv2
img = cv2.imread("spider.jpg")
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
<img src="https://github.com/VigneshkumaranNS/COLOR_CONVERSIONS_OF-IMAGE/assets/119484483/a741e3be-8e97-40ef-964d-c0e177987d7e" width="300">
<br>
<br>

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.
