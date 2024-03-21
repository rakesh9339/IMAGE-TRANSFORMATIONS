# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.
<br>
### Step2:
Load the image file in the program.
<br>

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.
<br>

### Step4:
Display the modified image output.
<br>

### Step5:
End the program.
<br>

## Program:
```python
Developed By: DARIO G
Register Number: 212222230027
```

i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread( "tiger.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis( 'off')
plt.imshow(input_image)
plt.show()
rows,cols,dim =input_image.shape
M =np.float32([[1,0,100],
               [0,1,100],
               [0,0,1]])
translated_image =cv2.warpPerspective(input_image, M, (cols, rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("tree.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1.5,0 ,0],
              [0,1.8,0],
              [0,0,1]])
scaled_img=cv2.warpPerspective(in_img, M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```


iii)Image shearing

``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("Building.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,0.5,0],
                [0,1 ,0],
                [0,0 ,1]])
M_y=np.float32([[1,  0,0],
                [0.5,1,0],
                [0,  0,1]])
sheared_img_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
sheared_img_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(sheared_img_x)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_y)
plt.show()

```

iv)Image Reflection
``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("sea.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,  0,0  ],
                [0,-1,rows],
                [0,0,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0  ],
                [ 0,0,1  ]])
reflect_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
reflect_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()  


```


v)Image Rotation


``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("wheel.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(in_img,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show() 
```

vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img = cv2.imread("wood.jpg")
in_img = cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.imshow(in_img)
plt.show()
cropped_img=in_img[2000:3000 ,1000:2500]
plt.imshow(cropped_img)
plt.show()
```

## Output:

### ORINGINAL IMAGE:
![image](https://github.com/Nagul71/IMAGE-TRANSFORMATIONS/assets/118661118/88295b75-d208-45a2-a923-2e4aab3ae07e)


### i)Image Translation


![image](https://github.com/Nagul71/IMAGE-TRANSFORMATIONS/assets/118661118/6b209b13-b8a6-4496-b9c5-779b27eb0b7b)


### ii) Image Scaling
#### Original Image
![image](https://github.com/Nagul71/IMAGE-TRANSFORMATIONS/assets/118661118/b7f52453-11af-4f22-b403-303bd624a202)

#### Scaled Image

![image](https://github.com/Nagul71/IMAGE-TRANSFORMATIONS/assets/118661118/2baac832-1126-452d-b871-1fe20fc91057)



### iii)Image shearing
![image](https://github.com/Nagul71/IMAGE-TRANSFORMATIONS/assets/118661118/a528ce3c-a2ce-4ab1-8ca3-b391d3c830d7)
![image](https://github.com/Nagul71/IMAGE-TRANSFORMATIONS/assets/118661118/6f70cd03-042e-4dc4-a25a-40658986ceb3)




### iv)Image Reflection
![image](https://github.com/Nagul71/IMAGE-TRANSFORMATIONS/assets/118661118/c97b784f-bb91-40f6-8b5d-d6810bbe8387)
![image](https://github.com/Nagul71/IMAGE-TRANSFORMATIONS/assets/118661118/aaf3a639-7cb7-4ff5-99b5-bc6b6c8f0435)




### v)Image Rotation
![image](https://github.com/Nagul71/IMAGE-TRANSFORMATIONS/assets/118661118/f18ddbf5-6619-4f07-a719-3c6d169339e9)



### vi)Image Cropping


![image](https://github.com/Nagul71/IMAGE-TRANSFORMATIONS/assets/118661118/fe7f73c9-4e08-492d-8eb5-c3195ac98fa3)
![image](https://github.com/Nagul71/IMAGE-TRANSFORMATIONS/assets/118661118/7cf49f6b-3308-411c-a2c5-064cff757bdc)





## Result:
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
