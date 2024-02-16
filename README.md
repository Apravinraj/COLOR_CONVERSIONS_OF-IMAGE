# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image


### Developed By:PRAVIN RAJ A
### Register Number: 212222240079
### IMAGE

![304442919-c9ec43be-c35a-4cbb-91e4-abaea3ee631b](https://github.com/Apravinraj/COLOR_CONVERSIONS_OF-IMAGE/assets/118707879/6755473c-4706-4df3-97c1-026f0c22a20c)

### Program:

### i) Read and display the image
```#Read and display the image
import cv2
image=cv2.imread('exp1.jpg',1)
image=cv2.resize(image,(200,325))
cv2.imshow('PRAVIN RAJ',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

## Output:

![304443378-4afb154d-9e78-4981-9f4e-2a21f0cb341a](https://github.com/Apravinraj/COLOR_CONVERSIONS_OF-IMAGE/assets/118707879/84740ce7-3773-4888-ac66-e7759d92ffcc)
### Program:
### ii)Write the image
```
#Write the image
import cv2
image=cv2.imread('exp1.jpg',0)
cv2.imwrite('demos.jpg',image)
```
<br>
<br>

### Output

![304443746-462c4bb1-d793-468b-842e-9f2fa5e0fdfb](https://github.com/Apravinraj/COLOR_CONVERSIONS_OF-IMAGE/assets/118707879/d7688b2f-8604-468d-a082-563627ef81cb)

### Program:
### iii)Shape of the Image
```
#Shape of the Image
import cv2
image=cv2.imread('exp1.jpg',1)
print(image.shape)
```
<br>
<br>

### Output

![304444224-a8e6ab3b-d8ec-45ba-8beb-b11bd4478fa4](https://github.com/Apravinraj/COLOR_CONVERSIONS_OF-IMAGE/assets/118707879/3ed0b836-2387-464c-9863-7a27be756f47)

### Program:
### iv)Access rows and columns
```
#Access rows and columns
import random
import cv2
image=cv2.imread('exp1.jpg',1)
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                    random.randint(0,255),
                    random.randint(0,255)] 
cv2.imshow('part image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

### Output

![304444441-7b594820-61e3-4884-bd31-96c959a4bd39](https://github.com/Apravinraj/COLOR_CONVERSIONS_OF-IMAGE/assets/118707879/924a2d18-6c0f-4931-b526-c79a1ad4eaa5)

### Program:
### v)Cut and paste portion of image
```
#Cut and paste portion of image
import cv2
image=cv2.imread('exp1.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[150:200,110:160]
image[110:160,150:200] = tag
cv2.imshow('partimage1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

### Output

![304444666-70e5f610-c3e5-43fc-83c8-427150297f15](https://github.com/Apravinraj/COLOR_CONVERSIONS_OF-IMAGE/assets/118707879/b6db4ddf-51d6-42ef-a0c3-44ed7ffb2d78)

### Program:
### vi) BGR and RGB to HSV and GRAY
```
#BGR and RGB to HSV and GRAY
import cv2
img = cv2.imread('exp1.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)

hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)

gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)

gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

## Original Image

![304445586-945f9cfa-4ae4-4efe-a50e-c5988dfa4119](https://github.com/Apravinraj/COLOR_CONVERSIONS_OF-IMAGE/assets/118707879/845390d4-48f4-4bbc-834a-eb24750be0aa)
### Output

![304447083-7db5be3c-41a0-4fb0-8061-5ed7423f2632](https://github.com/Apravinraj/COLOR_CONVERSIONS_OF-IMAGE/assets/118707879/94fb3bbf-89f0-4d44-a58c-4a48475a56c5)

### Program:
### vii) HSV to RGB and BGR
```
#HSV to RGB and BGR
import cv2
img = cv2.imread('exp1.jpg')
img = cv2.resize(img,(300,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

### Original HSV

![304458218-44529ae0-3956-4018-a138-35c3a427b41e](https://github.com/Apravinraj/COLOR_CONVERSIONS_OF-IMAGE/assets/118707879/bbfb3d46-34fc-49ef-9018-7d492fe1a49c)

### Output

![304458441-d58e2620-c2ff-4371-9709-82327e1c16aa](https://github.com/Apravinraj/COLOR_CONVERSIONS_OF-IMAGE/assets/118707879/0b118be2-b565-4028-ac3f-fdd2e7baf8e3)

### Program:
### viii) RGB and BGR to YCrCb
```
#RGB and BGR to YCrCb
import cv2
img = cv2.imread('exp1.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

### Output

![304460065-3856ba4c-a2c3-44e2-94e5-4a49a913e14e](https://github.com/Apravinraj/COLOR_CONVERSIONS_OF-IMAGE/assets/118707879/ea7c29a8-dd9a-40a9-b08f-2d07a70b3a16)

### Program:
### ix) Split and merge RGB Image
```
#Split and merge RGB Image
import cv2
img = cv2.imread('exp1.jpg',1)
img = cv2.resize(img,(300,200))

R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

### Output
## Channels

![304460607-4ad7d95a-3c50-443f-b342-7f5ead729520](https://github.com/Apravinraj/COLOR_CONVERSIONS_OF-IMAGE/assets/118707879/c89257d4-b513-429b-b2a9-2e7ab07b8ed9)

### Merged RGB

![304460691-1d219980-ac93-4940-ab20-deb47f5906a8](https://github.com/Apravinraj/COLOR_CONVERSIONS_OF-IMAGE/assets/118707879/9bb2ad03-9352-4cad-9855-9f31b1e43dbb)

### Program:
### x) Split and merge HSV Image
```
#Split and merge HSV Image
import cv2
img = cv2.imread("exp1.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

## Output
### Merged HSV

![304461687-20844066-4618-4bd1-ae49-5457f89c33e1](https://github.com/Apravinraj/COLOR_CONVERSIONS_OF-IMAGE/assets/118707879/680b37ee-1e3a-4a17-a72a-c6f78fab310e)

### Splitted

![304463227-f4b282bb-e555-4e70-b417-37ae828b1daa](https://github.com/Apravinraj/COLOR_CONVERSIONS_OF-IMAGE/assets/118707879/63a78497-ec28-4cac-9930-f5931aa41160)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







