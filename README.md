# 🎵 Song Popularity Prediction

This project analyzes the factors that influence a song’s popularity using clustering (K-Means) and predictive modeling (Linear Regression), developed as part of a group assignment for the **Machine Learning I** course.

> 🚀 The goal: Help producers and artists better understand what musical attributes drive success and use that insight to forecast whether a song will perform well.

---

## 🧠 Project Objectives

- Identify key characteristics that define different types of songs
- Group songs based on their acoustic, instrumental, and rhythmic features using **unsupervised learning**
- Predict track popularity using **linear regression**, measuring the influence of genre, artist popularity, and other musical properties
- Deliver strategic recommendations for music production and marketing

---

## 📁 Project Structure

- Assignment 1_Popularity Prediction_Notebook.ipynb >>> Full code: EDA, Clustering (K-Means), Regression models
- README.md >>> Project summary and documentation

---

## 🔍 Dataset

The dataset, `Songs_2025.xlsx`, includes **2,300 songs** with 19 features, such as:
- Musical properties: `danceability`, `energy`, `acousticness`, `tempo`, etc.
- Metadata: `artist popularity`, `release year`, `genre`, etc.

---

## 📊 Methodology

### 1. **Exploratory Data Analysis**
- Cleaned outliers (279 rows)
- Consolidated multiple genres into a new `"super-genre"` feature
- One-hot encoded genre labels for modeling

### 2. **Segmentation (K-Means Clustering)**
- Used 4 features: `speechiness`, `acousticness`, `instrumentalness`, and `liveness`
- Applied the **Elbow Method** → Optimal `k = 5`
- Silhouette Score = **0.446**, Inertia = **2314.23**
- Cluster profiling yielded insights into listener segments

### 3. **Linear Regression**
- Used OLS with stepwise selection
- Top features: `artist popularity`, `energy`, `reggae`, `rock`, `rnb_soul`, etc.
- Achieved **R² = 0.34**, with MAE, RMSE, and MAPE indicating good model reliability

---

## 💡 Key Insights

- 🔋 **Energy** has a strong *negative* impact on popularity → calmer songs are more successful
- 🎤 **Reggae** songs tend to perform well
- 🌟 **Artist popularity** significantly boosts track success
- 🎸 Genres like **rock** and **acoustic** show moderate positive influence

---

## 📈 Model Performance

| Metric        | Value (Test Set) |
|---------------|------------------|
| R² Score      | 0.34             |
| MAPE          | < 10%            |
| MAE / RMSE    | Low              |

> 📌 These results suggest a practical tool for producers and marketers to forecast a song's potential.

---

## 🛠 Tools Used

- Python
- Pandas, NumPy, Matplotlib, Seaborn
- Scikit-learn (KMeans)
- Statsmodels (OLS regression)

---

## 🙋‍♀️ Authors

Ana Cortés Barquier, Tomás Valbuena Sierra, Tomás Luz, Robert Koegel, Hiromitsu Fujiyama

---

## 📌 Future Improvements

- Incorporate **social media engagement** and **listener demographics**
- Explore **non-linear models** like Random Forests or Gradient Boosting
- Build a **classification model** to predict “hit or not” based on threshold

---

## 📄 License

This project is for academic and educational purposes only.