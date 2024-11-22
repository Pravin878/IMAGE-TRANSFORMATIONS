# EX 4
# IMAGE-TRANSFORMATIONS
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import the necessary libraries and read the original image and save it as a image variable.

### Step2:

Translate the image using a function warpPerpective()

### Step3:

Scale the image by multiplying the rows and columns with a float value.

### Step4:

Shear the image in both the rows and columns.

### Step5:

Find the reflection of the image.

### Step6:

Rotate the image using angle function.

## Program:
```
Developed By: Pravin kumar G
Register Number: 212222230109
```

## i)Image Translation

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread("kamal2.jpg")
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,50],  [0,1,100],  [0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```

## ii) Image Scaling

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("kamal2.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```


## iii)Image shearing

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("kamal2.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()
```


### iv)Image Reflection

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("kamal2.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```


### v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("kamal2.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()

angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(input_image,M,(int(cols),int(rows)))

plt.imshow(rotated_img)
plt.show()
```



### vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("kamal2.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()
```


## Output:
### i)Image Translation

![image](https://github.com/user-attachments/assets/4a88b9fb-6671-4c43-b16f-42b738d19c06)

### ii) Image Scaling

![image](https://github.com/user-attachments/assets/5e68348f-66ad-4875-93bc-2fd66fabd9e8)

![WhatsApp Image 2024-11-18 at 21 14 41_b2fc0067](https://github.com/user-attachments/assets/9b1a0e57-dd29-48cd-b999-6660687b9033)

### iii)Image shearing

![image](https://github.com/user-attachments/assets/5f896db6-cc4b-424f-9182-bca697c8fc68)

![image](https://github.com/user-attachments/assets/7b0868f4-6955-4e08-b23a-f55e17aedfe3)

### iv)Image Reflection

![image](https://github.com/user-attachments/assets/1572c325-7fff-4271-b132-59b82074898d)

![image](https://github.com/user-attachments/assets/c29677bc-70a9-425f-902a-60b4dd9cfa0b)

### v)Image Rotation

![image](https://github.com/user-attachments/assets/ff0fc055-cbe0-469e-abb9-f68b8a7141df)

### vi)Image Cropping

![image](https://github.com/user-attachments/assets/032da5e3-be8a-483f-b118-8d1463023749)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
