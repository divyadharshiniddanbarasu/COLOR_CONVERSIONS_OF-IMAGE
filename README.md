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
### Developed By: Divyadharshini.A
### Register Number: 212222240027


## Output:

### i) Read and display the image

import cv2
image=cv2.imread('images.jpg',1)
image=cv2.resize(image,(400,300))
cv2.imshow('natural',image)
cv2.waitKey(0)
cv2.destroyAllWindows()

OUTPUT

![308084853-46b97dc0-2f8d-4dde-9e61-0be6bf5fcab7](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/f92cce43-70c6-4df3-b7ba-1be6e7677cce)


### ii)Write the image

import cv2
image=cv2.imread('images.jpg',0)
cv2.imwrite('natural.jpg',image)

OUTPUT

![308085161-0469e549-2130-4f5b-ae98-9ae7a25c64ac](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/ef20079e-7182-4e0d-8c3c-b0960df06766)



### iii)Shape of the Image

import cv2
image=cv2.imread('images.jpg',1)
print(image.shape)

OUTPUT

![308085662-ad69e405-1f96-4b0a-933a-c548bf8d514a](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/d17cc93b-82ec-48e0-b3b1-fce69774a7bd)



### iv)Access rows and columns
    import random
    import cv2
    image=cv2.imread('images.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('natural',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

OUTPUT

![308093360-29a58fd7-6d7f-4ffb-82d6-ef3fcefe62b3](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/478d4be2-9c38-47d3-ba4b-854a80686c49)

    

### v)Cut and paste portion of image
   import cv2
   image=cv2.imread('images.jpg',1)
   image=cv2.resize(image,(400,400))
   tag =image[130:200,110:190]
   image[110:180,120:200] = tag
   cv2.imshow('natural',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()

OUTPUT

![308094212-1c8bdacc-990d-4ddf-adfa-abd950bad17a](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/762947c3-a5c4-4135-8450-9cd8cedcb063)

### vi) BGR and RGB to HSV and GRAY

  import cv2
img = cv2.imread('images.jpg',1)
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

OUTPUT

![308095475-b328331c-a2f7-4b35-b77d-482552d28fd2](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/b22dbac4-99e0-4375-be31-e94335fdc229)
![308095628-0a643231-0519-4217-8e74-6feded114557](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/2ceb9087-0a49-4561-83cb-64dbd7e090d4)
![308095726-4b9326dc-1343-418b-8a90-c1d3d51faf2c](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/f9efbac7-323e-4250-9c02-4668e5d88f7e)
![308095818-8533b3bb-a62a-4916-80a8-562bd412a035](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/6a40b501-6d7c-4ffc-af4c-48dfa78e39ec)
![308095915-7b200a5e-f9be-41b3-acc6-3854c7c16d59](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/5220cc60-c8f9-440c-8670-62d1875f2375)



### vii) HSV to RGB and BGR
import cv2
img = cv2.imread('images.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()

OUTPUT

![308097818-e816abb7-ca10-4500-9d78-2011ac8d126d](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/32d11756-ca3f-43bf-b655-76012b4e7919)
![308097927-5dbb8777-b706-482b-95d7-3edf6b6cd3d4](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/094e7db2-4eeb-4d8e-bc6b-e77f99ccbdd3)
![308098067-f87fe894-a67a-4769-9160-92e882af48bb](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/d961f483-f91e-499c-a82a-3028bc6968ca)



### viii) RGB and BGR to YCrCb

import cv2
img = cv2.imread('images.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()

OUTPUT

![308098468-ff5f46b2-65ed-466d-878d-c3d9c867221b](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/678c85c1-3ee8-47e9-b8a8-b0766e7db7b1)
![308098777-fc3140a8-edbf-424a-bb42-3d52f7549d0f](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/0f891043-b566-4192-a222-c13a2325f5ba)
![308098971-fd1ac8b2-72f0-4b6b-ab8a-19c0c5e02956](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/1fbccbd0-d1be-44e0-a1c8-826e509bf44c)




### ix) Split and merge RGB Image

import cv2
img = cv2.imread('images.jpg',1)
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

OUTPUT

![308099371-7202f7a6-3235-4a40-98fb-cbca61404de6](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/e37afecf-c213-4e9c-8526-6dd8aaf0c4c0)
![308099537-d6e714bc-fec7-4337-8e1f-9bd1331d8cd8](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/c41da89a-d641-4df1-a373-17fd41a355ba)
![308099631-ffea9028-43ae-408a-9e51-bf9fd937da78](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/905927c5-f348-4dbf-874a-ca3fc5717a03)
![308099714-9b4aeb30-e837-447f-a6bd-d2464ba59627](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/683d229b-9573-4950-81ce-228a1192f4f8)


### x) Split and merge HSV Image

import cv2
img = cv2.imread("images.jpg",1)
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


OUTPUT

![308100006-daebecff-e02d-4660-ab5a-ba6e75a2a9ed](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/835d2e54-d79a-4934-aba9-9f867be69f06)
![308100133-10f31d28-a179-4dd3-96f3-75fd2d195c5f](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/6078fe7f-8a16-42c9-9c3e-3e3a633dd61c)
![308100213-0fa5ba4d-10c3-460c-b632-ed823cd840bd](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/79bc642e-e034-49ae-a6c0-4397ffb92536)
![308100273-67f81c4a-2190-4026-a284-248b566e23a6](https://github.com/divyadharshiniddanbarasu/COLOR_CONVERSIONS_OF-IMAGE/assets/119393424/d39f1c95-f3b7-4084-9d25-cb28f4dd840b)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







