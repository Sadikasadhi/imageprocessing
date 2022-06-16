# imageprocessing

import cv2
img=cv2.imread('b1.jpg')
cv2.imshow("RGB",img)
cv2.waitKey(0)

img=cv2.imread('b1.jpg',0)
cv2.imshow("Gray",img)
cv2.waitKey(0)

ret,bw_img=cv2.threshold(img,127,255,cv2.THRESH_BINARY)
cv2.imshow("Binary",bw_img)
cv2.waitKey(0)
cv2.destroyAllWindows()







import cv2
img=cv2.imread('b1.jpg')
print('original image length width',img.shape)
cv2.imshow('original image',img)
cv2.waitKey(0)

imgresize=cv2.resize(img,(150,160))
cv2.imshow('Resized image',imgresize)
print('Resized image length,width',imgresize.shape)
cv2.waitKey(0)
