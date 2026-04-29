# Histogram Equalization Using OpenCV (Grayscale & Color Images)

## Developed by : SANTHOSH KUMAR A
## Register No  : 212224230250

## Aim

To write a Python program using OpenCV to perform histogram equalization on both grayscale and color images to enhance image contrast and brightness.

The program performs the following operations:

- Read and display a grayscale image  
- Plot histogram of the grayscale image  
- Apply histogram equalization on grayscale image  
- Read and display a color image  
- Plot histogram of B, G, R channels  
- Convert image to HSV color space  
- Apply histogram equalization on the Value (V) channel  
- Convert the enhanced image back to BGR format  
- Display original and enhanced images with histograms  

---

## Software Used

- Anaconda – Python 3.7  
- Jupyter Notebook / VS Code  
- OpenCV (`cv2`)  
- NumPy  
- Matplotlib  

---

## Algorithm

### Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:
Read the image `parrot.jpg` in grayscale format.

### Step 3:
Display the grayscale image and plot its histogram.

### Step 4:
Apply histogram equalization using `cv2.equalizeHist()` to enhance contrast.

### Step 5:
Display original grayscale image, its histogram, enhanced image, and its histogram using a 2 × 2 grid.

### Step 6:
Read the same image in color format.

### Step 7:
Split the image into B, G, R channels and plot their histograms.

### Step 8:
Convert the image from BGR to HSV color space.

### Step 9:
Apply histogram equalization on the V (Value) channel.

### Step 10:
Merge the channels and convert the image back to BGR format.

### Step 11:
Display original color image, histogram, enhanced image, and enhanced histogram using a 2 × 2 grid.

```
import cv2
from matplotlib import pyplot as plt
```
```
image = cv2.imread('C:\\Users\\admin\\Downloads\\tiger.png')
```
```
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```
```
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

print("Name : SANTHOSH KUMAR A")
print("REG NO: 212224230250")
```
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
```
```
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

print("Name : SANTHOSH KUMAR A")
print("REG NO: 212224230250")
```
```
equalized_image = cv2.equalizeHist(gray_image)
```
```
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

print("Name : SANTHOSH KUMAR A")
print("REG NO: 212224230250")
```
```
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
```
```
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

print("Name : SANTHOSH KUMAR A")
print("REG NO: 212224230250")
```
##  Output
<img width="713" height="529" alt="image" src="https://github.com/user-attachments/assets/6d57dd1c-d120-48d4-821a-3cd5dd687e0a" />
<img width="757" height="614" alt="image" src="https://github.com/user-attachments/assets/65335fdc-041e-4928-bbfa-092d4875f0f1" />
<img width="720" height="530" alt="image" src="https://github.com/user-attachments/assets/c0c4fe2e-015d-4eb6-ac87-afe3dbe17410" />

<img width="734" height="608" alt="image" src="https://github.com/user-attachments/assets/4f35fd27-264d-489c-b8e8-6a6846b6346f" />


## Result

Thus, histogram equalization is successfully performed on both grayscale and color images using OpenCV. The contrast and brightness of the images are significantly improved, enhancing visual quality and feature visibility.
