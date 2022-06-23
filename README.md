# imageprocessing

1.Develop a program to display grayscale image using read and Write Operations.
<br>
import cv2 <br>
img=cv2.imread('flower4.jpg',0) <br>
cv2.imshow('image',img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97940468/175270926-d16f09bc-6f52-4e13-8315-2f468bbe937d.png)
<br>
2.Develop a program to display the image using matplotlib.<br>
import matplotlib.image as mping <br>
import matplotlib.pyplot as plt <br>
img=mping.imread('rose2.jpg') <br>
plt.imshow(img) <br>
OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97940468/175273562-5e5c9e46-c75a-424f-9831-ced1e9dc57bf.png)
<br>
3.Develop a program to perform linear transformation.
  Rotation<br>
  Scalling<br>
import cv2<br>
from PIL import Image<br>
img=Image.open('leaf1.jpg')<br>
img=img.rotate(180)<br>
img.show()<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
OUTPUT:<br>  
  ![image](https://user-images.githubusercontent.com/97940468/175281528-ae192b0c-596f-4194-942d-1dc6c92e8366.png)
<br>
Develop the program to change the image to different color spaces
<br>

import cv2 
img=cv2.imread("D:\Sadika\\b5.jpg")
gray=cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
hsv=cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
lab=cv2.cvtColor(img,cv2.COLOR_BGR2LAB)
hls=cv2.cvtColor(img,cv2.COLOR_BGR2HLS)
yuv=cv2.cvtColor(img,cv2.COLOR_BGR2YUV)
cv2.imshow("GRAY image",gray)
cv2.imshow("HSV image",hsv)
cv2.imshow("LAB image",lab)
cv2.imshow("HLS image",hls)
cv2.imshow("YUV image",yuv)
cv2.waitKey(0)
cv2.destroyAllWindows()

<br>
OUTPUT:
<br>
![image](https://user-images.githubusercontent.com/97940468/175271468-3b8c4b20-b1d4-4078-8bef-cf8f31661187.png)


<br>



