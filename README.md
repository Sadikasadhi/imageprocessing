# imageprocessing

1.Develop a program to display grayscale image using read and Write Operations.
<br>
OUTPUT:
![image](https://user-images.githubusercontent.com/97940468/175270926-d16f09bc-6f52-4e13-8315-2f468bbe937d.png)

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
![image](https://user-images.githubusercontent.com/97940468/175270255-9781d7c8-506a-450f-9698-5488ab11fb18.png)

<br>



