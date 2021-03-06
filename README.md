# Image-processing
1.Develp program to display grayscale image using read and write operation.
//gray scale image is the process of converting an image from other color space.
import numpy as np
import cv2
img = cv2.imread('nature.jpg',0)
cv2.imshow('Original',img,)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imwrite('graynature.jpg',img)
## output:
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
##  Output:
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
##  Output:
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
##  Output:
![image](https://user-images.githubusercontent.com/72437208/104432837-6bbb3200-55af-11eb-98d8-a15554b13a9d.png)
![image](https://user-images.githubusercontent.com/72437208/104433079-acb34680-55af-11eb-9b80-54c18aae2d01.png)

5.Develop program to given colour images to different colour space.
//Color spaces are a way to represent the color channels present in the image that gives the image that particular hue.There are several different color spaces and each has its own significance.color spaces are RGB (Red, Green, Blue), CMYK (Cyan, Magenta, Yellow, Black), HSV (Hue, Saturation, Value).
import cv2
img=cv2.imread('nature.jpg')
yuv_img = cv2.cvtColor(img, cv2.COLOR_BGR2YUV)
cv2.imshow('yuv image', yuv_img)
cv2.waitKey()
cv2.imshow('Y channel', yuv_img[:, :, 0])
cv2.imshow('U channel', yuv_img[:, :, 1])
cv2.imshow('V channel', yuv_img[:, :, 2])
cv2.waitKey()
hsv_img = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)
cv2.imshow('HSV image', hsv_img)
cv2.waitKey()
cv2.imshow('h channel',hsv_img[:,:,0])
cv2.imshow('s channel',hsv_img[:,:,1])
cv2.imshow('v channel',hsv_img[:,:,2])
cv2.waitKey()
##  Output: 
![image](https://user-images.githubusercontent.com/72437208/104434358-2435a580-55b1-11eb-8558-a8fb0094eb06.png)
![image](https://user-images.githubusercontent.com/72437208/104434643-75de3000-55b1-11eb-90a8-93555969233b.png)
![image](https://user-images.githubusercontent.com/72437208/104434791-aa51ec00-55b1-11eb-8a85-acd36d700804.png)
![image](https://user-images.githubusercontent.com/72437208/104435009-ea18d380-55b1-11eb-9b73-703a4b83f291.png)

6.Develop a program to create an images from 2D array.Generate array of random size.
// 2D array:Two dimensional array is an array within an array.It is the type of the array,the position of data element is reffered by two indices instead of one.
import numpy as np
from PIL import Image
array = np.linspace(0,1,200*220)
mat = np.reshape(array,(200,220))
img = Image.fromarray( mat , 'RGB')
img.show()
##  Output:
![image](https://user-images.githubusercontent.com/72437208/104435578-8f33ac00-55b2-11eb-8c20-e7d896f53481.png)

7.Develop a program to find the neighbors of each element in the matrix.
import numpy as np
i=0
j=0
a = np.array([[1,2,3,4,5,6,7],[7,6,5,4,3,2,1],[4,5,6,7,3,8,3],[2,3,4,5,6,7,8],[4,5,6,7,8,9,4]])
print('7x7 matrix is:\n', a)           
def neighbors(r, row, column):
     return [[a[i][j] if  i >= 0 and i < len(a) and j >= 0 and j < len(a[0]) else 0
                for j in range(column-1-r, column+r)]
                    for i in range(row-1-r, row+r)]
neighbors(2,2,2)

## Output:
![image](https://user-images.githubusercontent.com/72437208/104447021-39b2cb80-55c1-11eb-8cdb-1a4278cd407b.png)
 
8. Write a program to find sum of neighbors values in matrix.
import numpy as np
def sumNeighbors(M,x,y):
    l= []
    for i in range(max(0,x-1),x+2): 
        for j in range(max(0,y-1),y+2):
            try:
                t = M[i][j]
                l.append(t)
            except IndexError: 
                pass
    return sum(l)-M[x][y] 
M = [[1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]] 
M = np.asarray(M)
N = np.zeros(M.shape)
for i in range(M.shape[0]):
    for j in range(M.shape[1]):
        N[i][j] = sumNeighbors(M, i, j)
print("Original matrix:\n", M)
print("Summed neighbors matrix:\n", N)
Output:
![image](https://user-images.githubusercontent.com/72437208/104446795-f8bab700-55c0-11eb-9cde-16ee6db543be.png)

9. Write a C++ program to perform operator overloading.
#include <iostream>
using namespace std;
class TestClass {
private:
int count;
public:
TestClass() : count(5) {}
void operator --() {
count = count - 3;
}
void Display() {

cout << "Count: " << count; }
};

int main() {
TestClass tc;
--tc;
tc.Display();
return 0;
}
## Output:
count: 2

void operator ++():Overload the meaning of the ++ operator.
#include <iostream>  
#include <iostream>  
using namespace std;
class OperatorOverload {
private:
int x;
public:
OperatorOverload() : x(10) {}
void operator ++() {
x = x + 2;
}
void Print() {
cout << "The Count is: " << x;
}
};
int main() {
OperatorOverload ov;
++ov;  
ov.Print();
return 0;
}
## Output:
The count is: 12

10.Develop a program to implementation of negative transformation.
import cv2
import numpy as np
img=cv2.imread('nature.jpg')
cv2.imshow('nature.jpg',img)
print(img.dtype)
img_neg=255-img
cv2.imshow('negative',img_neg)
cv2.waitKey(0)
## Output:
![image](https://user-images.githubusercontent.com/72437208/105329502-3c33a780-5bf7-11eb-9b69-cfa2e757ac63.png)
![image](https://user-images.githubusercontent.com/72437208/105329752-8157d980-5bf7-11eb-9ad0-b661768f0021.png)

11. Develop a program to implementation of contrast transformation.
from PIL import Image, ImageEnhance 
im = Image.open('nature.jpg') 
im3 = ImageEnhance.Color(im) 
im3.enhance(2.0).show()   
## output:
![image](https://user-images.githubusercontent.com/72437208/105329502-3c33a780-5bf7-11eb-9b69-cfa2e757ac63.png)
![image](https://user-images.githubusercontent.com/72437208/105330492-5c179b00-5bf8-11eb-83d9-a7b51310b406.png)

12. Develop a program to implementation of threshold images.
import cv2  
import numpy as np  
img= cv2.imread('nature.jpg')  
ret, thresh1 = cv2.threshold(img, 120, 255, cv2.THRESH_BINARY) 
ret, thresh2 = cv2.threshold(img, 120, 255, cv2.THRESH_BINARY_INV) 
ret, thresh3 = cv2.threshold(img, 120, 255, cv2.THRESH_TRUNC) 
ret, thresh4 = cv2.threshold(img, 120, 255, cv2.THRESH_TOZERO) 
ret, thresh5 = cv2.threshold(img, 120, 255, cv2.THRESH_TOZERO_INV) 
cv2.imshow('Binary Threshold', thresh1) 
cv2.imshow('Binary Threshold Inverted', thresh2) 
cv2.imshow('Truncated Threshold', thresh3) 
cv2.imshow('Set to 0', thresh4) 
cv2.imshow('Set to 0 Inverted', thresh5) 
cv2.waitKey(0) 
cv2.destroyAllWindows()
## output:
![image](https://user-images.githubusercontent.com/72437208/105331231-36d75c80-5bf9-11eb-8e0a-436f84d46a30.png)
![image](https://user-images.githubusercontent.com/72437208/105331418-700fcc80-5bf9-11eb-9a1b-1f00fab92a60.png)

13.Develop program to power law(Gamma) transformation.
import cv2 
import numpy as np 
img = cv2.imread('nature.jpg') 
for gamma in [0.1,0.5,1.2,2.2]: 
    gamma_corrected = np.array(255*(img / 255) ** gamma, dtype = 'uint8') 
    cv2.imshow('gamma_transformed'+str(gamma)+'.jpg', gamma_corrected) 
cv2.waitKey(0)                                                                   
## Output:
![image](https://user-images.githubusercontent.com/72437208/105331880-fb895d80-5bf9-11eb-8c84-2669f9e023c5.png)




