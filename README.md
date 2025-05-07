# SpamMessageDetect
文本挖掘-垃圾信息判别
# 📬 Spam Message Recognition using Naive Bayes and Random Forest

A machine learning project that evaluates the effectiveness of Naive Bayes and Random Forest models in classifying SMS messages as spam or ham. The study includes feature selection methods, hyperparameter tuning, and multiple evaluation metrics.

---

## 📁 Dataset

- **Name**: SMS Spam Collection Dataset  
- **Size**: 5,574 messages  
- **Labels**: `ham` (legitimate) or `spam`  
- **Format**: Two columns – `v1` (label), `v2` (text message)  
- **Source**: Public domain, collected for academic research

---

## 🎯 Project Objectives

- Compare Naive Bayes and Random Forest performance in spam detection
- Apply and assess different feature selection techniques
- Tune model parameters via cross-validation
- Evaluate using precision, recall, and confusion matrix

---

## ⚙️ Methodology

### 🔹 Text Vectorization
- **TF-IDF**: Converts text into numerical matrix `[5572 x 8709]`

### 🔹 Feature Selection (Top 3000)
- **Chi-Squared**
- **Mutual Information**

### 🔹 Classification Models
- **Naive Bayes**
  - Best smoothing parameter: α = 0.1
- **Random Forest**
  - Best parameters: 
    - `n_estimators = 60`, `max_features = 'sqrt'` (Chi-Squared)
    - `n_estimators = 40`, `max_features = 'sqrt'` (Mutual Information)

### 🔹 Evaluation Metrics
- Confusion Matrix
- Precision & Recall
- 5-Fold Cross-Validation for tuning

---

## 📊 Results

| Model         | Feature Selection | Precision | Recall   | Time     |
|---------------|-------------------|-----------|----------|----------|
| Naive Bayes   | Chi-Squared       | 100%      | 89.71%   | < 2 sec  |
| Naive Bayes   | Mutual Info       | 99.19%    | 89.70%   | < 2 sec  |
| Random Forest | Chi-Squared       | 100%      | 87.5%    | > 40 sec |
| Random Forest | Mutual Info       | 100%   03%   | > 40 sec |

---

## 🧠 Key Insights

- Both models achieved **100% precision**, meaning no legitimate messages were classified as spam.
- **Naive Bayes** performed faster and achieved slightly better recall than Random Forest.
- **Chi-Squared** feature selection yielded slightly better results compared to Mutual Information.

---

## ✅ Conclusion

Despite Random Forest’s reputation for robustness, **Naive Bayes** proved superior in this specific task due to its speed and comparable accuracy. Future work should explore model generalization on real-world data and try advanced NLP techniques like contextual embeddings.

---

## 📌 Authors

Group 5 — Text Mining Final Project  
(Spring Semester, [University/Department Placeholder])

