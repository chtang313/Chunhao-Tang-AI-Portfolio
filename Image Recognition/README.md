# 🐾 Computer Vision Image Recognition – Lab 08

A hands-on introduction to how images are represented, visualized, and preprocessed for basic computer vision workflows. This project shows how raw image data is turned into usable input for machine learning models using Python.

---

## 📌 Overview

This lab focuses on building intuition for image processing and computer vision:

- Understanding RGB channels and how images are stored as arrays  
- Displaying individual R / G / B channels  
- Converting images into NumPy arrays  
- Loading datasets using `glob`  
- Reading images with Matplotlib (`plt`) and OpenCV (`cv2`)  
- Applying key preprocessing operations:
  - Resizing  
  - Grayscale conversion  
  - Blurring  
  - Sharpening  
  - Upscaling  

---

## 🧰 Technologies & Libraries

- **NumPy** – Array manipulation and numerical operations  
- **Matplotlib** – Image visualization  
- **OpenCV (cv2)** – Image decoding, processing, and transformations  
- **glob** – Loading groups of image files  
- **pandas** – General data utilities and helpers  

---

## 📂 Dataset

The lab uses a simplified **Cats vs Dogs** dataset to demonstrate basic image workflows.

Example file loading (conceptual):

```
from glob import glob

cat_files = glob('/input/cat-and-dog/training_set/training_set/cats/*.jpg')
dog_files = glob('/input/cat-and-dog/training_set/training_set/dogs/*.jpg')
```

Random samples from each class are selected for visualization and experimentation.

---

## 🖼️ Project Highlights

### 1️⃣ Image Channels

- Splits RGB images into their red, green, and blue channels  
- Visualizes each channel independently  
- Shows how each channel contributes to the final color image  

### 2️⃣ Reading Images

- Compares `plt.imread()` (RGB) and `cv2.imread()` (BGR)  
- Demonstrates how channel ordering affects displayed colors  
- Ensures correct visualization depending on the library used  

### 3️⃣ Preprocessing Techniques

Includes examples of core OpenCV operations such as:

```
cv2.resize(...)
cv2.cvtColor(...)
cv2.GaussianBlur(...)
cv2.filter2D(... )  # Sharpening kernel
```

These operations form the backbone of many modern computer vision pipelines.

### 4️⃣ Dataset Handling

- Loads image paths using `glob`  
- Previews cat and dog images  
- Shows how to iterate through subsets of images for future training or feature extraction  

---

## 📘 Learning Outcomes

By completing this lab, you learn:

- How pixel and channel data represent images numerically  
- Practical differences between common image-reading libraries  
- How to visualize and isolate individual RGB channels  
- Core preprocessing steps used in ML and CV workflows  
- Basic dataset management patterns for image-based machine learning tasks  

---

## 📎 References

- High-level guides and tutorials on Python-based image processing and OpenCV  
- Online articles explaining preprocessing techniques, filters, and practical CV workflows  

(Links omitted here in the README to keep the project self-contained and respectful of external content copyrights.)
```
