# 🖼️ Object Background Removal using OpenCV

A lightweight and effective background removal pipeline built using **Python** and **OpenCV**, based purely on classical image processing—no deep learning required.  
The project removes backgrounds from still-object images and outputs **transparent PNGs** while preserving object quality.

---

## 🚀 Features
- Removes background from still-object images  
- Based on **Canny Edge Detection + Contours + Mask Smoothing**  
- Outputs **RGBA images** with transparent backgrounds  
- Batch processes all images in a folder  
- Maintains original resolution and object detail  

---

## 🧠 How the Algorithm Works

The background removal pipeline proceeds through the following steps:

### **1. Convert to Grayscale**
Prepares the image for edge-based processing.

### **2. Edge Detection (Canny)**
Extracts strong edges outlining the object.

### **3. Morphological Filtering**
Dilation + erosion strengthen edges and remove small artifacts.

### **4. Contour Detection**
Contours are extracted and filled to create a binary object mask.

### **5. Mask Smoothing**
Blurring and smoothing operations soften the transitions and avoid jagged edges.

### **6. Foreground Masking**
The object is blended with a white background using the smoothed mask.

### **7. Alpha Channel Addition**
The white background is replaced with transparency, producing a clean **RGBA** output.

---

## 🛠️ Usage Instructions

### **1. Open the notebook**
Open and run **BackgroundRemoval.ipynb** in:
- Jupyter Notebook  
- JupyterLab  
- VS Code with Python extension  

### **2. Prepare images**
Place your input images inside the folder referenced in the notebook (e.g., `base_objects/`).

### **3. Run the notebook**
Run all cells to generate PNG images with fully transparent backgrounds.  
Processed images will be saved automatically in the output folder (e.g., `result_removed_background/`).

---

## 📉 Known Limitations

Since the project uses purely classical image processing filters:

- Glossy or reflective objects may produce inaccurate edges  
- Backgrounds similar in color to the object may not be fully removed  
- Performance decreases with complex lighting, shadows, or busy backgrounds  
- Not designed for human segmentation or complex scenes  

---

## 📜 License

This project is open-source and available under the **MIT License**.
