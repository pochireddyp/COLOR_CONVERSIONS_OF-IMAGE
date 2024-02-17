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

##### Program:
### Developed By:Pochireddy.P
### Register Number: 212223240115

```
<table>
  <tr>
    <td width=50%>

### i) Read and display the image

```Python
    import cv2
    image=cv2.imread('Pochi.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('Deepika',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
#### OUTPUT:
![pochi1 1](https://github.com/pochireddyp/COLOR_CONVERSIONS_OF-IMAGE/assets/150232043/29ab33c6-cb23-4f7d-bb9e-a3aee119b12d)
<br>
<br>

### ii)Write the image
```Python
    import cv2
    image=cv2.imread('Pochi.jpg',0)
    cv2.imwrite('nemo.jpg',image)
```
#### OUTPUT:

![pochi1 2](https://github.com/pochireddyp/COLOR_CONVERSIONS_OF-IMAGE/assets/150232043/fcfee264-4051-4b9b-ada9-67452c6bd980)

<br>
<br>

### iii)Shape of the Image
```Python
     import cv2
    image=cv2.imread('Pochi.jpg',1)
    print(image.shape)
```
  </td> 
  <td>

#### OUTPUT:
![pochi1 3](https://github.com/pochireddyp/COLOR_CONVERSIONS_OF-IMAGE/assets/150232043/d7589429-1259-4b50-9d47-e562a9b22fb6)

<br>
<br>

### iv)Access rows and columns
```Python
     import random
     import cv2
     image=cv2.imread('Pochi.jpg',1)
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
#### OUTPUT:
![pochi1 4](https://github.com/pochireddyp/COLOR_CONVERSIONS_OF-IMAGE/assets/150232043/9c567711-5e66-4a81-86b0-e17c71bf53c9)
<br>
<br>

### v)Cut and paste portion of image
```Python
     import cv2
     image=cv2.imread('Pochi.jpg',1)
     image=cv2.resize(image,(400,400))
     tag =image[150:200,110:160]
     image[110:160,150:200] = tag
     cv2.imshow('partimage1',image)
     cv2.waitKey(0)
     cv2.destroyAllWindows()
```
  </td>
  <td>

#### OUTPUT:

![pochi1 5](https://github.com/pochireddyp/COLOR_CONVERSIONS_OF-IMAGE/assets/150232043/8991f0f7-3e56-425d-ab62-e24904527bba)

<br>
<br>

### vi) BGR and RGB to HSV and GRAY
```Python
    import cv2
    img = cv2.imread('Pochi.jpg',1)
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

#### OUTPUT:
![pochi1 6](https://github.com/pochireddyp/COLOR_CONVERSIONS_OF-IMAGE/assets/150232043/f1d65467-b13e-4850-a6fa-a8b258e7abea).

<br>
<br>

### vii) HSV to RGB and BGR

```Python
import cv2
img = cv2.imread('Pochi.jpg')
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
#### OUTPUT:
![pochi1 7](https://github.com/pochireddyp/COLOR_CONVERSIONS_OF-IMAGE/assets/150232043/3cf0c232-fcc4-40ee-aa30-c21bf5f4b8b5)

<br>
<br>

### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('Pochi.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
#### OUTPUT:
![pochi1 8](https://github.com/pochireddyp/COLOR_CONVERSIONS_OF-IMAGE/assets/150232043/85f78757-9b5c-464a-9936-dfdc22bd677a)
<br>
<br>

### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('Pochi.jpg',1)
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
#### OUTPUT:
![pochi1 9](https://github.com/pochireddyp/COLOR_CONVERSIONS_OF-IMAGE/assets/150232043/837fa87a-4123-47a0-962e-af8bf537d89c)
<br>
<br>

### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("Pochi.jpg",1)
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
#### OUTPUT:

![pochi1 10](https://github.com/pochireddyp/COLOR_CONVERSIONS_OF-IMAGE/assets/150232043/38764d8c-d7f3-4e53-bf36-2e0ea24ecb9f)

<br>
<br>

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







