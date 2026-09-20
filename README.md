# Machine-Learning-Based-Detection-of-Suspicious-Online-Reviews-Using-Optimized-Two-Model-Stacking
# 🧠 Review Authenticity Classification

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-ML-orange?logo=scikit-learn)
![Streamlit](https://img.shields.io/badge/Streamlit-Web_App-red?logo=streamlit)

> A text-classification system for distinguishing genuine product reviews from machine-generated or spam-like review content.

---

## 🔎 Project Summary

Online platforms receive large volumes of user-generated reviews, making automated classification useful for identifying potentially unreliable content.

This project applies **natural language processing (NLP)** and **ensemble machine learning** to classify review text.

The classification pipeline combines:

* TF-IDF feature extraction
* Logistic Regression
* Naïve Bayes
* Stacking-based ensemble learning

An interactive Streamlit application provides a convenient interface for testing individual reviews or processing review datasets.

---

## ✨ Key Capabilities

### 🤖 Ensemble Classification

Combines multiple classification algorithms through a stacked learning architecture.

### 📝 Text Feature Engineering

Transforms review text into numerical representations using **TF-IDF vectorization**.

### 📊 Model Evaluation

Provides classification metrics for evaluating the performance of individual models and the combined ensemble.

### 🌐 Interactive Interface

The Streamlit frontend supports:

* Single-review classification
* Batch review processing
* Model prediction
* Interactive experimentation

### ☁️ Remote Demonstration

The application can be exposed temporarily for demonstrations using services such as **ngrok**.

---

## 📚 Dataset

The project uses a CSV-based review dataset containing approximately **40,000 records**:

| Category             |    Samples |
| -------------------- | ---------: |
| Genuine reviews      |     20,000 |
| AI-generated reviews |     20,000 |
| **Total**            | **40,000** |

Before training, the data undergoes text cleaning and preprocessing using Python data-science libraries.

---

## 🧠 Machine Learning Pipeline

The general workflow is:

```text
Raw Review
    │
    ▼
Text Cleaning
    │
    ▼
Preprocessing
    │
    ▼
TF-IDF Vectorization
    │
    ▼
┌───────────────────────┐
│ Base Classification   │
│                       │
│ Logistic Regression   │
│ Naïve Bayes           │
└───────────┬───────────┘
            │
            ▼
     Stacking Ensemble
            │
            ▼
       Final Prediction
```

This architecture allows the system to compare the behavior of different learners while producing a combined prediction.

---

## 🛠️ Technology Stack

| Technology   | Purpose                        |
| ------------ | ------------------------------ |
| Python 3.10  | Application and ML development |
| Pandas       | Dataset manipulation           |
| NumPy        | Numerical operations           |
| Scikit-learn | Machine-learning pipeline      |
| TF-IDF       | Text feature extraction        |
| Streamlit    | Interactive web interface      |
| ngrok        | Optional remote demonstration  |

---

## 📈 Model Performance

The reported test-set performance is:

**Accuracy: 92.16%**

The stacked model was reported to provide improved precision and recall compared with the individual base classifiers.

> Performance figures depend on the dataset split, preprocessing pipeline, feature configuration, and evaluation methodology. Results should therefore be reproduced locally before being treated as independently verified benchmarks.

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/DarkHackGod/Machine-Learning-Based-Detection-of-Suspicious-Online-Reviews-Using-Optimized-Two-Model-Stacking.git
```

### 2. Enter the project directory

```bash
cd Machine-Learning-Based-Detection-of-Suspicious-Online-Reviews-Using-Optimized-Two-Model-Stacking
```

### 3. Create a virtual environment

```bash
python3 -m venv .venv
```

Activate it on Linux/macOS:

```bash
source .venv/bin/activate
```

On Windows:

```powershell
.venv\Scripts\activate
```

```

The application will provide a local address that can be opened in your browser.

---

## 📂 Suggested Project Structure

```text
project/
├── app.py
├── dataset/
│   └── reviews.csv
├── models/
├── notebooks/
├── requirements.txt
├── README.md
└── .gitignore
```

The exact structure may differ depending on the implementation.

---

## 🧪 Evaluation

Recommended evaluation metrics include:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion matrix

Testing multiple metrics is useful because accuracy alone may not fully describe classifier behavior.

---

## 🔮 Possible Improvements

Future development could explore:

* Additional NLP preprocessing techniques
* Hyperparameter optimization
* Additional ensemble architectures
* Cross-validation
* Class imbalance analysis
* Transformer-based text representations
* Model explainability
* Confidence scoring
* Larger and more diverse datasets

---

## ⚠️ Dataset & Model Considerations

Classification results depend heavily on the quality and composition of the training data.

A model trained on a particular collection of genuine and generated reviews may not generalize perfectly to reviews produced by unseen models, writing styles, languages, or platforms.

For this reason, real-world deployment should include additional validation and monitoring.


## 👤 Project Information

This repository demonstrates the application of **NLP, supervised classification, and ensemble learning** to review-authenticity analysis.

Contributions, experiments, and improvements to the model pipeline are welcome.
