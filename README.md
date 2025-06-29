# 🧠 Parkinson’s Disease Prediction using Machine Learning

This project implements a machine learning model to predict whether a person has Parkinson’s disease based on biomedical voice measurements. The model uses 22 voice-related features to assess the likelihood of Parkinson’s, providing a quick and non-invasive diagnostic aid.

---

## Dataset

The dataset used originates from the [UCI Parkinson’s Disease Dataset](https://archive.ics.uci.edu/ml/datasets/parkinsons) and includes 195 voice recordings with 23 attributes (22 features + 1 target).

| Feature Type               | Examples                          |
|----------------------------|-----------------------------------|
| Fundamental Frequencies    | `MDVP:Fo(Hz)`, `MDVP:Fhi(Hz)`      |
| Jitter/Shimmer             | `MDVP:Jitter(%)`, `MDVP:Shimmer`  |
| Noise & Harmonics Ratio    | `NHR`, `HNR`                      |
| Nonlinear Measures         | `RPDE`, `DFA`, `D2`, `PPE`        |

**Target variable:**
- `0`: Healthy
- `1`: Parkinson’s disease

**Dataset characteristics:**
- 147 Parkinson’s cases  
- 48 healthy cases  
- No missing values

---

## Libraries Used

- `numpy` – Numerical operations  
- `pandas` – Data handling  
- `matplotlib` – Visualization  
- `scikit-learn` – Model training, evaluation, and preprocessing  
- `streamlit` – Interactive prediction interface  

---

## Workflow

### 1. Data Loading & Exploration
- Load CSV using pandas  
- Explore distributions, correlation heatmaps, and class balance  

### 2. Data Preprocessing
- Separate features and labels  
- Scale features using `StandardScaler`  
- Split dataset into 80/20 train-test split  

### 3. Model Training
- Classifier: Support Vector Machine (SVM) with RBF kernel  
- Performance metrics: Accuracy, Precision, Recall, F1-score  
- Cross-validation for robustness  

### 4. Evaluation
- Achieved accuracy ~95% on test data  
- Confusion matrix and ROC curve plotted  

### 5. Prediction System
- Takes 22 biomedical voice input features  
- Returns prediction of whether Parkinson’s is likely  

---

## Model Performance

**Final Metrics (SVM Classifier):**
- Accuracy: **95.8%**
- Precision: **94.6%**
- Recall: **97.3%**
- F1 Score: **95.9%**

---

## 🧪 Example Prediction

**Input Features:**  
```
input_data = (197.07600,206.89600,192.05500,0.00289,0.00001,0.00166,0.00168,0.00498,0.01098,0.09700,0.00563,0.00680,0.00802,0.01689,0.00339,26.77500,0.422229,0.741367,-7.348300,0.177551,1.743867,0.085569)
```
**Output:**  
```
[0]
The Person does not have Parkinsons Disease
```


---

## ▶️ How to Run

### Prerequisites
- Python 3.8 or higher  
- pip package manager  

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/your-username/parkinsons-disease-prediction.git
cd parkinsons-disease-prediction
```
2. **Create and activate virtual environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```
4. **Run the Notebook**
```bash
jupyter notebook Parkinsons_Disease_prediction_Model.ipynb
```
Play around and make changes trying different inputs and predictions from the dataset! 


