# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
##Step1:
Import the necessary libraries and read the original image and save it a image variable.

##Step2:
Translate the image using Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]]) Translated_image=cv2.warpPerspective(org_img,Translation_matrix,(col,row))

##Step3:
Scale the image using Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]]) Scaled_image=cv2.warpPerspective(org_img,Scaling_Matrix,(col,row))

##Step4:
Shear the image using Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]]) Sheared_image=cv2.warpPerspective(org_img,Shearing_matrix,(col2,int(row1.5)))

##Step5:
Reflection of image can be achieved through the code Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]]) Reflected_image_row=cv2.warpPerspective(org_img,Reflection_matrix_row,(col,int(row)))

##Step6:
Rotate the image using Rotation_angle=np.radians(10) Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0], [np.sin(Rotation_angle),np.cos(Rotation_angle),0], [0,0,1]]) Rotated_image=cv2.warpPerspective(org_img,Rotation_matrix,(col,(row)))

##Step7:
Crop the image using cropped_image=org_img[10:350,320:560]

##Step8:
Display all the Transformed images.

## Program:
```python
Developed By:S. MEENA
Register Number:2122212400895

i)Image Translation
Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]])
Translated_image=cv2.warpPerspective(original_img,Translation_matrix,(col,row))
plt.axis("off")
plt.imshow(Translated_image)

ii) Image Scaling
Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]])
Scaled_image=cv2.warpPerspective(original_img,Scaling_Matrix,(col,row))
plt.axis("off")
plt.imshow(Scaled_image)


iii)Image shearing
Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]])
Sheared_image=cv2.warpPerspective(original_img,Shearing_matrix,(col*2,int(row*1.5)))
plt.axis("off")
plt.imshow(Sheared_image)


iv)Image Reflection
Reflection_matrix_col=np.float32([[-1,0,col],[0,1,0],[0,0,1]])
Reflected_image_col=cv2.warpPerspective(original_img,Reflection_matrix_col,(col,int(row)))
plt.axis("off")
plt.imshow(Reflected_image_col)
Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]])
Reflected_image_row=cv2.warpPerspective(original_img,Reflection_matrix_row,(col,int(row)))
plt.axis("off")
plt.imshow(Reflected_image_row)



v)Image Rotation
Rotation_angle=np.radians(10)
Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0],
                                [np.sin(Rotation_angle),np.cos(Rotation_angle),0],
                                [0,0,1]])
Rotated_image=cv2.warpPerspective(original_img,Rotation_matrix,(col,(row)))
plt.axis("off")
plt.imshow(Rotated_image)

vi)Image Cropping
cropped_image=original_img[10:350,320:560]
plt.axis("off")
plt.imshow(cropped_image)



vi)Image Cropping
import  numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("teddy.png)
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow()
rows,cols,dim=input_img.shape
M=np.float32([1.5,0,0],[0,2,0],[0,0,1])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.ais('off')
plt.imshow(scaled_img)
plt.show()

```
## Output:
### i)Image Translation
![sc](https://user-images.githubusercontent.com/94677128/166959964-5127e32b-fe77-4c07-9b62-fb23f8e80db6.png)

### ii) Image Scaling
![Screenshot (45)](https://user-images.githubusercontent.com/94677128/166960193-fc93b38b-1249-483b-9495-f98804889255.png)



### iii)Image shearing
![searing](https://user-images.githubusercontent.com/94677128/166957577-b25b570d-2dbe-456f-a72c-21395d7e8699.png)



### iv)Image Reflection
![reflection](https://user-images.githubusercontent.com/94677128/166957948-b0bf28ad-9c97-4d39-8a46-f6bb5a38569f.png)




### v)Image Rotation
![rotate](https://user-images.githubusercontent.com/94677128/166959270-ef396c79-e9ce-4ae9-ab73-f51686f488b5.png)



### vi)Image Cropping
![cropping](https://user-images.githubusercontent.com/94677128/166958367-656f92b8-9f73-414d-9d0c-f3288f4a34dd.png)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
