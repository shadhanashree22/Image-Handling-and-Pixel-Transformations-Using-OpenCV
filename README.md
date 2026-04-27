# IMAGE-MODELLING-AND-PIXEL-TRANSFORMATION-USING-OPENCV

## Experiment No: 1

## Name:
S V SHADHANASHREE

## Register Number:
212223230202

## AIM
To perform image modelling and pixel transformations using OpenCV.

## Software Required
- Anaconda - Python 3.7  
- OpenCV  
- Matplotlib  
- Jupyter Notebook  

## Algorithm

### Step 1:
Read the input image `Qno.1.jpg` using OpenCV and display it using Matplotlib.

### Step 2:
Perform drawing operations on the image:
- Draw a line from the top-left to bottom-right.
- Draw a circle at the center of the image.
- Draw a rectangle around the image.
- Add the text "OpenCV Drawing" at the top-left corner.

### Step 3:
Perform color space transformations:
- Convert RGB to HSV and display it.
- Convert RGB to GRAY and display it.
- Convert RGB to YCrCb and display it.
- Convert the HSV image back to RGB.

### Step 4:
Modify pixel values by changing a selected block of pixels to white.

### Step 5:
Resize the original image to half its size and display it.

### Step 6:
Crop a Region of Interest (ROI) from the image and display it.

### Step 7:
Flip the image:
- Horizontally  
- Vertically  

### Step 8:
Save the final modified image to the local directory.

---

## PROGRAM

### **Step 1: Read and Display Image**
```python
import cv2
import matplotlib.pyplot as plt

img = cv2.imread('Qno.1.jpg', cv2.IMREAD_COLOR)

img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

plt.imshow(img_rgb)
plt.title("Original Image")
plt.axis('off')
plt.show()
```

### **Step 2: Draw a Line**
```python
line_img = cv2.line(img_rgb,(0,0),(768,600),(255,0,0),2)

plt.imshow(line_img)
plt.title("Image with Line")
plt.axis('off')
plt.show()
```

### **Step 3: Draw a Circle**
```python
circle_img = cv2.circle(img_rgb,(400,300),150,(255,0,0),10)

plt.imshow(circle_img)
plt.title("Image with Circle")
plt.axis('off')
plt.show()
```

### **Step 4: Draw a Rectangle**
```python
rectangle_img = cv2.rectangle(
img_rgb,(0,0),(768,600),(0,0,255),10
)

plt.imshow(rectangle_img)
plt.title("Image with Rectangle")
plt.axis('off')
plt.show()
```

### **Step 5: Add Text**
```python
text_img = cv2.putText(
img_rgb,
"OpenCV Drawing",
(10,30),
cv2.FONT_HERSHEY_SIMPLEX,
1,
(255,255,255),
10
)

plt.imshow(text_img)
plt.title("Image with Text")
plt.axis('off')
plt.show()
```

### **Step 6: Convert RGB to HSV**
```python
image_hsv = cv2.cvtColor(
img_rgb,
cv2.COLOR_RGB2HSV
)

plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis('off')
plt.show()
```

### **Step 7: Convert RGB to Gray**
```python
image_gray = cv2.cvtColor(
img_rgb,
cv2.COLOR_RGB2GRAY
)

plt.imshow(image_gray,cmap='gray')
plt.title("Gray Image")
plt.axis('off')
plt.show()
```

### **Step 8: Convert RGB to YCrCb**
```python
image_ycrcb = cv2.cvtColor(
img_rgb,
cv2.COLOR_RGB2YCrCb
)

plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis('off')
plt.show()
```

### **Step 9: Convert HSV back to RGB**
```python
image_hsv_to_rgb = cv2.cvtColor(
image_hsv,
cv2.COLOR_HSV2RGB
)
```

### **Step 10: Modify Pixel Block**
```python
img[200:500,200:500]=[255,255,255]

plt.imshow(cv2.cvtColor(
img,
cv2.COLOR_BGR2RGB
))
plt.show()
```

### **Step 11: Resize Image**
```python
resized_image=cv2.resize(
img,
(768//2,600//2)
)

plt.imshow(
cv2.cvtColor(
resized_image,
cv2.COLOR_BGR2RGB
)
)
plt.show()
```

### **Step 12: Crop ROI**
```python
roi=img[50:350,50:350]

plt.imshow(
cv2.cvtColor(
roi,
cv2.COLOR_BGR2RGB
)
)
plt.show()
```

### **Step 13: Flip Horizontally**
```python
flipped_horizontally=cv2.flip(img,1)

plt.imshow(
cv2.cvtColor(
flipped_horizontally,
cv2.COLOR_BGR2RGB
)
)
plt.show()
```

### **Step 14: Flip Vertically**
```python
flipped_vertically=cv2.flip(img,0)

plt.imshow(
cv2.cvtColor(
flipped_vertically,
cv2.COLOR_BGR2RGB
)
)
plt.show()
```

### **Step 15: Save Final Image**
```python
cv2.imwrite(
"final_output.jpg",
flipped_horizontally
)
```

## OUTPUT
### Original Image
<img width="620" height="481" alt="image" src="https://github.com/user-attachments/assets/2a7a1c7b-c8a6-4a43-b905-2b045ed331d3" />


### Image with Line
<img width="493" height="409" alt="image" src="https://github.com/user-attachments/assets/89b2039d-4a96-4973-9f61-2dfb4a47bc97" />


### Image with Circle

<img width="493" height="409" alt="image" src="https://github.com/user-attachments/assets/b361f97c-8882-4dd9-a6c7-2f231172c3e3" />


### Image with Rectangle

<img width="493" height="409" alt="image" src="https://github.com/user-attachments/assets/85709d32-de84-4a89-a616-bd76a1d82c42" />


### Image with Text

<img width="493" height="409" alt="image" src="https://github.com/user-attachments/assets/b60ba6b4-9c57-4092-b2d0-409af05f530f" />


### HSV, Gray and YCrCb Images

<img width="493" height="409" alt="image" src="https://github.com/user-attachments/assets/50d08188-7eff-4bca-ad8b-54c03697a161" />


<img width="493" height="409" alt="image" src="https://github.com/user-attachments/assets/6706e725-c7bc-4bef-99ae-412da6adce59" />


<img width="493" height="409" alt="image" src="https://github.com/user-attachments/assets/7e290fe4-4740-4201-837b-5c37ebacbf0b" />




### Resized Image

<img width="493" height="409" alt="image" src="https://github.com/user-attachments/assets/f9c627d2-da64-4609-80f9-e9fc641f19fc" />


### Cropped ROI

<img width="389" height="409" alt="image" src="https://github.com/user-attachments/assets/8ad235c6-ea52-463c-a3ba-586a780a08e2" />


### Flipped Images

<img width="493" height="409" alt="image" src="https://github.com/user-attachments/assets/99a8107f-0a0d-462b-8e39-011620b6331f" />


<img width="493" height="409" alt="image" src="https://github.com/user-attachments/assets/f888ce0d-ecd5-4286-a5ea-a33cc4864921" />



---

## RESULT
Thus image modelling and pixel transformations were performed successfully using OpenCV.
