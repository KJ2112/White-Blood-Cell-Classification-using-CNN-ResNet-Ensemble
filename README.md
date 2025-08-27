# 🧬 White Blood Cell Classification using CNN & ResNet Ensemble  
Deep learning project for medical image analysis. Trained a custom CNN and ResNet-based ensemble to classify White Blood Cells (WBCs) into Neutrophils, Lymphocytes, Eosinophils, and Monocytes. Achieved 98.7% accuracy.
## 📌 Project Overview  
Accurate **White Blood Cell (WBC) classification** is crucial for hematological diagnosis, but manual analysis under a microscope is **time-consuming and error-prone**.  
This project leverages **deep learning** to automate WBC subtype classification. We trained an **ensemble of a custom CNN and ResNet-based model** on annotated blood smear images, achieving **98.7% accuracy**.  

The model classifies a given WBC into one of four classes:  
- **Neutrophils**  
- **Lymphocytes**  
- **Eosinophils**  
- **Monocytes**  

## 🎯 Objectives  
- Automate **WBC classification** from blood smear images.  
- Improve accuracy using **ensemble learning** (Custom CNN + ResNet).  
- Apply **data augmentation** and preprocessing to handle dataset variability.  
- Compare model performance across CNN, ResNet, MobileNet, and ensemble methods.  

## 🛠️ Methodology  
- **Dataset:** Publicly available WBC dataset with annotated RBC + single WBC images.  
- **Preprocessing:**  
  - Resized images to 224×224 px.  
  - Pixel normalization.  
  - Data augmentation (rotation, flipping, zooming).  
- **Models Used:**  
  - **Custom CNN** (Conv + BatchNorm + MaxPooling + Dropout).  
  - **MobileNetV2** (fine-tuned on dataset).  
  - **ResNet50** (residual blocks with skip connections).  
- **Ensemble:** Combined CNN + MobileNet predictions using majority voting for higher robustness.  

## 📊 Results  
| Model       | Accuracy |  
|-------------|----------|  
| CNN         | 96.2%    |  
| ResNet50    | 86.0%    |  
| MobileNetV2 | 93.8%    |  
| **Ensemble (CNN + MobileNet)** | **98.7%** |  

- Ensemble improved **precision, recall, and F1** across all classes.  
- Confusion matrices confirm robust performance across Neutrophils, Lymphocytes, Monocytes, and Eosinophils.  

## 📂 Repository Structure  

```text
 └── Blood_cell_detection.ipynb # Main training & evaluation notebook
 └── PROJECT_REPORT.pdf # Detailed project report
 └──README.md


## 🚀 How to Run  
1. Clone the repo:  
   ```bash
   git clone https://github.com/<your-username>/wbc-classification.git
   cd wbc-classification
2.Install dependencies
 pip install -r requirements.txt
3.Run the notebook
 jupyter notebook notebooks/Blood_cell_detection.ipynb
  
