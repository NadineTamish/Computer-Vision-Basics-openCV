# Intro to Computer Vision – Presentation 

##  Goal of Presentation  
Introduce **Computer Vision (CV)** concepts to **beginners with no AI background** 

---

## Session Overview  

### 1. What is Computer Vision?  
**Definition:**  
Computer Vision is the field of AI that enables computers to “see” and understand the visual world.  

**Analogy:**  
Just like humans use their eyes + brain to recognize objects, computers use cameras + algorithms.  

**Applications:**  
- Face unlock on phones  
- Self-driving cars  
- Medical imaging (detecting tumors, stroke lesions)  
- Augmented reality filters  
- Factory defect detection  

---

### 2. What is an Image?  
- An **image** is a grid of **pixels** (tiny squares).  
- **Grayscale image:**  
  - 1 value per pixel → range [0–255]  
  - 0 = black, 255 = white, values in between = shades of gray  
- **RGB image:**  
  - 3 values per pixel → Red, Green, Blue channels  
  - Combined to form full color images  

---

### 3. How Do Computers See?  
- **Humans see objects** → “this is a cat.”  
- **Computers see numbers** → matrices of pixel intensities.  

To recognize shapes/objects, we need processing steps like:  
- Detecting edges  
- Extracting features  
- Classifying objects  

---

### 4. Image Transformations  
There are two broad categories:  

1. **Filtering** → Changes pixel **values**  
2. **Warping** → Changes pixel **locations** (e.g., rotation, scaling)  

---

### 5. Image Filtering  
- **Point Operations (per-pixel):**  
  Each pixel processed independently.  
  Examples: brightness, contrast, invert.  

- **Neighborhood Operations (“Filters”):**  
  Each pixel updated based on surrounding neighbors.  
  Examples: blur, sharpen, edge detection, noise removal.  

---

### 6. Important Filters  

####  Gaussian Filter  
- A **smoothing filter** that reduces noise.  
- Works by giving higher weight to nearby pixels (bell-curve distribution).  
- Preserves general shapes while removing random noise.  
- Example: removing grain from an old photo.  

####  Sobel Filter  
- An **edge detection filter**.  
- Uses gradients to highlight areas where pixel intensity changes quickly.  
- Detects edges in both **horizontal** and **vertical** directions.  
- Used in object detection and feature extraction.  

####  Box Filter  
- A simple averaging filter.  
- Replaces each pixel with the **average** of its neighborhood.  
- Produces **uniform blurring**.  
- Good for quick smoothing but can blur edges too much.  

####  Median Filter  
- Replaces each pixel with the **median value** of its neighborhood.  
- Excellent for removing **“salt-and-pepper” noise** (random black & white dots).  
- Preserves edges better than Box Filter.  

####  Bilateral Filter  
- A smart filter that **smooths noise** while **keeping edges sharp**.  
- Considers both **pixel intensity difference** and **spatial distance**.  
- Used in photo editing apps for “beautifying” or “denoising” faces.  


---

### 7. Introduction to OpenCV  
**OpenCV** = Open Source Computer Vision Library.  
- Written in C++ with Python bindings.  
- Used in robotics, research, and AI projects.  

**Basic Example in Python:**  
```python
import cv2

# Load an image
img = cv2.imread("image.jpg")

# Display the image
cv2.imshow("Image", img)
cv2.waitKey(0)

```
---
### 8. Useful Links

**numpy videos**

https://www.youtube.com/watch?v=xECXZ3tyONo
https://www.youtube.com/watch?v=uRsE5WGiKWo
