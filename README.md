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
Developed By: Rakesh J.S
Register Number: 212222230115
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

### (i) Image Translation
<br>
<br>

![image](https://github.com/KANISHKAR2607/IMAGE-TRANSFORMATIONS/assets/118886772/5ef8771e-5b26-4364-bb9f-76c9067cad73) ![image](https://github.com/KANISHKAR2607/IMAGE-TRANSFORMATIONS/assets/118886772/a689e0f0-5012-4a26-bf60-75f2bad69c06)





<br>
<br>

### (ii) Image Scaling
<br>
<br>

![image](https://github.com/KANISHKAR2607/IMAGE-TRANSFORMATIONS/assets/118886772/b080c5b0-3bc8-4642-a7d8-b57dc62c871d) ![image](https://github.com/KANISHKAR2607/IMAGE-TRANSFORMATIONS/assets/118886772/eebe805c-f0b5-411d-a5f5-de0aa7144ca0)





<br>
<br>


### (iii) Image shearing
<br>
<br>

![image](https://github.com/KANISHKAR2607/IMAGE-TRANSFORMATIONS/assets/118886772/2a4e4646-2b45-4c94-a807-39273f45141b) ![image](https://github.com/KANISHKAR2607/IMAGE-TRANSFORMATIONS/assets/118886772/4e65674d-cd9c-4099-aec8-58305e88e46f)




<br>
<br>


### (iv) Image Reflection


#### Reflecting Horizontally

![image](https://github.com/KANISHKAR2607/IMAGE-TRANSFORMATIONS/assets/118886772/834c6f27-e4fa-481e-a38d-aa8769115eb5) ![image](https://github.com/KANISHKAR2607/IMAGE-TRANSFORMATIONS/assets/118886772/8b859359-b271-4bff-98da-417b232613a4)




#### Reflecting Vertically

![image](https://github.com/KANISHKAR2607/IMAGE-TRANSFORMATIONS/assets/118886772/834c6f27-e4fa-481e-a38d-aa8769115eb5) ![image](https://github.com/KANISHKAR2607/IMAGE-TRANSFORMATIONS/assets/118886772/bc10d84a-7cf7-43df-90a8-b20e84242345)




#### Reflecting Horizontally & Vertically


![image](https://github.com/KANISHKAR2607/IMAGE-TRANSFORMATIONS/assets/118886772/834c6f27-e4fa-481e-a38d-aa8769115eb5) ![image](https://github.com/KANISHKAR2607/IMAGE-TRANSFORMATIONS/assets/118886772/26a1324c-bc48-4206-a877-5d3fb49a7564)


<br>
<br>


### (v) Image Rotation
<br>
<br>

![image](https://github.com/KANISHKAR2607/IMAGE-TRANSFORMATIONS/assets/118886772/c11d65bc-f6cc-4f6e-b1ac-1bdb7e2d6dbf) ![image](https://github.com/KANISHKAR2607/IMAGE-TRANSFORMATIONS/assets/118886772/2e4ce3df-b6cc-4c59-a6b9-bc1fb526f7bf)




<br>
<br>



### (vi) Image Cropping
<br>
<br>

![image](https://github.com/KANISHKAR2607/IMAGE-TRANSFORMATIONS/assets/118886772/9cced89b-d2df-4f68-aff7-5dd9b997533d) ![image](https://github.com/KANISHKAR2607/IMAGE-TRANSFORMATIONS/assets/118886772/0a847c66-7cb6-43dd-b470-f1bb7a155763)



<br>
<br>










## Result:
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
