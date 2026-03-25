# Digital-Image-Processing-CNN
CNN-based Digital Image Processing project with feature visualization and performance analysis
# Lightweight CNN for Image Classification
> CIFAR-10 image classification with CLAHE preprocessing, data augmentation, and feature map visualization

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat-square)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-orange?style=flat-square)
![OpenCV](https://img.shields.io/badge/OpenCV-CLAHE-green?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-Google%20Colab-yellow?style=flat-square)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square)

---

## Project Overview
This project builds a **lightweight Convolutional Neural Network (CNN)** trained on a stratified 
10,000-image subset of the CIFAR-10 dataset. It incorporates CLAHE-based contrast enhancement, 
data augmentation, and convolutional feature map visualization to analyze what the model learns 
at each layer depth.

---

## Tech Stack
| Tool | Purpose |
|------|---------|
| TensorFlow / Keras | Model building & training |
| OpenCV | CLAHE contrast enhancement |
| scikit-learn | Stratified sampling & metrics |
| NumPy | Data manipulation |
| Matplotlib / Seaborn | Visualization |
| Google Colab (GPU) | Training environment |

---

## Dataset
- **Source:** [CIFAR-10](https://www.cs.toronto.edu/~kriz/cifar.html)
- **Full dataset:** 60,000 images across 10 classes
- **Subset used:** 10,000 images (stratified sampling)
- **Split:** Organized into `train/`, `val/`, and `test/` folders by class
  - Training: 8,500 images
  - Validation: 1,000 images
  - Test: 1,500 images

---

## Model Architecture
```
Input (32x32x3)
    ↓
Conv Block 1 → Conv2D + BatchNorm + MaxPooling
    ↓
Conv Block 2 → Conv2D + BatchNorm + MaxPooling
    ↓
Conv Block 3 → Conv2D + BatchNorm + MaxPooling
    ↓
Global Average Pooling
    ↓
Dense Output (Softmax, 10 classes)
```
- **Early stopping** monitored on validation loss
- **Lightweight design** — optimized for efficiency

---

## How to Run

### Prerequisites
```bash
pip install tensorflow opencv-python scikit-learn matplotlib seaborn numpy
```

### Steps
1. Open the `.ipynb` file in **Google Colab**
2. Enable GPU runtime:
   `Runtime → Change runtime type → GPU`
3. Run cells in order:
   - **Cell 1–2:** Download CIFAR-10 & stratified sampling
   - **Cell 3–4:** Preprocessing (CLAHE, normalization, augmentation)
   - **Cell 5–6:** Build & train the CNN model
   - **Cell 7–8:** Evaluate performance & generate confusion matrix
   - **Cell 9–10:** Feature map visualizations

---

## Results
| Metric | Score |
|--------|-------|
| Test Accuracy | XX% |
| Precision | XX% |
| Recall | XX% |
| F1-Score | XX% |

> 📝 Replace XX% with your actual numbers from the notebook output

---

## Preprocessing Pipeline
- **CLAHE** — Contrast Limited Adaptive Histogram Equalization
- **Normalization** — Pixel values scaled to [0, 1]
- **Augmentation:**
  - Random horizontal flips
  - Random rotations
  - Random translations
  - Random zoom

---

## Feature Map Visualization
Visualizes activations from each convolutional layer to show:
- **Layer 1** — edges and basic textures
- **Layer 2** — shapes and patterns
- **Layer 3** — high-level object features

---

## Repository Structure
```
Digital-Image-Processing-CNN/
│
├── CNN_Classification.ipynb   # Main notebook
├── README.md                  # Project documentation
└── outputs/
    ├── confusion_matrix.png
    ├── training_curves.png
    └── feature_maps.png
```

---

## Author
**Prathyusha Pentam**
MS in Data Science — Texas A&M University–Corpus Christi
[GitHub](https://github.com/Prathyusha263)

---

## License
This project is for academic and portfolio purposes.
