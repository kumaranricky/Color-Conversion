# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
###Step1:
Import cv2 and save and image as filename.jpg

###Step2:
Use imread(filename, flags) to read the file.

###Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

###Step4:
Split and merge the image using cv2.split and cv2.merge commands.

###Step5:
End the program and close the output image windows.

## Program:
```python
# Developed By:Kumaran.B
# Register Number:212220230026
#prerequisites
import cv2
img=cv2.imread("rr.jpg")
cv2.imshow("trade",img)
cv2.waitKey(0)


# i) Convert BGR and RGB to HSV and GRAY
# bgr to hsv and gray
bgr_hsv = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',bgr_hsv)
bgr_gray = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',bgr_gray)
#rgb to hsv and gray
rgb_hsv = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',rgb_hsv)
rgb_gray = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',rgb_gray)
cv2.waitKey(0)


# ii)Convert HSV to RGB and BGR
hsv_rgb = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB',hsv_rgb)
hsv_bgr = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR',hsv_bgr)
cv2.waitKey(0)


# iii)Convert RGB and BGR to YCrCb
rgb_ycrcb = cv2.cvtColor(img,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb',rgb_ycrcb)
bgr_ycrcb = cv2.cvtColor(img,cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb',bgr_ycrcb)
cv2.waitKey(0)


# iv)Split and Merge RGB Image
#split rgb
blue=img[:,:,0]
green=img[:,:,1]
red=img[:,:,2]
cv2.imshow("B",blue)
cv2.imshow("G",green)
cv2.imshow("R",red)
#merge rgb
Merge_rgb=cv2.merge((blue,green,red))
cv2.imshow("Merge_RGB",Merge_rgb)
cv2.waitKey(0)


# v) Split and merge HSV Image
#split hsv
h,s,v=cv2.split(bgr_hsv)
cv2.imshow("H",h)
cv2.imshow("S",s)
cv2.imshow("V",v)
#merge hsv
Merge_hsv=cv2.merge((h,s,v))
cv2.imshow("Merge_hsv",Merge_hsv)
cv2.waitKey(0)

```
## Output:
### i) BGR and RGB to HSV and GRAY
![s1](https://user-images.githubusercontent.com/75243072/162784386-d23e7a61-024a-48bd-8b4a-bc902f27a720.png)


### ii) HSV to RGB and BGR
![s2](https://user-images.githubusercontent.com/75243072/162784529-6aac016c-aefa-4e5f-a297-29aef52ce0ff.png)


### iii) RGB and BGR to YCrCb
![s3](https://user-images.githubusercontent.com/75243072/162784557-7961bf19-d965-4968-a7cc-dfdcc6c9480e.png)


### iv) Split and merge RGB Image
![s4](https://user-images.githubusercontent.com/75243072/162784588-34eea57d-5987-49e3-bdc4-2c22c87f05db.png)


### v) Split and merge HSV Image
![s5](https://user-images.githubusercontent.com/75243072/162784612-54e368e2-4041-4334-a038-015952992fe0.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
