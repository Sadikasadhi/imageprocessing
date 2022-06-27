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
  i)Rotation<br>
  ii)Scalling<br>
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

8.Convert the original image to gray scale and then to binary.<br>
import cv2<br>
img=cv2.imread('flower8.jpg')<br>
cv2.imshow("RGB",img)<br>
cv2.waitKey(0)<br>

img=cv2.imread('flower8.jpg',0)<br>
cv2.imshow("Gray",img)<br>
cv2.waitKey(0)<br>

ret,bw_img=cv2.threshold(img,127,255,cv2.THRESH_BINARY)<br>
cv2.imshow("Binary",bw_img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>

OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97940468/175286167-3b9163ce-5da6-4d79-a5ce-bb0f45ba0194.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175286247-9f2aae70-3c27-4cff-99aa-7d10ff68cc00.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175286326-f094c78c-7324-4b62-a580-c3a423a193fb.png)<br>


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

10.Develop a program to readimage using URL.<br>
from skimage import io<br>
import matplotlib.pyplot as plt<br>
url='https://static.scientificamerican.com/sciam/cache/file/7A715AD8-449D-4B5A-ABA2C5D92D9B5A21_source.png'<br>
image=io.imread(url)<br>
plt.imshow(image)<br>
plt.show()<br>

OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97940468/175286697-288a374c-1ce3-42eb-b46d-dd8b7af57655.png)<br>

11.Write a program to mask and blur the image.<br>

import cv2<br>
import matplotlib.image as mpimg<br>
import matplotlib.pyplot as plt<br>
img=mpimg.imread('fish3.jpg')<br>
plt.imshow(img)<br>
plt.show<br>

![image](https://user-images.githubusercontent.com/97940468/175287049-e73ac905-438d-4e09-be74-0b294e4a5537.png)<br>

hsv_img = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)<br>
light_red=(0,50,50)<br>
dark_red=(10,255,255) <br>
mask_red=cv2.inRange(hsv_img,light_red,dark_red)<br>
result_red=cv2.bitwise_and(img,img,mask=mask_red)<br>
plt.subplot(1,2,1) <br>
plt.imshow(mask_red,cmap="gray")<br>
plt.subplot(1,2,2) <br>
plt.imshow(result_red) <br>
plt.show()<br>

![image](https://user-images.githubusercontent.com/97940468/175287148-f56dd729-715e-44ac-b69a-1fba8f8ea721.png)<br>

blur = cv2.GaussianBlur(result_red,(7,7),0)<br>
plt.imshow(blur)<br>
plt.show()<br>
![image](https://user-images.githubusercontent.com/97940468/175287229-ba480cfd-881a-4966-b366-8a7b2b682b44.png)<br>

12.Write a program to perform arithmatic operations on images<br>

import cv2<br>
import matplotlib.image as mpimg<br>
import matplotlib.pyplot as plt<br>

img1=cv2.imread('img1.jpg')<br>
img2=cv2.imread('img2.jpg')<br>

fimg1=img1 + img2<br>
plt.imshow(fimg1)<br>
plt.show()<br>

cv2.imwrite('output.jpg',fimg1)<br>
fimg2=img1 - img2<br>
plt.imshow(fimg2)<br>
plt.show()<br>

cv2.imwrite('output.jpg',fimg2)<br>
fimg3=img1 * img2<br>
plt.imshow(fimg3)<br>
plt.show()<br>

cv2.imwrite('output.jpg',fimg3)<br>
fimg4=img1 / img2<br>
plt.imshow(fimg4)<br>
plt.show()<br>

cv2.imwrite('output.jpg',fimg4)<br>

OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97940468/175287926-9c06ab99-d986-40fd-a2b3-94a9d2b13a4a.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175287982-07c3ef5d-9c04-4f61-ba4b-2e5ee01ec9e2.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175288054-58d7fb6e-d2a5-4f00-a704-f3e7011d9c4f.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175288101-d0c21143-2e9d-4e7c-8eff-353710cf0e73.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175288148-b4243125-9a61-401a-916d-7d995752aaaf.png)<br>

13.Develop the program to change the image to different color spaces.<br>
import cv2 <br>
img=cv2.imread("D:\Sadika\\b5.jpg")<br>
gray=cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)<br>
hsv=cv2.cvtColor(img,cv2.COLOR_BGR2HSV)<br>
lab=cv2.cvtColor(img,cv2.COLOR_BGR2LAB)<br>
hls=cv2.cvtColor(img,cv2.COLOR_BGR2HLS)<br>
yuv=cv2.cvtColor(img,cv2.COLOR_BGR2YUV)<br>
cv2.imshow("GRAY image",gray)<br>
cv2.imshow("HSV image",hsv)<br>
cv2.imshow("LAB image",lab)<br>
cv2.imshow("HLS image",hls)<br>
cv2.imshow("YUV image",yuv)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97940468/175288389-fe57e341-f802-4453-99ec-996a7d886b7d.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175288477-7e029aa7-e0bf-43c9-a6d6-d3f7f87aeb5f.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175288574-8676aa50-e3c3-4fdb-b00e-281a2602b6ea.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175288636-05a3c4ef-da1f-400e-9d9d-15dfca545267.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175288711-b4ba5977-c638-4d0f-8902-aabbaa4f9f6f.png)<br>

14.Program to create an image using 2D array<br>
import cv2 as c<br>
import numpy as np<br>
from PIL import Image<br>
array=np.zeros([100,200,3],dtype=np.uint8)<br>
array[:,:100]=[255,130,0]<br>
array[:,100:]=[0,0,255]<br>
img=Image.fromarray(array)<br>
img.save('IMAGES.jpg')<br>
img.show()<br>
c.waitKey(0)<br>

OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97940468/175289149-fdb3cf89-0c28-4a95-9ab5-914b202f0f3c.png)
<br>






