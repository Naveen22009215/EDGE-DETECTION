# EDGE-DETECTION
### Name: Naveen Kumar P
### Reg No:212222230092
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## CODE:
```
import cv2
import matplotlib.pyplot as plt
image1=cv2.imread ('image.jpeg') 
gray = cv2.cvtColor(image1,cv2.COLOR_BGR2GRAY)
plt.title('GRAY IMAGE')
plt.imshow(gray,cmap = 'gray')

img = cv2.GaussianBlur(gray,(3,3),0)
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
sobelxy =cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(1)
plt.subplot(2,2,1)
plt.imshow(gray,cmap = 'gray')
plt.title('Original'), plt.xticks([]), plt.yticks([])

laplacian = cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(laplacian)
plt.title('laplacian')
plt.show()

canny_edges = cv2.Canny(gray, 110, 140)
plt.imshow(canny_edges)
plt.title('Canny Edges')
plt.show()
```
## Output:
### GRAY SCALE IMAGE
![image](https://github.com/Naveen22009215/EDGE-DETECTION/assets/119401470/64ce9ae8-14ae-4b6c-98c2-6a21b2466edf)

### SOBEL EDGE DETECTOR
![image](https://github.com/Naveen22009215/EDGE-DETECTION/assets/119401470/c133b7b9-264d-4115-95ca-bf7da7af979b)


### LAPLACIAN EDGE DETECTOR
![image](https://github.com/Naveen22009215/EDGE-DETECTION/assets/119401470/b4591471-4480-4426-9730-cc0c6173d4a7)


### CANNY EDGE DETECTOR
![image](https://github.com/Naveen22009215/EDGE-DETECTION/assets/119401470/21ee3729-798c-4e2e-a461-ee1b8894fa46)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
