
## 📌 Project Overview
This project implements a **Multimodal Deep Learning** model using TensorFlow and Keras to predict real estate prices. Unlike traditional models that only use numerical data, this approach combines:
1.  **Tabular Data:** Structural features like square footage, bedrooms, and age.
2.  **Image Features:** Visual data (simulated as 512-dimensional vectors) representing the aesthetic or condition of the property.

The architecture uses a **Late Fusion** technique, where two separate neural network branches are trained independently and then concatenated to make a final price prediction.

---

## 🏗️ Model Architecture
The model consists of two main input branches:

### 1. Tabular Branch
* **Input:** 5 numerical features (`area_sqft`, `bedrooms`, `bathrooms`, `age_years`, `garage`).
* **Structure:** Dense layers (128 → 64) with Dropout (0.3) to prevent overfitting.

### 2. Image Branch
* **Input:** 512-dimensional feature vector (representative of a CNN output like VGG16).
* **Structure:** Dense layers (256 → 128) with Dropout (0.3).

### 3. Fusion & Output
* **Merge:** Concatenation of both branches.
* **Head:** Dense layers (128 → 64) leading to a single linear output for regression.



```bash
pip install numpy pandas tensorflow scikit-learn matplotlib pillow opencv-python joblib
