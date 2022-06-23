# imageprocessing

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
![image](https://user-images.githubusercontent.com/97940468/175268492-8cbcb325-a1c9-40dd-a5a5-ea696a0b13ee.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175268579-acb81aa2-9f08-425d-b17c-ef59a1799ac4.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175268651-d026fa2d-45ab-4156-a490-f1c10775f892.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175268751-90b8d7ee-ff00-45b5-a23c-45a0831a6a4f.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175268824-ad7ac3a1-6198-476c-a865-925252f0ae51.png)<br>
<br>



