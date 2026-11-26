# Implementation of Erosion and Dilation Using OpenCV

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

- Image Erosion
- Image Dilation

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create a blank image using NumPy.

### Step 3:

Insert text onto the image using OpenCV's text drawing function.

### Step 4:

Display the original image.

### Step 5:

Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion

- Apply the erosion operation using the created kernel.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

### Step 7: Image Dilation

- Apply the dilation operation using the same kernel.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

### Step 8:

Compare the original, eroded, and dilated images.

## Program
```py

# Step 1: Import required libraries
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Step 2: Create a blank image
image = np.zeros((300, 600), dtype=np.uint8)

# Step 3: Insert text into the image
cv2.putText(image, 'OPENCV', (100, 180),
            cv2.FONT_HERSHEY_SIMPLEX, 3, 255, 5)

# Step 4: Display the original image
plt.figure(figsize=(12, 4))

plt.subplot(1, 3, 1)
plt.imshow(image, cmap='gray')
plt.title('Original Image')
plt.axis('off')

# Step 5: Create a structuring element (kernel)
kernel = np.ones((5, 5), np.uint8)

# Step 6: Perform Erosion
erosion = cv2.erode(image, kernel, iterations=1)

plt.subplot(1, 3, 2)
plt.imshow(erosion, cmap='gray')
plt.title('Eroded Image')
plt.axis('off')

# Step 7: Perform Dilation
dilation = cv2.dilate(image, kernel, iterations=1)

plt.subplot(1, 3, 3)
plt.imshow(dilation, cmap='gray')
plt.title('Dilated Image')
plt.axis('off')

# Step 8: Display all images
plt.tight_layout()
plt.show()
```

## Developed By

**Name:** NARENDHIRAN P

**Register No:** 212224230177

## Output

### Original Image

- A text image containing characters is displayed.
- The image serves as the input for morphological processing.

<img width="382" height="225" alt="image" src="https://github.com/user-attachments/assets/e059d510-63ed-4769-9b24-9edc08fa8c94" />


### Erosion

- Original image is displayed.
- Eroded image is displayed.
- The thickness of the characters is reduced.
- Object boundaries shrink inward.

<img width="232" height="148" alt="image" src="https://github.com/user-attachments/assets/76e9c392-1d1b-4b07-bd10-8c285a31467e" />


### Dilation

- Original image is displayed.
- Dilated image is displayed.
- The thickness of the characters increases.
- Object boundaries expand outward.

<img width="218" height="145" alt="image" src="https://github.com/user-attachments/assets/bef6b7ef-0b8a-4986-acba-b7518a25cac9" />


## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.
