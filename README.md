# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
```
i) import numpy as np
   import cv2
   from google.colab.patches import cv2_imshow
   imread=cv2.imread("/content/image1.png.png")
   cv2_imshow(image)

ii) imagecv2_imread("/content/image1.png.png",0)
    cv2_imshow(image)

iii)import cv
    import numpy as np
    from google.colab.patches import cv2_imshow
    image = cv2.imread('/content/image1.png.png')
    height, width, channels = image.shape

    print("Height:", height)
    print("Width:", width)
    print("Number of channels:", channels)

iv)
!pip install opencv-python
import numpy as np
import cv2
from google.colab.patches import cv2_imshow
image = cv2.imread('/content/image1.png.png', 0)
cv2_imshow(image)
color_image = cv2.cvtColor(image, cv2.COLOR_GRAY2BGR)
import random
for i in range(100):
    for j in range(color_image.shape[1]):
        color_image[i][j] = [random.randint(0, 255), random.randint(0, 255), random.randint(0, 255)]
cv2_imshow(color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

v) 
import numpy as np
import cv2
from google.colab.patches import cv2_imshow
color_image = cv2.cvtColor(image, cv2.COLOR_GRAY2BGR)
import random
for i in range(100):
    for j in range(color_image.shape[1]):
        color_image[i][j] = [random.randint(0, 255), random.randint(0, 255), random.randint(0, 255)]
tag = color_image[300:400, 300:400]
resized_tag = cv2.resize(tag, (100 ,100))
color_image[50:150, 50:150] = resized_tag
cv2_imshow(color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
vi)
import numpy as np
import cv2
from google.colab.patches import cv2_imshow
house_color_image = cv2.imread("/content/image1.png.png")
cv2_imshow(house_color_image)

hsv_image = cv2.cvtColor(house_color_image, cv2.COLOR_BGR2HSV)
hsv_image1 = cv2.cvtColor(house_color_image, cv2.COLOR_BGR2HSV)
gray_image = cv2.cvtColor(house_color_image, cv2.COLOR_BGR2GRAY)
gray_image1 = cv2.cvtColor(house_color_image, cv2.COLOR_BGR2GRAY)
cv2_imshow(hsv_image)
cv2_imshow(hsv_image1)
cv2_imshow(gray_image)
cv2_imshow(gray_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()
vii)
import cv2
import numpy as np
from google.colab.patches import cv2_imshow
image = cv2.imread('/content/image1.png.png')
hsv_image = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
rgb_image = cv2.cvtColor(hsv_image, cv2.COLOR_HSV2RGB)
bgr_image = cv2.cvtColor(hsv_image, cv2.COLOR_HSV2BGR)
cv2_imshow(image)
cv2_imshow(rgb_image)
cv2_imshow(bgr_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
viii)
import cv2
import numpy as np
from google.colab.patches import cv2_imshow
image = cv2.imread('/content/image1.png.png')
ycrcb_image = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2_imshow(image)
cv2_imshow(ycrcb_image)
# Wait for a key press and close all windows
cv2.waitKey(0)
cv2.destroyAllWindows()
ix)
import cv2
import numpy as np
from google.colab.patches import cv2_imshow
image = cv2.imread('/content/image1.png.png')
b, g, r = cv2.split(image)
merged_image = cv2.merge([b, g, r])
cv2_imshow(image)
cv2_imshow(merged_image)

# Wait for a key press and close all windows
cv2.waitKey(0)
cv2.destroyAllWindows()
x)
import cv2
import numpy as np
from google.colab.patches import cv2_imshow
image = cv2.imread('/content/image1.png.png')
hsv_image = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv_image)
merged_hsv_image = cv2.merge([h, s, v])
merged_bgr_image = cv2.cvtColor(merged_hsv_image, cv2.COLOR_HSV2BGR)
cv2_imshow(image)
cv2_imshow(merged_bgr_image)

# Wait for a key press and close all windows
cv2.waitKey(0)
cv2.destroyAllWindows()


```
### Developed By:MARELLA HASINI
### Register Number:212223240083 


## Output:

### i) Read and display the image
<br>![OUTPUT](<read and display.png>)

### ii)Write the image

<br>![output](<write image.png>)
### iii)Shape of the Image

<br>![OUTPUT](<shape of image.png>)

### iv)Access rows and columns
<br>![OUTPUT](<access rows and columns.png>)

### v)Cut and paste portion of image
<br>![OUTPUT](<cut and paste.png>)

### vi) BGR and RGB to HSV and GRAY
<br>![OUTPUT](<bgr and rgb to hsv and gray.png>)
![OUTPUT](<bgr and rgb to hsv and gray 2.png>)
![OUTPUT](<bgr and rgb to hsv and gray 3.png>)

### vii) HSV to RGB and BGR
<br>![OUTPUT](<hsv to rgb and bgr.png>)
![OUTPUT](<hsv to rgb and bgr2.png>)

### viii) RGB and BGR to YCrCb
<br>![OUTPUT](<RGB and BGR to YCrCb.png>)

### ix) Split and merge RGB Image
<br>![OUTPUT](<split rgb (2).png>)

### x) Split and merge HSV Image
<br>![OUTPUT](<split HSV-2.png>)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.





