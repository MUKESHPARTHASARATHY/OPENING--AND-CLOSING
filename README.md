# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

 
## Program:
### Name: MUKESH P
### Register number: 212222240068
```
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((300, 600, 3), dtype="uint8")

# Create the Text using cv2.putText
text = "MUKESH"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

# Use Opening operation
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

# Use Closing Operation
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

# Convert images from BGR to RGB for Matplotlib
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)

# Plot the original, opening, and closing images using Matplotlib
plt.figure(figsize=(10, 5))
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")

plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")

plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")

```
## Output:

### Display the input Image

![download](https://github.com/user-attachments/assets/11fd0de7-318f-4e38-b701-d78a917eba47)



### Display the result of Opening

![download](https://github.com/user-attachments/assets/ac098ddf-6f72-454d-b895-0179498117c1)


### Display the result of Closing

![download](https://github.com/user-attachments/assets/61be1d68-13c8-4879-90e0-b667d1e9f562)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
