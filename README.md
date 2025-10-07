# Implementation-of-Erosion-and-Dilation
## Aim:
To implement Erosion and Dilation using Python and OpenCV.
## Software Required:
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
import the neccesary packages

### Step2:
create the text using cv2.put Text

### Step3:
create the structuting element

### Step4:
Erodde the image

### Step5:
Dilate the image

 
## Program:

``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)

# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Amruthavarshini Gopal', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)

# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)

# Display the eroded image
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')

# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)

# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')
```
## Output:

### Display the input Image

<img width="498" height="522" alt="Screenshot 2025-10-07 154536" src="https://github.com/user-attachments/assets/e0714a02-0e1a-44bc-83be-b332cfc2b034" />


### Display the Eroded Image

<img width="485" height="517" alt="Screenshot 2025-10-07 154545" src="https://github.com/user-attachments/assets/ac5233a6-d819-44df-a09a-a152dc9147b2" />

### Display the Dilated Image

<img width="486" height="512" alt="Screenshot 2025-10-07 154554" src="https://github.com/user-attachments/assets/ffbaa96a-cd39-4751-86d9-b38e3bc50f58" />


## Result:
Thus the generated text image is eroded and dilated using python and OpenCV.
