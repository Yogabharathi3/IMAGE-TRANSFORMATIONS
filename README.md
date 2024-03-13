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
![Screenshot 2024-03-13 140426](https://github.com/Yogabharathi3/IMAGE-TRANSFORMATIONS/assets/118899387/28156dcf-358e-4bc1-8262-8d026159bcc0)
![Screenshot 2024-03-13 140433](https://github.com/Yogabharathi3/IMAGE-TRANSFORMATIONS/assets/118899387/254f434d-3808-4628-8040-7831b9d50803)

### ii) Image Scaling
![Screenshot 2024-03-13 140647](https://github.com/Yogabharathi3/IMAGE-TRANSFORMATIONS/assets/118899387/da2728bc-22a4-47a1-b683-d75e0291376c)
![Screenshot 2024-03-13 140655](https://github.com/Yogabharathi3/IMAGE-TRANSFORMATIONS/assets/118899387/e7f7463a-3e2d-48ad-8406-b4a831ebdd9a)

### iii)Image shearing
![Screenshot 2024-03-13 140834](https://github.com/Yogabharathi3/IMAGE-TRANSFORMATIONS/assets/118899387/5eaf2b39-a0cf-4c85-89ee-7a2928a0fca3)
![Screenshot 2024-03-13 140841](https://github.com/Yogabharathi3/IMAGE-TRANSFORMATIONS/assets/118899387/96356b1a-686f-4e7a-8996-45e36e3ae1d9)
![Screenshot 2024-03-13 140847](https://github.com/Yogabharathi3/IMAGE-TRANSFORMATIONS/assets/118899387/7fa18db4-06e2-4471-95aa-7ab174d3b87b)

### iv)Image Reflection
![image](https://github.com/Yogabharathi3/IMAGE-TRANSFORMATIONS/assets/118899387/3c4971f8-b8a4-406a-ba60-323f93415606)
![Screenshot 2024-03-13 141038](https://github.com/Yogabharathi3/IMAGE-TRANSFORMATIONS/assets/118899387/93b26f93-cfac-4aa8-9d27-48535c97ec39)
![Screenshot 2024-03-13 141050](https://github.com/Yogabharathi3/IMAGE-TRANSFORMATIONS/assets/118899387/7b3519cd-4921-4575-8827-6b2ac904188a)

### v)Image Rotation
![Screenshot 2024-03-13 141156](https://github.com/Yogabharathi3/IMAGE-TRANSFORMATIONS/assets/118899387/28d4f6bb-3754-42e7-b083-41dedf08c2dc)
![Screenshot 2024-03-13 141204](https://github.com/Yogabharathi3/IMAGE-TRANSFORMATIONS/assets/118899387/a92d58a5-491a-401d-9a76-e265765116b4)

### vi)Image Cropping
![Screenshot 2024-03-13 141328](https://github.com/Yogabharathi3/IMAGE-TRANSFORMATIONS/assets/118899387/b383a754-4e25-44fc-b6f2-f7f3be01cfae)
![Screenshot 2024-03-13 141335](https://github.com/Yogabharathi3/IMAGE-TRANSFORMATIONS/assets/118899387/ccb76dd9-491b-42d1-88fe-470361a89020)

## Result: 
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
