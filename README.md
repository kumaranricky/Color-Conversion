# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 and save and image as filename.jpg
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.
### Step4:
Split and merge the image using cv2.split and cv2.merge commands.
### Step5:
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
## <br>Output:
### i) BGR and RGB to HSV and GRAY
![s1](https://user-images.githubusercontent.com/75243072/173755840-ddf0f3e3-d2ef-41bf-ac6d-7204d19c59e5.png)

### ii) HSV to RGB and BGR
![s2](https://user-images.githubusercontent.com/75243072/173755905-9b96c7bb-9ae4-4c54-bd40-17b0b9203476.png)

### iii) RGB and BGR to YCrCb
![s3](https://user-images.githubusercontent.com/75243072/173755966-bf822b13-22a6-4195-9b3f-1d0c656fe3f7.png)

### iv) Split and merge RGB Image
![s4](https://user-images.githubusercontent.com/75243072/173756005-2dd5a963-1153-46ca-b19b-05b9a8cdad8a.png)

### <br><br><br><br>v) Split and merge HSV Image
![s5](https://user-images.githubusercontent.com/75243072/173756045-f2380ffe-b281-44b1-b6a0-15146280e1b9.png)

## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
