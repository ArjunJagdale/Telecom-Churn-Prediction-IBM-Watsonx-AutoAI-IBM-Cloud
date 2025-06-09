# Telecom-Churn-Prediction-IBM-Watsonx-AutoAI-IBM-Cloud
Thanks for sharing the screenshots of your **Telecom Churn Prediction** project on **IBM Watsonx AutoAI**. Here's a breakdown of what you're seeing in each screenshot, along with the **steps you likely followed** (and may have forgotten) to reach this stage.

---
Link to project notebook-  https://eu-de.dataplatform.cloud.ibm.com/analytics/notebooks/v2/6b2a60b7-6179-49c7-8354-46e44d92c975/view?access_token=91c1102349858837f6dbe0065857dcf651656dc376f1a2e5c1e8d5d46bee49ec&context=cpdaas

## ✅ **What the Screenshots Show**

### 🔹 Relationship Map + Progress Map

---

This is from the **"Experiment summary"** tab:

* **Center**: Dataset used – `telecom_churn.csv`.
* **Pipelines**: AutoAI has automatically generated **8 pipelines** combining algorithms and feature transformers.
* **Top Algorithms**: Snap Random Forest and XGBClassifier were used.
* **Feature Transformers**: These are preprocessing techniques (e.g., encoding, normalization).
* **Right Panel** – Progress map:
  AutoAI tested 8 combinations (pipelines) of models and transformations.
  ✅ **Experiment completed** in 17 minutes.

---

### 🔹 Pipeline Leaderboard

---

This shows the **leaderboard of generated pipelines**, ranked by **accuracy (optimized)**:

| Rank | Pipeline | Algorithm          | Accuracy | Enhancements     | Build Time |
| ---- | -------- | ------------------ | -------- | ---------------- | ---------- |
| 1    | P8       | Snap Random Forest | 0.800    | HPO-1, FE, HPO-2 | 04:05      |
| 2    | P7       | Snap Random Forest | 0.800    | HPO-1, FE        | 02:35      |
| 3    | P6       | Snap Random Forest | 0.800    | HPO-1            | 01:31      |
| 4    | P4       | XGBClassifier      | 0.800    | HPO-1, FE, HPO-2 | 09:07      |

* **HPO** = Hyperparameter Optimization
* **FE** = Feature Engineering
  ✅ Pipeline 8 is the best one selected by AutoAI.

---

### 🔹 Pipeline Comparison (Metric Chart)

---

Metrics shown (cross-validation scores) for all pipelines:

* **Accuracy**: \~0.800 for all top models.
* **Average Precision**, **Balanced Accuracy**, **Log Loss**, etc., show slight variation.
* Some metrics like **F1**, **Precision**, and **Recall** are not computed (values are zero/missing) — this may be due to configuration limits in AutoAI preview mode.

---

## 🔁 **AutoAI Setup**
---

### ✅ 1. **Create a Project**

* Go to **IBM Watsonx.ai Studio**
* Click **"New Project"** → Choose **AutoAI experiment**

---

### ✅ 2. **Upload Dataset**

* Upload the `telecom_churn.csv` file (visible in center of Relationship Map)
* Choose **`churn`** as the **prediction column** (target variable).

---

### ✅ 3. **Configure Experiment Settings**

* Selected prediction type: **Binary Classification** (churn or not)
* Chose to **optimize for accuracy** or let AutoAI decide
* (Optional) Adjusted runtime or resource settings

---

### ✅ 4. **Run AutoAI**

* AutoAI performed:

  * **Data preprocessing**
  * **Feature engineering**
  * **Algorithm selection**
  * **Pipeline generation**
  * **Hyperparameter tuning**
* Generated and compared **8 pipelines** (visible in the progress map)

---

### ✅ 5. **Pipeline Evaluation**

* Viewed the **pipeline leaderboard**
* Compared performance using metrics like accuracy, log loss, ROC AUC, etc.

---

### ✅ 6. **Model Selection**

* AutoAI **automatically chose the best pipeline** (Pipeline 8) based on accuracy
* You could click “Save Code” to generate a **notebook for deployment**

---

## ScreenShots:
![Screenshot 2025-06-09 223546](https://github.com/user-attachments/assets/e7b3c1d5-fad9-47e9-926c-60a05055d776)
![Screenshot 2025-06-09 223645](https://github.com/user-attachments/assets/7bdf5625-50f0-4e11-8199-e425bd3c7b89)
![Screenshot 2025-06-09 223620](https://github.com/user-attachments/assets/259d9f64-14d0-49b0-9ba0-21bf36b1cada)
![Screenshot 2025-06-10 003556](https://github.com/user-attachments/assets/f6023154-4f13-416a-91e8-734b0e3e2bb9)
