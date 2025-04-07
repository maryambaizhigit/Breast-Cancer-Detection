# 🧠 Breast Cancer Detection via Ultrasound – Multi-Class Semantic Segmentation

Semantic segmentation of breast ultrasound images using deep learning to detect and classify tissue as **normal**, **benign**, or **malignant**. This project applies medical imaging and computer vision to assist in early breast cancer diagnosis.

---

## 🔍 Project Overview

Breast cancer is one of the leading causes of death among women globally. Early and accurate detection can significantly improve survival rates. This project aims to build a **semantic segmentation model** to identify and delineate regions of concern in **breast ultrasound images**, categorized into:

- **Normal**
- **Benign**
- **Malignant**

The segmentation helps provide detailed, pixel-level classification to support diagnostic decision-making in clinical workflows.

---

## 🧪 Dataset

- **Source:** [Al-Dhabyani et al. (2020), Data in Brief](https://doi.org/10.1016/j.dib.2019.104863)
- **Images:** 780 breast ultrasound images (PNG format, ~500×500 pixels)
- **Patients:** 600 female patients, aged 25–75
- **Labels:** Pixel-level ground truth segmentation masks
- **Classes:**  
  - `0`: Normal  
  - `1`: Benign  
  - `2`: Malignant

---

## 🛠️ Tools & Techniques

- **Framework:** PyTorch  
- **Architecture:** Custom multi-class UNet  
- **Augmentation:** Horizontal/vertical flips, rotation  
- **Loss Function:** Weighted Dice Loss (malignant class weighted 2×)  
- **Evaluation Metric:** Weighted Mean Dice Coefficient

---

## 🎯 Evaluation

The **Weighted Mean Dice Coefficient** was used as the primary evaluation metric:

- **Malignant** class had **2× higher weight** due to its clinical importance.
- Final segmentation model achieved high precision across all three classes, with a focus on **malignant tumor detection**.

---

## 📈 Highlights

- Developed a **custom `MultiClassBUSIDataset`** class for loading and augmenting the dataset.
- Applied **real-time augmentation** for better generalization.
- Designed a training loop with **loss tracking and validation visualizations**.
- Achieved strong segmentation results using **UNet with Dice Loss**.

---

🔗 Citation

Al-Dhabyani W, Gomaa M, Khaled H, Fahmy A.
Dataset of breast ultrasound images.
Data in Brief. 2020 Feb;28:104863.
DOI: 10.1016/j.dib.2019.104863

---
👩‍💻 Author

Maryam Baizhigitova
📍 Boston, MA
📧 mbaizhigitova04@gmail.com
