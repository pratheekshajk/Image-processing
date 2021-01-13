# Image-processing
1.Develp program to display grayscale image using read and write operation.

import numpy as np
import cv2
img = cv2.imread('nature.jpg',0)
cv2.imshow('Original',img,)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imwrite('graynature.jpg',img)
output:
![image](https://user-images.githubusercontent.com/72437208/104428673-c43c0080-55aa-11eb-832e-b04d75df9e75.png)
![image](https://user-images.githubusercontent.com/72437208/104424592-94d6c500-55a5-11eb-9db9-35ccfad4e4cd.png)
2.Develop a program to perform linear transformation on image.
// scaling is the process of resizing a digital images.
Scaling:
import cv2
import numpy as np
src=cv2.imread('nature.jpg',1)
img=cv2.imshow('nature.jpg',src)
scale_p=500
width=int(src.shape[1]*scale_p/100)
height=int(src.shape[0]*scale_p/100)
dsize=(width,height)
result=cv2.resize(src,dsize)
cv2.imwrite('scaling.jpg',result)
cv2.imshow('scaling.jpg',result)
cv2.waitKey(0)
Output:
![image](https://user-images.githubusercontent.com/72437208/104428673-c43c0080-55aa-11eb-832e-b04d75df9e75.png)
![image](https://user-images.githubusercontent.com/72437208/104426450-f6982e80-55a7-11eb-9df3-2e58fa883d9c.png)
Rotation is convert images one coordinate to another.
Rotation:
import cv2
import numpy as np
src=cv2.imread('nature.jpg')
img=cv2.imshow('nature.jpg',src)
windowsname='image'
image=cv2.rotate(src,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow(windowsname,image)
cv2.waitKey(0)
Output:
![image](https://user-images.githubusercontent.com/72437208/104428673-c43c0080-55aa-11eb-832e-b04d75df9e75.png)
![image](https://user-images.githubusercontent.com/72437208/104427222-006e6180-55a9-11eb-95f2-4a8108d2a254.png)
3.Develop a program to find sum and mean of multiple images.
// Create a folder and store images.Read all images and perform sum and mean of images.
import cv2 
import os
path='C:\pyth'
img=[]
files=os.listdir(path)
for file in files:
    fpath=path+"\\"+file
    img.append(cv2.imread(fpath))
i=0
im=[]
for im in img:
    im+=img[i]
    i=i+1
cv2.imshow("sum",im)
mean=im/len(files)
cv2.imshow("mean",mean)
cv2.waitKey(0)
Output:
![image](https://user-images.githubusercontent.com/72437208/104429879-17fb1980-55ac-11eb-9c95-d2579bbd2eb8.png)
![image](https://user-images.githubusercontent.com/72437208/104430224-6ad4d100-55ac-11eb-8896-7d1a259674ae.png)
4.Convert images grayscale and binary image.
// gray scale image is the process of converting an image from other color space.
// binary images is type of image where each pixel is black or white.where 0 represent black and 1 represent white.
import numpy as np
import cv2
img = cv2.imread('nature.jpg',0)
cv2.imshow('Original',img)
cv2.imwrite('graynature.jpg',img)
img = cv2.imread('nature.jpg', 2) 
ret, bw_img = cv2.threshold(img, 127, 255, cv2.THRESH_BINARY) 
cv2.imshow("Binary", bw_img) 
cv2.waitKey(0)
cv2.destroyAllWindows()
Output:
![image](https://user-images.githubusercontent.com/72437208/104432837-6bbb3200-55af-11eb-98d8-a15554b13a9d.png)
![image](https://user-images.githubusercontent.com/72437208/104433079-acb34680-55af-11eb-9b80-54c18aae2d01.png)
