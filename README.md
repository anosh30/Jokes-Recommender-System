# 😂 Jokes Recommender System using User-User Collaborative Filtering

## 🎯 Objective

The objective of this project is to design and implement a **User-User Collaborative Filtering Recommender System** using the **Jester Dataset**. The system predicts a user's joke ratings based on ratings from the most similar users, using only the concepts studied during the course.

---

## 📁 Dataset Description

### 🔗 Dataset Link:
[Jester Dataset - Kaggle](https://www.kaggle.com/code/lusfernandotorres/text-summarization-with-large-language-models/input)

### 📦 Selected Version:
**Dataset 3** — Contains **2.3 million ratings** from users on various jokes.

### 📄 File Structure:
- Each row corresponds to a **user**
- Columns contain **ratings for jokes**
- Missing ratings are represented with **NaN** or **0**

### 🎯 Dataset Purpose:
To build a recommendation engine that can:
- Predict missing joke ratings for a user
- Recommend jokes based on similar users' preferences
- Evaluate accuracy using **MAE (Mean Absolute Error)**

---

## 🧠 Methodology

### ✅ Task Overview:
1. **Preprocess** the data (handle missing values, normalize ratings)
2. **Compute similarity** between users (e.g., Cosine similarity)
3. Predict joke ratings using the **K most similar users**
4. Compare the performance with a **Random K-user Recommender**
5. Evaluate both using **Mean Absolute Error (MAE)**

---

## 🏗️ Architecture Diagram

> Included in the PDF submission:
- Data Preprocessing Pipeline
- Similarity Calculation Block
- KNN-Based Prediction Module
- Evaluation Metrics Layer

---

## ⚙️ Implementation Details

### 🔍 Similarity Measures:
- Cosine Similarity
- Pearson Correlation (optional)

### 📊 Data Split:
- **80% Train**
- **20% Test**

### 🔎 Techniques for User Selection:
- Filtered top **2,000 most active users**
- Alternatively, tested **PCA-based dimensionality reduction**

### 🧪 Evaluation Metric:
- **MAE (Mean Absolute Error)** between actual and predicted ratings

### 🧪 Baseline Model:
- Randomly selects **K users**
- Predicts ratings based on their average ratings

---

## 🔢 Hyperparameters

| Parameter | Value / Description                      |
|-----------|-------------------------------------------|
| `K`       | Optimal number of neighbors (tuned)      |
| `Similarity` | Cosine Similarity (default)           |
| `Max Users` | 2000 (top-rated users)                  |
| `Batch Size` | Adjusted for performance (optional)    |

---

## 📊 Performance Evaluation

| Recommender Type | MAE (Lower is Better) |
|------------------|-----------------------|
| **Random K-Users**   | 2.14                  |
| **User-User CF**     | 1.08 (with K=10)      |

---

## 📎 Outputs Required (in Notebook)

- ✅ **Top 2K Users** with their similarity measures
- ✅ **Test Instances** showing original vs predicted ratings
- ✅ MAE comparisons between **baseline** and **CF model**

---

## 📁 Submission Requirements

- ✔️ **Jupyter Notebook (.ipynb)**: Complete implementation with results
- ✔️ **PDF Report**: Includes architecture diagram and result discussion

---

## 👨‍🏫 Evaluation Criteria

| Component                       | Weight |
|--------------------------------|--------|
| Task Completion (Team)         | 30%    |
| Individual Viva Performance    | 70%    |

> ⚠️ Students missing the viva session will receive **ZERO** marks.

---

## 💡 General Guidelines

- ❌ No cross-team collaboration is allowed
- 💬 Direct all clarifications to the course instructor early
- 🧠 Only course-taught concepts are allowed for implementation
- 🐍 Python is the mandatory implementation language

---

## 📬 Contact

For any questions or clarifications, please reach out to the course TA or instructor.

---

## 📜 License

This project is part of **CS-4063: Natural Language Processing (Spring 2025)**. Academic use only.

