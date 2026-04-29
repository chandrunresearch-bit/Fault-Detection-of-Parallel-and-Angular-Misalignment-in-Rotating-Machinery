Fault Detection of Parallel and Angular Misalignment in Rotating Machinery

This project focuses on detecting *shaft misalignment faults* (Parallel and Angular) in rotating machinery using vibration signal analysis and machine learning.

The workflow includes:

* Time-domain signal processing
* Frequency-domain (spectrum) analysis
* Feature extraction
* Class balancing (SMOTE)
* Classification using RF, XGBoost
* Analysis using Autoencoder
* Visualization (Confusion Matrix, Feature Importance, t-SNE)

## 📂 Dataset Structure
The dataset consists of *3 classes*:
Dataset/

 Healthy/
 Misalignment parallel/
 Misalignment angular/


Each folder contains multiple *CSV files* (time-domain and spectrum data).

⚠️ *Important*

* The dataset is provided in .zip format
* You *must extract all zip files* before running the code

---

## 📊 Classes

| Label | Class Name |
| ----- | ---------- |
| 0     | Healthy    |
| 1     | Parallel   |
| 2     | Angular    |

---

## ⚙️ Features Extracted

From vibration signals:

* RMS
* Standard Deviation
* Kurtosis
* Skewness
* Peak-to-Peak
* Crest Factor
* Spectral Entropy
* Frequency Band Energy (Low / Mid / High)

---

## 🧠 Machine Learning Model

* Model: Autoencoder, RF & XGBoost Classifier
* Class balancing: SMOTE
* Validation:

  * Train/Test Split (80/20)
  * 5-Fold Cross Validation

---

## 📈 Outputs

* Spectrum comparison plots
* Harmonic ratio analysis table
* Confusion matrix
* Feature importance graph
* t-SNE visualization

---

# 💻 Running the Project

---

## ✅ Option 1: Run in Local IDE (VS Code / PyCharm / Jupyter)

### 1. Clone Repository

bash
git clone https://github.com/chandrunresearch-bit/Fault-Detection-of-Parallel-and-Angular-Misalignment-in-Rotating-Machinery.git
cd Fault-Detection-of-Parallel-and-Angular-Misalignment-in-Rotating-Machinery

---

### 2. Install Dependencies

bash
pip install numpy pandas scipy scikit-learn matplotlib xgboost lightgbm imbalanced-learn

---

### 3. Extract Dataset

Unzip all dataset files:

Healthy.zip
Misalignment parallel.zip
Misalignment angular.zip

After extraction:

Dataset/
├── Healthy/
├── Misalignment parallel/
└── Misalignment angular/

---

### 4. Update Dataset Path

In the script, change:

python
BASE = "your/local/path/to/Dataset"

Example:

python
BASE = "C:/Users/YourName/Dataset"

---

### 5. Run Script

bash
python Hybrid_VMD_CNN_Autoencoder.ipynb

(or run in Jupyter Notebook)

---

## ☁️ Option 2: Run in Google Colab

---

### 1. Upload Dataset to Google Drive

* Upload extracted dataset folders to:


My Drive/Vibration Results/


---

### 2. Open Notebook in Colab

Upload or open:


Hybrid_VMD_CNN_Autoencoder.ipynb


---

### 3. Install Dependencies

python
!pip install xgboost lightgbm imbalanced-learn -q


---

### 4. Mount Google Drive

python
from google.colab import drive
drive.mount('/content/drive')


---

### 5. Verify Dataset Path

Make sure this matches your Drive:

python
BASE = "/content/drive/My Drive/Vibration Results"


---

### 6. Run All Cells

* Runtime → Run All

---

## ⚠️ Notes

* Angular 1800 RPM data is excluded due to similarity with parallel fault
* Ensure all CSV files exist before running
* t-SNE may take ~1 minute depending on dataset size

---

## 📌 Future Improvements

* Advanced deep learning models 
* Real-time fault detection
* Deployment as web app
The Experimental real time dataset has 3 folders Healthy, Misalignment parallel, Misalignment angular
Each folder contains six CSV files
The Experiment was conducted with all csv files
