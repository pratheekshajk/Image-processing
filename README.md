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
![image](https://user-images.githubusercontent.com/72437208/104426450-f6982e80-55a7-11eb-9df3-2e58fa883d9c.png)
Rotation is 
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
