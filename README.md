# 📘 Amazon Review Sentiment Analysis  
**By Michael Yassa**

This project performs binary sentiment classification on Amazon product reviews using a traditional NLP pipeline. We process real-world review data and train a Logistic Regression model using TF-IDF features to classify reviews as either **positive** or **negative**.

It showcases an end-to-end pipeline from raw data to a trained model with evaluation and a simple interactive input widget.

---

## 🎯 Objectives

- Clean and preprocess Amazon customer review text  
- Extract numerical features using **TF-IDF**  
- Train and evaluate a **Logistic Regression** classifier  
- Analyze performance using precision, recall, F1-score, and confusion matrix  
- Provide an interactive UI for live sentiment prediction  

---

## 📂 Dataset Description

The dataset used is sourced from [fastText's Amazon Reviews](https://fasttext.cc/docs/en/supervised-tutorial.html), available in the following files:
- `train.ft.txt.bz2` — training data  
- `test.ft.txt.bz2` — test data  

Each line in the dataset follows this format:
__label__1 This product was terrible and broke on the first day.
__label__2 This product is amazing and exceeded my expectations.


Where:
- `__label__1` = Negative sentiment (1–2 stars)  
- `__label__2` = Positive sentiment (4–5 stars)  

Neutral reviews (3-star ratings) were intentionally excluded to create a clear binary classification problem.

---

## ⚙️ Project Workflow

1. **Load & Decode Data**: Handle bz2-compressed format efficiently  
2. **Preprocessing**:
   - Lowercasing  
   - Punctuation and non-ASCII removal  
   - Stopword filtering (NLTK)  
   - Optional stemming (PorterStemmer)  
3. **TF-IDF Vectorization**: Convert cleaned text into sparse numerical feature vectors  
4. **Model Training**: Logistic Regression trained on TF-IDF vectors  
5. **Model Evaluation**:  
   - Metrics: Accuracy, Precision, Recall, F1-score  
   - Confusion Matrices for validation and test sets  
6. **Interactive Testing**:  
   - Input your own review with `ipywidgets` and view predicted sentiment

---
## 📒 Project Structure

```
amazon-sentiment-analysis/
│
├── notebooks/
│   └── Sentiment_Analysis.ipynb     # Main Jupyter Notebook
│
├── data/
│   ├── train.ft.txt.bz2             # Training data
│   └── test.ft.txt.bz2              # Test data
│
├── README.md                        # Project overview and instructions
├── requirements.txt                 # List of dependencies
└── .gitignore                       # Files to ignore in version control
```
