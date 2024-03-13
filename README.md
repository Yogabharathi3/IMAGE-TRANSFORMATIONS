# IMAGE-TRANSFORMATIONS
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import the necessary libraries and read the original image and save it as a image variable.
### Step2:

Translate the image.
### Step3:

Scale the image.
### Step4:

Shear the image.
### Step5:

Find reflection of image.
### Step6:

Rotate the image.
### Step7:

Crop the image.
### Step8:
Display all the Transformed images.

## Program:
```python
Developed By:YOGABHARATHI S
Register Number:212222230179
```
### Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image = cv2.warpPerspective(lion_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
### Image Scaling:
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
scaled_img = cv2.warpPerspective(lion_image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```
### Image shearing:
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(lion_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(lion_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()
```
### Image Reflection:
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
dog_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(lion_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(lion_image,M_Y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()
```
### Image Rotation:
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
angle = np.radians(30)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(lion_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```
### Image Cropping:
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
cropped_img=lion_image[11:500,27:630]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation

### ii) Image Scaling

### iii)Image shearing

### iv)Image Reflection

### v)Image Rotation

### vi)Image Cropping

## Result: 
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
