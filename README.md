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
3.Develop a program to perform linear transformation.<br>
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

4.Develop a program to convert color string to RGB color values.<br>

from PIL import ImageColor<br>
img1=ImageColor.getrgb("yellow")<br>
print(img1)<br>
img2=ImageColor.getrgb("red")<br>
print(img2)<br>
img1=ImageColor.getrgb("pink")<br>
print(img3)<br>
OUTPUT:<br>
(255, 255, 0)<br>
(255, 0, 0)<br>
(255, 192, 203)<br>

5.Write a program to create image using colors spaces.<br>
from PIL import Image<br>
img=Image.new('RGB',(200,400),(255,255,0))<br>
img.show()<br>
OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97940468/175282545-c9b75b06-2c7a-40e6-bd65-fa6ca2d6a367.png)<br>


6.Develop a program to visualize the image using various color.<br>

import cv2<br>
import matplotlib.pyplot as plt<br>
import numpy as np<br>
img=cv2.imread('plant4.jpg')<br>
plt.imshow(img)<br>
plt.show()<br>
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)<br>
plt.imshow(img)<br>
plt.show()<br>
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)<br>
plt.imshow(img)<br>
plt.show()<br>
OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97940468/175283104-5976774f-6924-4746-b8f3-1f1f0983a008.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175283186-7b30852a-5485-465f-a252-c3f71be403bb.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175283262-28553f7f-dbd8-4948-99ff-72743aacf5e1.png)<br>

7.Write a program to display the image attributes.<br>

from PIL import Image<br>
image=Image.open('plant4.jpg')<br>
print("Filename:",image.filename)<br>
print("Format:",image.format)<br>
print("Mode:",image.mode)<br>
print("size:",image.size)<br>
print("Width:",image.width)<br>
print("Height:",image.height)<br>
image.close()<br>

OUTPUT:<br>
Filename: plant4.jpg<br>
Format: JPEG<br>
Mode: RGB<br>
size: (259, 194)<br>
Width: 259<br>
Height: 194<br>

8.Convert the original image to gray scale and then to binary.


9.Resize the original image<br>
import cv2<br>
img=cv2.imread('b1.jpg')<br>
print('original image length width',img.shape)<br>
cv2.imshow('original image',img)<br>
cv2.waitKey(0)<br>

imgresize=cv2.resize(img,(150,160))<br>
cv2.imshow('Resized image',imgresize)<br>
print('Resized image length,width',imgresize.shape)<br>
cv2.waitKey(0)<br>

OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97940468/175284242-e0f0835d-e45b-414e-84c9-ece1d5ba5e72.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175284048-d800dc17-2246-4548-851a-ac4e893ddd71.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175284124-9a6f913a-fe6a-430a-9e90-acfcdec884fb.png)<br>

















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



