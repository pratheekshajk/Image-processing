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
