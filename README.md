# Chest X-Ray Image Processing and Classification

This project was developed as part of my **Summer Internship 2025**, focusing on **medical image processing** and the classification of chest X-rays into **three categories: Pneumonia, COVID-19, and Normal**.  
The study applies state-of-the-art deep learning models to achieve high accuracy in detecting respiratory conditions from radiographic images.

---

## 📊 Datasets

The datasets were collected from Kaggle:

1. [Chest X-Ray Pneumonia](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)  
2. [COVID-19 Radiography Database](https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database)  
3. [COVID-QU Dataset](https://www.kaggle.com/datasets/anasmohammedtahir/covidqu) *(COVID images only)*  

Dataset combination and balancing details are available in [`datasets.md`](datasets.md).

Final class distribution after balancing:

| Class      | Number of Images |
|------------|------------------|
| Pneumonia  | 15,903           |
| COVID-19   | 15,565           |
| Normal     | 13,358           |

---

## ⚙️ Training Setup

- Platform: **Kaggle**  
- Accelerator: **GPU T4 x2**  
- Epochs: **15–20**  
- Image size: **224×224**  
- Framework: **TensorFlow / Keras**  
- Models saved as `.h5` files (users are encouraged to run and save their own models).  

---

## 🧠 Models Implemented

1. **DenseNet121 (Baseline and Improved)**  
   - Pretrained on ImageNet  
   - Fine-tuned for 3-class classification  
   - Best Test Accuracy: **0.9644**  

2. **Hybrid Transformer Model**  
   - Combines CNN feature extraction with transformer layers  
   - Best Accuracy: **0.9355**  

Both implementations are provided in the `notebooks/` folder.

---

## 📈 Results

| Model                  | Accuracy |
|-------------------------|----------|
| Hybrid Transformer      | 0.9355   |
| DenseNet121 (Original)  | 0.9539   |
| DenseNet121 (Improved)  | **0.9644** |

Evaluation metrics include confusion matrices, precision, recall, and F1-scores.  
Plots and outputs are available directly inside the Jupyter notebooks.

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/chest-xray-classification.git
   cd chest-xray-classification

2. Install dependencies:
    pip install -r requirements.txt

3. Run on Kaggle with GPU T4x2:
    - Upload the dataset folders from Kaggle.
    - Open the notebooks in notebooks/.
    - Update dataset paths if necessary.
    - Train the models and save the .h5 files locally.

---

## 📂 Repository Structure
.
├── notebooks/        # Jupyter notebooks for DenseNet121 & Hybrid
├── datasets.md       # Dataset sources & balancing details
├── requirements.txt  # Python dependencies
└── README.md         # Project documentation

---

## 🔮 Future Work

- Experiment with other architectures (EfficientNet, Swin Transformer).
- Apply more advanced data augmentation for robustness.
- Explore explainability methods (Grad-CAM, SHAP) for clinical interpretability.
- Validate results on external hospital datasets for real-world application.

---

## 📚 References

1. Chowdhury, N. K., Rahman, M. M., & Kabir, M. A. (2022). COVID-19 Chest X-ray Classification and Severity Assessment Using Convolutional and Transformer Neural Networks. Applied Sciences, 12(10), 4861. https://doi.org/10.3390/app12104861

2. Kaggle Datasets:
    - Mooney, P. T. Chest X-Ray Pneumonia. https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia
    - Rahman, T. COVID-19 Radiography Database. https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database
    - Tahir, A. M. COVID-QU Dataset. https://www.kaggle.com/datasets/anasmohammedtahir/covidqu
