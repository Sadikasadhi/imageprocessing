
# imageprocessing

**1.Develop a program to display grayscale image using read and Write Operations.**
<br>
import cv2 <br>
img=cv2.imread('flower4.jpg',0) <br>
cv2.imshow('image',img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
**OUTPUT:<br>**
![image](https://user-images.githubusercontent.com/97940468/175270926-d16f09bc-6f52-4e13-8315-2f468bbe937d.png)
<br>
**2.Develop a program to display the image using matplotlib.<br>**
import matplotlib.image as mping <br>
import matplotlib.pyplot as plt <br>
img=mping.imread('rose2.jpg') <br>
plt.imshow(img) <br>
**OUTPUT:<br>**
![image](https://user-images.githubusercontent.com/97940468/175273562-5e5c9e46-c75a-424f-9831-ced1e9dc57bf.png)
<br>
**3.Develop a program to perform linear transformation.<br>
    i)Rotation<br>
    ii)Scalling<br>**
import cv2<br>
from PIL import Image<br>
img=Image.open('leaf1.jpg')<br>
img=img.rotate(180)<br>
img.show()<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
**OUTPUT:<br>**  
  ![image](https://user-images.githubusercontent.com/97940468/175281528-ae192b0c-596f-4194-942d-1dc6c92e8366.png)
<br>




**4.Develop a program to convert color string to RGB color values.<br>**

from PIL import ImageColor<br>
img1=ImageColor.getrgb("yellow")<br>
print(img1)<br>
img2=ImageColor.getrgb("red")<br>
print(img2)<br>
img3=ImageColor.getrgb("pink")<br>
print(img3)<br>
**OUTPUT:<br>**
(255, 255, 0)<br>
(255, 0, 0)<br>
(255, 192, 203)<br>

**5.Write a program to create image using colors spaces.<br>**
from PIL import Image<br>
img=Image.new('RGB',(200,400),(255,255,0))<br>
img.show()<br>
**OUTPUT:<br>**
![image](https://user-images.githubusercontent.com/97940468/175282545-c9b75b06-2c7a-40e6-bd65-fa6ca2d6a367.png)<br>


**6.Develop a program to visualize the image using various color.<br>**

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
**OUTPUT:<br>**
![image](https://user-images.githubusercontent.com/97940468/175283104-5976774f-6924-4746-b8f3-1f1f0983a008.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175283186-7b30852a-5485-465f-a252-c3f71be403bb.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175283262-28553f7f-dbd8-4948-99ff-72743aacf5e1.png)<br>

**7.Write a program to display the image attributes.<br>**

from PIL import Image<br>
image=Image.open('plant4.jpg')<br>
print("Filename:",image.filename)<br>
print("Format:",image.format)<br>
print("Mode:",image.mode)<br>
print("size:",image.size)<br>
print("Width:",image.width)<br>
print("Height:",image.height)<br>
image.close()<br>

**OUTPUT:<br>**
Filename: plant4.jpg<br>
Format: JPEG<br>
Mode: RGB<br>
size: (259, 194)<br>
Width: 259<br>
Height: 194<br>

**8.Convert the original image to gray scale and then to binary.<br>**
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

**OUTPUT:<br>**
![image](https://user-images.githubusercontent.com/97940468/175286167-3b9163ce-5da6-4d79-a5ce-bb0f45ba0194.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175286247-9f2aae70-3c27-4cff-99aa-7d10ff68cc00.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175286326-f094c78c-7324-4b62-a580-c3a423a193fb.png)<br>


**9.Resize the original image<br>**
import cv2<br>
img=cv2.imread('b1.jpg')<br>
print('original image length width',img.shape)<br>
cv2.imshow('original image',img)<br>
cv2.waitKey(0)<br>

imgresize=cv2.resize(img,(150,160))<br>
cv2.imshow('Resized image',imgresize)<br>
print('Resized image length,width',imgresize.shape)<br>
cv2.waitKey(0)<br>

**OUTPUT:<br>**
![image](https://user-images.githubusercontent.com/97940468/175284242-e0f0835d-e45b-414e-84c9-ece1d5ba5e72.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175284048-d800dc17-2246-4548-851a-ac4e893ddd71.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175284124-9a6f913a-fe6a-430a-9e90-acfcdec884fb.png)<br>

**10.Develop a program to readimage using URL.<br>**
from skimage import io<br>
import matplotlib.pyplot as plt<br>
url='https://static.scientificamerican.com/sciam/cache/file/7A715AD8-449D-4B5A-ABA2C5D92D9B5A21_source.png'<br>
image=io.imread(url)<br>
plt.imshow(image)<br>
plt.show()<br>

**OUTPUT:<br>**
![image](https://user-images.githubusercontent.com/97940468/175286697-288a374c-1ce3-42eb-b46d-dd8b7af57655.png)<br>

**11.Write a program to mask and blur the image.<br>**

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

import cv2<br>
import matplotlib.image as mpimg<br>
import matplotlib.pyplot as plt<br>
img=mpimg.imread('fish1.jpg')<br>
plt.imshow(img)<br>
plt.show<br>

![image](https://user-images.githubusercontent.com/97940468/176416594-caaaec6e-9201-4d73-917c-f34d19c5e607.png)<br>

hsv_img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)<br>
light_orange=(1, 190, 200)<br>
dark_orange=(18, 255, 255)<br>
mask=cv2.inRange(hsv_img,light_orange,dark_orange)<br>
result=cv2.bitwise_and(img,img,mask=mask)<br>
plt.subplot(1,2,1)<br>
plt.imshow(mask,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(result)<br>
plt.show()<br>

![image](https://user-images.githubusercontent.com/97940468/176416791-791b03e0-da40-41ab-b044-598d1e66ffe4.png)<br>

light_white=(0,0,200)<br>
dark_white=(145,60,255)<br>
mask_white=cv2.inRange(hsv_img,light_white,dark_white)<br>
result_white=cv2.bitwise_and(img,img,mask=mask_white)<br>
plt.subplot(1,2,1)<br>
plt.imshow(mask_white,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(result_white)<br>
plt.show()<br>

![image](https://user-images.githubusercontent.com/97940468/176417006-9b1f7165-9283-4a6a-abc8-1409253b673f.png)<br>


final_mask=mask+mask_white<br>
final_result=cv2.bitwise_and(img,img,mask=final_mask)<br>
plt.subplot(1,2,1)<br>
plt.imshow(final_mask,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(final_result)<br>
plt.show()<br>
![image](https://user-images.githubusercontent.com/97940468/176417318-049d8929-cc68-4b45-a3d0-2f3cfc88796b.png)<br>

blur=cv2.GaussianBlur(final_result, (7,7), 0)<br>
plt.imshow(blur)<br>
plt.show()<br>
![image](https://user-images.githubusercontent.com/97940468/176417476-f22f4164-c72c-48f1-9d95-8c0b70bdee8e.png)<br>

**12.Write a program to perform arithmatic operations on images<br>**

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

**OUTPUT:<br>**
![image](https://user-images.githubusercontent.com/97940468/175287926-9c06ab99-d986-40fd-a2b3-94a9d2b13a4a.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175287982-07c3ef5d-9c04-4f61-ba4b-2e5ee01ec9e2.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175288054-58d7fb6e-d2a5-4f00-a704-f3e7011d9c4f.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175288101-d0c21143-2e9d-4e7c-8eff-353710cf0e73.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175288148-b4243125-9a61-401a-916d-7d995752aaaf.png)<br>

**13.Develop the program to change the image to different color spaces.<br>**
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
**OUTPUT:<br>**
![image](https://user-images.githubusercontent.com/97940468/175288389-fe57e341-f802-4453-99ec-996a7d886b7d.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175288477-7e029aa7-e0bf-43c9-a6d6-d3f7f87aeb5f.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175288574-8676aa50-e3c3-4fdb-b00e-281a2602b6ea.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175288636-05a3c4ef-da1f-400e-9d9d-15dfca545267.png)<br>
![image](https://user-images.githubusercontent.com/97940468/175288711-b4ba5977-c638-4d0f-8902-aabbaa4f9f6f.png)<br>

**14.Program to create an image using 2D array<br>**
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

**OUTPUT:<br>**
![image](https://user-images.githubusercontent.com/97940468/175289149-fdb3cf89-0c28-4a95-9ab5-914b202f0f3c.png)
<br>

**15.Bitwise operation<br>**

import cv2<br>
import matplotlib.pyplot as plt<br>
image1=cv2.imread('img1.jpg',1)<br>
image2=cv2.imread('img1.jpg')<br>
ax=plt.subplots(figsize=(15,10))<br>
bitwiseAnd=cv2.bitwise_and(image1,image2)<br>
bitwiseOr=cv2.bitwise_or(image1,image2)<br>
bitwiseXor=cv2.bitwise_xor(image1,image2)<br>
bitwiseNot_img1=cv2.bitwise_not(image1)<br>
bitwiseNot_img2=cv2.bitwise_not(image2)<br>
plt.subplot(151)<br>
plt.imshow(bitwiseAnd)<br>
plt.subplot(152)<br>
plt.imshow(bitwiseOr)<br>
plt.subplot(153)<br>
plt.imshow(bitwiseXor)<br>
plt.subplot(154)<br>
plt.imshow(bitwiseNot_img1)<br>
plt.subplot(155)<br>
plt.imshow(bitwiseNot_img2)<br>
cv2.waitKey(0)<br>

**OUTPUT:<br>**
![image](https://user-images.githubusercontent.com/97940468/176419008-19206b9b-a161-431d-9ce5-1c88c18e797b.png)<br>

**16.Blurring image<br>**
#importing libraries<br>
import cv2<br>
import numpy as np<br>

image=cv2.imread('b7.jpg')<br>

cv2.imshow('Original Image',image)<br>
cv2.waitKey(0)<br>

#Gaussian Blur<br>
Gaussian=cv2.GaussianBlur(image,(7,7),0)<br>
cv2.imshow('Gaussian Blurring', Gaussian)<br>
cv2.waitKey(0)<br>

#Median Blur<br>
median=cv2.medianBlur(image,5)<br>
cv2.imshow('Median Blurring' ,median)<br>
cv2.waitKey(0)<br>

#Bilateral Blur<br>
bilateral=cv2.bilateralFilter(image,9,75,75)<br>
cv2.imshow('Bilateral Blurring', bilateral)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>

**OUTPUT:<br>**
![image](https://user-images.githubusercontent.com/97940468/176420151-9f7928c9-60ca-4526-8120-bb04cff1ef5e.png)<br>
![image](https://user-images.githubusercontent.com/97940468/176420227-a9dfe559-061c-4534-a65f-5bfcb96bd742.png)<br>
![image](https://user-images.githubusercontent.com/97940468/176420312-3aeb1a7d-dc64-4ab3-b196-b68338cebc67.png)<br>
![image](https://user-images.githubusercontent.com/97940468/176420403-c19ed3e8-c9eb-4e61-a259-d82ee11414dc.png)<br>

**17.Image Enhancement<br>**
from PIL import Image<br>
from PIL import ImageEnhance<br>
image=Image.open('b3.jpg')<br>
image.show()<br>
enh_bri=ImageEnhance.Brightness(image)<br>
brightness=1.5<br>
image_brightened=enh_bri.enhance(brightness)<br>
image_brightened.show()<br>

enh_col=ImageEnhance.Color(image)<br>
color=1.5<br>
image_colored=enh_col.enhance(color)<br>
image_colored.show()<br>

enh_con=ImageEnhance.Contrast(image)<br>
contrast=1.5<br>
image_contrasted=enh_con.enhance(contrast)<br>
image_contrasted.show()<br>

enh_sha=ImageEnhance.Sharpness(image)<br>
sharpness=1.5<br>
image_sharped=enh_sha.enhance(sharpness)<br>
image_sharped.show()<br>

**OUTPUT:<br>**
![image](https://user-images.githubusercontent.com/97940468/176421932-cd752748-2da1-4b34-a373-b8d56a20e41d.png)<br>
![image](https://user-images.githubusercontent.com/97940468/176422016-69116b56-d65d-4527-a249-a3981cd0b9dc.png)<br>
![image](https://user-images.githubusercontent.com/97940468/176422099-b9e724b6-db0c-49df-8bfd-5406447f95a1.png)<br>
![image](https://user-images.githubusercontent.com/97940468/176422146-e4dc626f-dd73-4d76-bc54-18d2e786a19e.png)<br>
![image](https://user-images.githubusercontent.com/97940468/176422212-8439e466-fc9d-41fa-b526-f3c753eeabfb.png)<br>

**18.Morpholigical operation<br>**
import cv2<br>
import numpy as np<br>
from  matplotlib import pyplot as plt<br>
from PIL import  Image,ImageEnhance<br>
img=cv2.imread('b2.jpg',0)<br>
ax=plt.subplots(figsize=(15,10))<br>
kernel=np.ones((5,5),np.uint8)<br>
opening=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)<br>
closing=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)<br>
erosion=cv2.erode(img,kernel,iterations=1)<br>
dilation=cv2.dilate(img,kernel,iterations=1)<br>
gradient=cv2.morphologyEx(img,cv2.MORPH_GRADIENT,kernel)<br>
plt.subplot(151)<br>
plt.imshow(opening)<br>
plt.subplot(152)
plt.imshow(closing)<br>
plt.subplot(153)<br>
plt.imshow(erosion)<br>
plt.subplot(154)<br>
plt.imshow(dilation)<br>
plt.subplot(155)<br>
plt.imshow(gradient)<br>
cv2.waitKey(0)<br>

**OUTPUT:<br>**
![image](https://user-images.githubusercontent.com/97940468/176422537-45e6c945-f524-43fd-a476-0a850bdf1131.png)<br>

**19.Develop a program to<br>
    i)Read the image,convert it into grayscale image<br>
    ii)Write(save) the grayscale image and<br>
    iii)Display the original image and grayscale image<br>**

import cv2<br>
OriginalImg=cv2.imread('j1.jpg')<br>
GrayImg=cv2.imread('j1.jpg',0)<br>
isSaved=cv2.imwrite('C:\Sadhi\img2.jpg',GrayImg)<br>
cv2.imshow('Display original Image',OriginalImg)<br>
cv2.imshow('Display Grayscale Image',GrayImg)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
if isSaved:<br>
    print('The image is successfully saved!')<br>

**OUTPUT:<br>**

![image](https://user-images.githubusercontent.com/97940468/179492874-d57f75a7-f995-49db-8c0f-f2ba288bcb0d.png)<br>
![image](https://user-images.githubusercontent.com/97940468/179493032-60de268e-78ea-42f4-8c78-eab354701b7d.png)<br>

**The Image Is Successfully saved<br>**

![image](https://user-images.githubusercontent.com/97940468/180201210-66107bfa-e52c-40c5-bb58-ccbf098b0fdd.png)<br>


**20.Slicing with background<br>**
import cv2<br>
import numpy as np<br>
from matplotlib import pyplot as plt<br>
image=cv2.imread('c2.jpg',0)<br>
x,y=image.shape<br>
z=np.zeros((x,y))<br>
for i in range(0,x):<br>
    for j in range(0,y):<br>
        if(image[i][j]>50 and image[i][j]<150):<br>
            z[i][j]=255<br>
        else:<br>
            z[i][j]=image[i][j]<br>
equ=np.hstack((image,z))<br>
plt.title('Graylevel slicing with background')<br>
plt.imshow(equ,'gray')<br>
plt.show()<br>

**OUTPUT:<br>**
![image](https://user-images.githubusercontent.com/97940468/178711799-4a52d336-dc84-4bef-a33f-97dbd80dae4e.png)<br>

**21.Slicing without background<br>**

import cv2<br>
import numpy as np<br>
from matplotlib import pyplot as plt<br>
image=cv2.imread('c2.jpg',0)<br>
x,y=image.shape<br>
z=np.zeros((x,y))<br>
for i in range(0,x):<br>
    for j in range(0,y):<br>
        if(image[i][j]>50 and image[i][j]<150):<br>
            z[i][j]=255<br>
        else:<br>
            z[i][j]=0<br>
equ=np.hstack((image,z))<br>
plt.title('Graylevel slicing without background')<br>
plt.imshow(equ,'gray')<br>
plt.show()<br>

**OUTPUT:<br>**
![image](https://user-images.githubusercontent.com/97940468/178712077-d0c20b0d-3838-40ab-8b50-cba46fabc6e8.png)<br>


**22.Analyze the image using Histogram <br>**
import numpy as np<br>
import skimage.color<br>
import skimage.io<br>
import matplotlib.pyplot as plt<br>

#read the image of a plant seedling as grayscale from the outset<br>
image = skimage.io.imread(fname="t1.jpg",as_gray=True)<br>
image1 = skimage.io.imread(fname="t1.jpg")<br>

#display the image<br>
fig, ax = plt.subplots()<br>
plt.imshow(image, cmap="gray")<br>
plt.show()<br>

fig, ax = plt.subplots()<br>
plt.imshow(image1,cmap="gray")<br>
plt.show()<br>

#create the histogram<br>
histogram, bin_edges = np.histogram(image, bins=256, range=(0, 1))<br>

#configure and draw the histogram figure<br>
plt.figure()<br>
plt.title("Grayscale Histogram")<br>
plt.xlabel("grayscale value")<br>
plt.ylabel("pixel count")<br>
plt.xlim([0.0, 1.0]) # <- named arguments do not work here<br>

plt.plot(bin_edges[0:-1], histogram) # <- or here<br>
plt.show()<br>

**OUTPUT:<br>**
![image](https://user-images.githubusercontent.com/97940468/179490709-c8fd0eca-a230-4ac3-bc20-51c6ade884e7.png)<br>
![image](https://user-images.githubusercontent.com/97940468/179490756-2a45bb68-9d37-41af-98ac-721df830a1df.png)<br>
![image](https://user-images.githubusercontent.com/97940468/179490855-4a364c5e-91c2-4037-9cb5-6457163a7d00.png)<br>

**23. Program to perform basic image data analysis using intensity transformation:<br>
    a) Image negative<br>
    b) Log transformation<br>
    c) Gamma correction<br>**
    
#%matplotlib inline<br>
import imageio<br>
import matplotlib.pyplot as plt<br>
#import warnings<br>
#import matplotlib.cbook<br>
#warnings.filterwarnings("ignore",category=matplotlib.cbook.mplDeprecation)<br>
pic=imageio.imread('c5.jpg')<br>
plt.figure(figsize=(6,6))<br>
plt.imshow(pic);<br>
plt.axis('off');<br>

![image](https://user-images.githubusercontent.com/97940468/179959941-a5fa81af-21d2-461e-9c7e-c2cf37a01733.png)<br>

negative=255-pic  #neg=(l-1)-img<br>
plt.figure(figsize=(6,6))<br>
plt.imshow(negative);<br>
plt.axis('off');<br>

![image](https://user-images.githubusercontent.com/97940468/179960235-6711891d-f6c1-43f3-80e0-98f4065acd6e.png)<br>

%matplotlib inline<br>

import imageio<br>
import numpy as np<br>
import matplotlib.pyplot as plt<br>

pic=imageio.imread('c5.jpg')<br>
gray=lambda rgb:np.dot(rgb[...,:3],[0.299,0.587,0.114])<br>
gray=gray(pic)<br>

max_=np.max(gray)<br>

def log_transform():<br>
    return(255/np.log(1+max_))*np.log(1+gray)<br>
plt.figure(figsize=(5,5))<br>
plt.imshow(log_transform(),cmap=plt.get_cmap(name='gray'))<br>
plt.axis('off');<br>

![image](https://user-images.githubusercontent.com/97940468/179961264-15dad3c6-9c7d-42f3-9b85-572ad3ff1a6c.png)<br>

import imageio<br>
import matplotlib.pyplot as plt<br>

#Gamma encoding<br>
pic=imageio.imread('c5.jpg')<br>
gamma=2.2 #Gamma<1~Dark;Gamma >~Bright<br>

gamma_correction=((pic/255)**(1/gamma))<br>
plt.figure(figsize=(5,5))<br>
plt.imshow(gamma_correction)<br>
plt.axis('off');<br>

![image](https://user-images.githubusercontent.com/97940468/179961514-a9ab5bee-32f4-4f61-b228-eda15aa9dae2.png)<br>

**24. Program to perform basic image manipulation:<br>
    a) Sharpness<br>
    b) Flipping<br>
    c) Cropping<br>**
    
**#Image sharpen<br>**
from PIL import Image<br>
from PIL import ImageFilter<br>
import matplotlib.pyplot as plt<br>

#Load the image<br>
my_image=Image.open('cat.jpg')<br>
plt.imshow(my_image)<br>
plt.show()<br>
#Use sharpen function<br>
sharp=my_image.filter(ImageFilter.SHARPEN)<br>
#Save the image<br>
sharp.save('C:\Sadhi\Image_sharpen.jpg')<br>
sharp.show()<br>
plt.imshow(sharp)<br>
plt.show()<br>

![image](https://user-images.githubusercontent.com/97940468/180195907-cbb8998c-e979-44df-9104-d0ca4a1a3b75.png)<br>
![image](https://user-images.githubusercontent.com/97940468/180195987-2d7ed65e-1860-495e-afa7-15dc878e5d33.png)<br>

![image](https://user-images.githubusercontent.com/97940468/180198812-31bb2fc4-d520-4c94-b014-e9952d0a243e.png)
<br>
 
**#Image flip<br>**
import matplotlib.pyplot as plt<br>
#load the image<br>
img=Image.open('cat.jpg')<br>
plt.imshow(img)<br>
plt.show()<br>
#use the flip function<br>
flip=img.transpose(Image.FLIP_LEFT_RIGHT)<br>

#save the image<br>
flip.save('C:\Sadhi\Image_flip.jpg')<br>
plt.imshow(flip)<br>
plt.show()<br>   

  ![image](https://user-images.githubusercontent.com/97940468/179962585-c788ed5b-5ff5-4a29-8d72-81f89b8fde37.png)<br>
  ![image](https://user-images.githubusercontent.com/97940468/179962687-1e677351-7997-4569-a5e7-35f8ab5832cb.png)<br>
  ![image](https://user-images.githubusercontent.com/97940468/180198933-9f5ecee8-2e9e-4c12-ae3d-998ecb092f72.png)

 
  
**#Image Crop<br>**  
#Importing Image class from PIL module<br>
from PIL import Image<br>
import matplotlib.pyplot as plt<br>
#Opens a image in RGB mode<br>
im=Image.open('cat.jpg')<br>

#Size of the image in pixels(size of original image)<br>
#(This is not mandatory)<br>
width,height=im.size<br>

#Cropped image of above dimension<br>
#(It will not Change original image)<br>
im1=im.crop((80,80,350,300))<br>

#Shows the image in image viewer<br>
im1.show()<br>
plt.imshow(im1)<br>
plt.show()<br>

![image](https://user-images.githubusercontent.com/97940468/179962952-9a298d43-f208-4fc7-8b90-efc91b7efb56.png)
<br>
__________________________________________________________________________________________
**PILLOW FUNCTION**
from PIL import Image, ImageChops, ImageFilter<br>
from matplotlib import pyplot as plt<br>

#Create a PIL Image objects<br>
x=Image.open("x.png")<br>
o=Image.open("o.png")<br>

#Find out attributes of Image Objects<br>
print('size of the image:',x.size,'colour mode:',x.mode)<br>
print('size of the image:',o.size,'colour mode:',o.mode)<br>

#plot 2 images one besides the other<br>
plt.subplot(121),plt.imshow(x)<br>
plt.axis('off')<br>
plt.subplot(122),plt.imshow(o)<br>
plt.axis('off')<br>

#multiply images<br>
merged=ImageChops.multiply(x,o)<br>

#adding 2 images<br>
add=ImageChops.add(x,o)<br>

#convert colour mode<br>
greyscale=merged.convert('L')<br>
greyscale<br>

OUTPUT:<br>
size of the image: (256, 256) colour mode: RGB<br>
size of the image: (256, 256) colour mode: RGB<br>
![image](https://user-images.githubusercontent.com/97940468/186653380-14746cc1-9207-49d5-8c90-bebff8708f9f.png)<br>
<br>
#more Attributes<br>
image = merged<br>

print('image size:',image.size,<br>
     '\ncolor mode:', image.mode,<br>
    '\nimage width:',image.width, '| also represented by:', image.size[0],<br>
     '\nimage height:',image.height, '| also represented by:', image.size[1],)<br>
 
 OUTPUT:<br>    
image size: (256, 256) <br>  
color mode: RGB <br>  
image width: 256 | also represented by: 256 <br>  
image height: 256 | also represented by: 256<br>  

#mapping the pixels of the image so we can use them as coord<br>  
pixel = greyscale.load()<br> 

#a nested loop to parse through all the pixels in the image<br> 
for row in range(greyscale.size[0]):<br> 
 for column in range(greyscale.size[1]):<br> 
    if pixel[row,column] != (255):<br> 
     pixel[row,column] = (0)<br> 
greyscale   <br>          

 OUTPUT:<br> 
 ![image](https://user-images.githubusercontent.com/97940468/186653791-924954f1-22a5-4a82-8280-a75b880625b2.png)<br> 
 
 #1.invert image<br> 
invert = ImageChops.invert(greyscale)<br> 

#2.invert by subtraction<br> 
bg = Image.new('L',(256,256), color=(255))#create a new image with a solid white background<br> 
subt = ImageChops.subtract(bg,greyscale)#subtract image from background<br> 

#3.rotate<br> 
rotate=subt.rotate(45)<br> 
rotate<br> 
 OUTPUT:<br> 
 ![image](https://user-images.githubusercontent.com/97940468/186654031-f3a594b4-03d3-44ff-b6cc-8aa56e883242.png)<br>
 #gaussian blur<br>
blur=greyscale.filter(ImageFilter.GaussianBlur(radius=1))<br>

#edge detection<br>
edge = blur.filter(ImageFilter.FIND_EDGES)<br>
edge<br>
 OUTPUT:<br> 
 ![image](https://user-images.githubusercontent.com/97940468/186654247-aa5d527f-61f5-4b18-b102-b2e371ea0f3e.png)<br>
 
 
 #change edge colours<br>
edge = edge.convert('RGB')<br>
bg_red=Image.new('RGB',(256,256),color=(255,0,0))<br>

filled_edge=ImageChops.darker(bg_red,edge)<br>
filled_edge<br>

OUTPUT:<br> 

![image](https://user-images.githubusercontent.com/97940468/186654584-00e0ee46-6a2d-44f0-9b10-ca3c2e6057b8.png)<br> 

#save image in the directory<br> 
edge.save('processed.png')<br> 

**Implement a program to perform various edge detection techniques<br>**
**a) Canny Edge detection **<br>

#Canny Edge detection<br> 
import cv2<br> 
import numpy as np<br> 
import matplotlib.pyplot as plt<br> 
plt.style.use('seaborn')<br> 

loaded_image=cv2.imread("c7.jpg")<br> 
loaded_image=cv2.cvtColor(loaded_image,cv2.COLOR_BGR2RGB)<br> 

gray_image=cv2.cvtColor(loaded_image,cv2.COLOR_BGR2GRAY)<br> 

edged_image=cv2.Canny(gray_image,threshold1=30,threshold2=100)<br> 

plt.figure(figsize=(20,20))<br> 
plt.subplot(1,3,1)<br> 
plt.imshow(loaded_image,cmap="gray")<br> 
plt.title("Original Image")<br> 
plt.axis("off")<br> 
plt.subplot(1,3,2)<br> 
plt.imshow(gray_image,cmap="gray")<br> 
plt.axis("off")<br> 
plt.title("GrayScale Image")<br> 
plt.subplot(1,3,3)<br> 
plt.imshow(edged_image,cmap="gray")<br> 
plt.axis("off")<br> 
plt.title("Canny Edge Detected Image")<br> 
plt.show<br> 
OUTPUT:
![image](https://user-images.githubusercontent.com/97940468/187900875-c39f6a7f-bc66-4941-aa47-71ab064b1b1b.png)
![image](https://user-images.githubusercontent.com/97940468/187900970-8e1c2f70-0c6b-404c-80f3-8b010065d594.png)
![image](https://user-images.githubusercontent.com/97940468/187901100-16c6025b-b985-478c-b012-f3fcfee976f4.png)

**b) Edge detection schemas-the gradient(Sobel-first order derivatives)based edge detector and the Laplacian(2nd order derivative,so it is extremely sensitive to noise)based edge detector**<br>
#LapLacian and Sobel Edge detecting methods<br> 
import cv2<br> 
import numpy as np<br> 
from matplotlib import pyplot as plt<br> 

#Loading image<br> 
#img0=cv2.imread('sanFrancisco.jpg',)<br> 
img0=cv2.imread("c7.jpg")<br> 

#Converting to gray scale<br> 
gray=cv2.cvtColor(img0,cv2.COLOR_BGR2GRAY)<br> 

#remove noise<br> 
img=cv2.GaussianBlur(gray,(3,3),0)<br> 

#covolute with proper kernels<br> 
laplacian=cv2.Laplacian(img,cv2.CV_64F)<br> 
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5) #X<br> 
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5) #y<br> 

plt.subplot(2,2,1),plt.imshow(img,cmap='gray')<br> 
plt.title('Original'),plt.xticks([]),plt.yticks([])<br> 
plt.subplot(2,2,2),plt.imshow(laplacian,cmap='gray')<br> 
plt.title('Laplacian'),plt.xticks([]),plt.yticks([])<br> 
plt.subplot(2,2,3),plt.imshow(sobelx,cmap='gray')<br> 
plt.title('Sobel X'),plt.xticks([]),plt.yticks([])<br> 
plt.subplot(2,2,4),plt.imshow(sobely,cmap='gray')<br> 
plt.title('Sobel Y'),plt.xticks([]),plt.yticks([])<br> 

plt.show()<br> 
OUTPUT:<br> 
![image](https://user-images.githubusercontent.com/97940468/187901330-37d06e5d-bf06-4388-bba6-26d860bdc9f1.png)
<br> 
**c) Edge detection using Prewitt Operator** <br>
#Edge detection using Prewitt operator<br> 
import cv2<br> 
import numpy as np<br> 
from matplotlib import pyplot as plt<br> 
img=cv2.imread('c7.jpg')<br> 
gray=cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)<br> 
img_gaussian=cv2.GaussianBlur(gray,(3,3),0)<br> 

#prewitt<br> 
kernelx=np.array([[1,1,1],[0,0,0],[-1,-1,-1]])<br> 
kernely=np.array([[-1,0,1],[-1,0,1],[-1,0,1]])<br> 
img_prewittx=cv2.filter2D(img_gaussian,-1,kernelx)<br> 
img_prewitty=cv2.filter2D(img_gaussian,-1,kernely)<br> 

cv2.imshow("Original Image",img)<br> 
cv2.imshow("Prewitt X", img_prewittx)<br> 
cv2.imshow("Prewitt Y", img_prewitty)<br> 
cv2.imshow("Prewitt",img_prewittx+img_prewitty)<br> 
cv2.waitKey()<br> 
cv2.destroyAllWindows()<br> 

OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97940468/187901965-a0affd3c-8ac2-45be-8ab7-14a2fdc45be2.png)
![image](https://user-images.githubusercontent.com/97940468/187902089-214468a1-dbfc-4297-ae11-df171fbfdab8.png)
![image](https://user-images.githubusercontent.com/97940468/187902173-5b443cf9-35cd-406a-b229-be31ec0d4bcd.png)
![image](https://user-images.githubusercontent.com/97940468/187902241-abd81635-2785-47e7-a23b-a158522e8ea6.png)

<br>

**d) Roberts Edge Detection-Roberts cross operator<br>**

#Roberts Edge Detection- Roberts cross operator<br>
import cv2<br>
import numpy as np<br>
from scipy import ndimage<br>
from matplotlib import pyplot as plt<br>
roberts_cross_v=np.array([[1,0],[0,-1]])<br>
roberts_cross_h=np.array([[0,1],[-1,0]])<br>

img=cv2.imread("c7.jpg",0).astype('float64')<br>
img/=255.0<br>
vertical=ndimage.convolve(img,roberts_cross_v)<br>
horizontal=ndimage.convolve(img,roberts_cross_h)<br>

edged_img=np.sqrt(np.square(horizontal)+np.square(vertical))<br>
edged_img*=255<br>
cv2.imwrite("Output.jpg",edged_img)<br>
cv2.imshow("OutputImage",edged_img)<br>
cv2.waitKey()<br>
cv2.destroyAllWindows()<br>

OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97940468/187902436-ebadfd95-7045-42c8-9459-bedc01bc5fab.png)<br>


import numpy as np<br>
import cv2<br>
import matplotlib.pyplot as plt<br>

#Open the image<br>
img = cv2.imread('dimage_damaged.png')<br>
plt.imshow(img)<br>
plt.show()<br>

#load the mask<br>
mask=cv2.imread('dimage_mask.png',0)<br>
plt.imshow(mask)<br>
plt.show()<br>

#Inpaint<br>
dst = cv2.inpaint(img,mask,3,cv2.INPAINT_TELEA)<br>

#Write the output.<br>
cv2.imwrite('dimage_inpainted.png',dst)<br>
plt.imshow(dst)<br>
plt.show()<br>

OUTPUT:<br>
![download](https://user-images.githubusercontent.com/97940468/190844556-a8a96309-8acf-4622-9c14-e84ae77009c4.png)<br>
![download](https://user-images.githubusercontent.com/97940468/190844562-892844e6-4f61-4f72-9809-70be879ecaac.png)<br>
![download](https://user-images.githubusercontent.com/97940468/190844567-6469c739-004a-40a6-bb9a-338e98890738.png)<br>

import numpy as np<br>
import matplotlib.pyplot as plt<br>
import pandas as pd<br>
plt.rcParams['figure.figsize'] =(10,8)<br>

def show_image(image,title='Image',cmap_type='gray'):<br>
    plt.imshow(image,cmap=cmap_type)<br>
    plt.title(title)<br>
    plt.axis('off')<br>
    
def plot_comparison(img_original,img_filtered,img_title_filtered):<br>
    fig,(ax1,ax2)=plt.subplots(ncols=2, figsize=(10,8), sharex=True, sharey=True)<br>
    ax1.imshow(img_original,cmap=plt.cm.gray)<br>
    ax1.set_title('Original')<br>
    ax1.axis('off')<br>
    ax2.imshow(img_filtered,cmap=plt.cm.gray)<br>
    ax2.set_title('img_title_filtered')<br>
    ax2.axis('off')<br>
    
from skimage.restoration import inpaint<br>
from skimage.transform import resize<br>
from skimage import color<br>

image_with_logo=plt.imread('imlogo.png')<br>

#Initialize the mask<br>
mask=np.zeros(image_with_logo.shape[:-1])<br>

#Set the pixels where the Logo is to  1<br>
mask[210:272, 360:425] = 1<br>

#Apply inpainting to remove the Logo<br>
image_logo_removed = inpaint.inpaint_biharmonic(image_with_logo,<br>
                                              mask,<br>
                                              multichannel=True)<br>

#show the original and Logo removed images<br>
plot_comparison(image_with_logo,image_logo_removed,'Image with logo removed')<br>


OUTPUT:<br>
![download](https://user-images.githubusercontent.com/97940468/190844700-c90a55d5-4ce6-4cb2-a5ad-861d100ec16d.png)<br>


from skimage.util import random_noise<br>

fruit_image=plt.imread('fruits.jpg')<br>

#add noise to the image<br>
noisy_image=random_noise(fruit_image)<br>

#Show the original and resulting image<br>
plot_comparison(fruit_image, noisy_image, 'Noisy image')<br>

OUTPUT:<br>
![download](https://user-images.githubusercontent.com/97940468/190844774-1ec064ca-5715-4078-8db9-e4215fb8085c.png)<br>

from skimage.restoration import denoise_tv_chambolle<br>

noisy_image=plt.imread('noisy.jpg')<br>

#Apply total variation filter denoising<br>
denoised_image=denoise_tv_chambolle(noisy_image,multichannel=True)<br>

#show the noisy and denopised image<br>
plot_comparison(noisy_image,denoised_image,'Denoised Image')<br>

OUTPUT:<br>
![download](https://user-images.githubusercontent.com/97940468/190844810-ceefaf3a-12d9-4385-8175-a198d5188e2b.png)


from skimage.restoration import denoise_bilateral<br>

landscape_image=plt.imread('noisy.jpg')<br>

#Apply bilateral filter denoising<br>
denoised_image=denoise_bilateral(landscape_image,multichannel=True)<br>

#Show original and resulting images<br>
plot_comparison(landscape_image, denoised_image,'Denoised Image')<br>


OUTPUT:<br>
![download](https://user-images.githubusercontent.com/97940468/190844844-dd994cf8-ed1a-4e74-9065-8fb3d4661fa3.png)<br>

from skimage.segmentation import slic<br>
from skimage.color import label2rgb<br>
import matplotlib.pyplot as plt<br>
import numpy as np<br>
face_image = plt.imread('face.jpg')<br>
segments = slic(face_image, n_segments=400)<br>
segmented_image=label2rgb(segments,face_image,kind='avg')<br>
plt.imshow(face_image)<br>
plt.show()<br>
plt.imshow((segmented_image * 1).astype(np.uint8))<br>
plt.show()<br>

OUTPUT:<br>
![download](https://user-images.githubusercontent.com/97940468/190844878-1ac3ef79-fe8c-4a5c-8a56-973d312c137e.png)<br>
![download](https://user-images.githubusercontent.com/97940468/190844889-094d27e1-24e7-4ca5-a1fb-6fa05b08ffbc.png)<br>

def show_image_contour(image,contours):<br>
    plt.figure()<br>
    for n, contour in enumerate(contours):<br>
        plt.plot(contour[:,1], contour[:,0],linewidth=3)<br>
    plt.imshow(image,interpolation='nearest',cmap='gray_r')<br>
    plt.title('Contours')<br>
    plt.axis('off')<br>
    
    
from skimage import measure, data<br>

#obtain the horse image<br>
horse_image=data.horse()<br>

#Find the contours with a constant level value of 0.8<br>
contours=measure.find_contours(horse_image,level=0.8)<br>

#Shows the image with contours found<br>
show_image_contour(horse_image,contours)  <br>
    
OUTPUT:<br>
![download](https://user-images.githubusercontent.com/97940468/190844948-454e22ad-b0e2-4603-b89f-ff569d8ee07e.png)<br>

from skimage.io import imread <br>
from skimage.filters import threshold_otsu <br>

image_dices=imread('diceimg.png') <br>

#make the image grayscale <br>
image_dices=color.rgb2gray(image_dices) <br>

#Obtain the optimal thresh value <br>
thresh=threshold_otsu(image_dices) <br>

#Apply threshholding <br>
binary=image_dices > thresh <br>

#Find contours at aconstant value of 0.8 <br>
contours=measure.find_contours(binary,level=0.8) <br>

#Show the image <br>
show_image_contour(image_dices, contours) <br>

OUTPUT:<br>
![download](https://user-images.githubusercontent.com/97940468/190844985-9c486bca-8a2b-438d-b6c3-844bc628adac.png)<br>

#Create list with the shape of each contour<br>
shape_contours=[cnt.shape[0] for cnt in contours]<br>

#Set 50 as the maximum sixe of the dots shape<br>
max_dots_shape=50<br>

#Count dots in contours excluding bigger then dots size<br>
dots_contours=[cnt for cnt in contours if np.shape(cnt)[0]<max_dots_shape]<br>

#Shows all contours found<br>
show_image_contour(binary, contours)<br>

#Print the dice's number<br>
print('Dices dots number:{}.'.format(len(dots_contours)))<br>

OUTPUT:<br>
Dices dots number:21.<br>
![download](https://user-images.githubusercontent.com/97940468/190845017-25e8abb4-32b9-447f-86de-17b8a4cd28ed.png)<br>

