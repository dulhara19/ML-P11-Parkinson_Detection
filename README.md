# Parkinson's Disease Detection Using Voice Features 

This project implements a machine learning pipeline to detect Parkinson's disease using voice-based features. We apply dimensionality reduction (PCA) and feature selection (Mutual Information) techniques, and compare their performance using a Random Forest Classifier.

---
## Dataset

We used the [`parkinsons.data`](https://archive.ics.uci.edu/ml/datasets/parkinsons) dataset from the UCI Machine Learning Repository. It contains biomedical voice measurements from people with and without Parkinson's disease.

### Key Features:

- **MDVP:Fo(Hz)** – Average vocal fundamental frequency  
- **MDVP:Fhi(Hz)** – Maximum vocal fundamental frequency  
- **MDVP:Flo(Hz)** – Minimum vocal fundamental frequency  
- **MDVP:Jitter(%)**, **MDVP:Shimmer** – Variations in pitch and amplitude  
- **NHR**, **HNR** – Noise-to-Harmonics ratio, etc.  
- **status** – Target variable (1 = Parkinson's, 0 = Healthy)

---

## Objectives

- Perform **Exploratory Data Analysis (EDA)** on the dataset  
- Apply **Mutual Information (MI)** to select top 10 features  
- Apply **Principal Component Analysis (PCA)** to reduce dimensionality  
- Train a **Random Forest Classifier** using both MI and PCA features  
- Compare model performances  
- Visualize **confusion matrix**, **ROC curve**, and other evaluation metrics  
- Lay groundwork for **voice-capturing application for real-time analysis**

---

## Tech Stack

- **Python**  
- **Pandas**, **NumPy**, **Matplotlib**, **Seaborn**  
- **Scikit-learn** (RandomForest, PCA, MI)  
- **Librosa**, **sounddevice** (for future voice capture and feature extraction)

---

## Model Performance

### Using Mutual Information (Top 10 features):
- **Accuracy**: 87%
- **F1 Score**: 0.87

### Using PCA (8 components):
- **Accuracy**: 92%
- **F1 Score**: 0.91

➡️ **PCA-based model showed better performance and was selected as final**
---

## 🔉 Future Scope: Voice-Based Medical Screening App

We plan to extend this project to create a real-time voice analysis app capable of:
- Recording voice via microphone
- Extracting features (MFCC, jitter, shimmer, etc.)
- Predicting neurological conditions like **Autism** or **Parkinson’s**
- Giving real-time feedback and results

---

## How to Run

1. Clone this repo:
    ```bash
    git clone https://github.com/yourusername/parkinsons-voice-detector.git
    cd parkinsons-voice-detector
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the notebook:
    - Open `Parkinson_Detection.ipynb` in **Google Colab** or **Jupyter Notebook**

---

## 🤝 Contributions

Open for collaboration! Feel free to open an issue or submit a pull request if you’d like to improve the model, add real-time voice capture, or extend to other disorders.

---

## 👨‍💻Author

Developed by DULHARA :)
