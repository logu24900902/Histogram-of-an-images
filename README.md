# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
### Developed By:LOGU R
### REG NO : 212224230141
```python
import cv2
import matplotlib.pyplot as plt 
Gray_image=cv2.imread("Lion image.jpeg")
plt.imshow(Gray_image)
plt.show()
Color_image=cv2.imread("shinchan Image.jpeg")
plt.imshow(Color_image)
plt.show()

# code to find the histogram of gray scale image and color image channels.

hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('gray_scale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

# Display the histogram of gray scale image and any one channel histogram from color image

hist1 = cv2.calcHist([Color_image],[0],None,[256],[0,256]) 
plt.figure()
plt.title("Histogram")
plt.xlabel('color_scale value') 
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()

# Write the code to perform histogram equalization of the image.

equ1=cv2.equalizeHist(cv2.imread('shinchan Image.jpeg',0)) 
equ=cv2.cvtColor(equ1,cv2.COLOR_BGR2RGB) 
plt.title("Equalised Image")
plt.axis("off")
plt.imshow(equ) 
plt.show()

```
## Output:
<img width="610" height="662" alt="image" src="https://github.com/user-attachments/assets/fdf8198e-e7c6-4b5f-8c6f-71eb6b5bddf4" />
<img width="595" height="438" alt="image" src="https://github.com/user-attachments/assets/3b9286f8-7a6c-45f1-ab99-68154e8ebf8e" />
<img width="616" height="434" alt="image" src="https://github.com/user-attachments/assets/482ed601-5102-4213-a0be-a0edc857eff5" />
<img width="527" height="319" alt="image" src="https://github.com/user-attachments/assets/2ae64e65-b42b-4a00-ab9e-fc2fcd62a865" />





## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
