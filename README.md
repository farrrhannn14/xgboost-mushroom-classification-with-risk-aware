# 🍄 Mushroom Toxicity Classification using XGBoost

## 📌 Project Overview
This project focuses on developing a binary classification model to predict whether mushrooms are **poisonous or edible** based on their physical and environmental characteristics. The model was developed using **XGBoost** with an emphasis not only on predictive performance, but also on **reliability of decision-making and risk-aware evaluation**. Instead of relying on default settings and aggregate metrics, this project explores how **feature importance analysis** and **threshold adjustment** can significantly affect model prediction results in classifications that are critical to safety.

---

## 🎯 Objectives
- Build a binary classifier for mushroom toxicity detection  
- Analyze the most influential features driving model predictions  
- Evaluate model performance beyond accuracy-based metrics  
- Adjust the decision threshold to reflect real-world risk considerations

---

## 📊 Dataset Description
The dataset contains categorical and numerical features describing mushroom characteristics, such as:
- Cap shape, surface, and color  
- Gill attachment and gill color  
- Ring type  
- Habitat and season  
- Stem dimensions  

The target variable indicates whether a mushroom is **poisonous (1)** or **edible (0)**.

## 📎 Data Source

The dataset used in this project was obtained from Kaggle:

**Mushroom Classification: Edible or Poisonous?**  
Source: Kaggle  
Link: [Dataset](https://www.kaggle.com/datasets/vishalpnaik/mushroom-classification-edible-or-poisonous)

---

## 🧠 Modeling Approach
- **Language**: `Python`
- **Algorithm**: `XGBoost Classifier`  
- **Preprocessing**:
  - One-hot encoding for categorical features  
  - Handling missing values  
  - Train–test split for evaluation  
- **Evaluation Metrics**:
  - Accuracy  
  - Precision, Recall, F1-score  
  - Confusion Matrix  
  - ROC-AUC  

The model demonstrates strong baseline performance before any threshold adjustment.

---

## 🔍 Feature Importance Analysis
To understand which features contribute most to the model’s predictions, feature importance scores from XGBoost were analyzed.

Key observations:
- Environmental and structural features such as **habitat**, **cap color**, **ring type**, and **gill attachment** play a significant role in determining toxicity.  
- Certain cap shapes and surface characteristics consistently appear among the top predictive features.  

Key Visualization:
<img width="1001" height="573" alt="image" src="https://github.com/user-attachments/assets/0f734e0e-d03d-4e4e-82a3-c203b6711941" />

---

## ⚖️ Threshold Tuning and Risk Considerations
In real-world mushroom classification, the cost of misclassification is **asymmetric**.  
A **false negative**—classifying a poisonous mushroom as edible—poses a far greater risk than a false positive.

For this reason, threshold tuning was performed to:
- Move beyond the default probability threshold of 0.5  
- Explicitly control the trade-off between **precision and recall**  
- Align model decisions with **safety-oriented objectives**  

Confusion Matrix after Threshold Tuning:
<img width="754" height="642" alt="image" src="https://github.com/user-attachments/assets/05325154-d096-47db-9584-a906c60c7770" />

The results show that adjusting the threshold significantly impacts recall and error distribution, making the model more suitable for risk-sensitive deployment scenarios.

---

## ✅ Key Takeaways
- High overall accuracy does not guarantee safe decision-making  
- Feature importance analysis helps validate model reasoning  
- Threshold tuning is a crucial step in safety-critical classification tasks  
- Model evaluation should be aligned with **real-world consequences**

---
