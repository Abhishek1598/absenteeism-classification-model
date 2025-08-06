
## ✅ Final Summary

In this project, we analyzed employee absenteeism data to uncover patterns and build a model to predict excessive absenteeism. Here’s a wrap-up of the work done:

### 📊 Data Preprocessing
- Checked for nulls, handled date-time conversions, and created additional time-based features such as **day of the week** and **month of absence**.
- Encoded **Reason for Absence** into 4 categorical dummy variables for interpretability and modeling.
- Cleaned and renamed columns for clarity and usability.

### 📈 Exploratory Data Analysis (EDA)
- Visualized absenteeism distribution using **boxplots** and **histograms**.
- Explored how absenteeism varies by:
  - Reason for absence (most common: medical consultation/checkups)
  - Day of the week (peak: Monday & Friday)
  - Month (higher in winter months)
  - Demographics such as education level, number of children, and pets.
- Built a **correlation matrix** which showed weak correlation with absenteeism, but strong internal correlation among transport, distance, BMI, etc.

### 🧠 Logistic Regression Modeling
- Created a binary target (`Excessive Absenteeism`) using the **median** of absenteeism hours.
- Checked class balance (~50/50 split).
- Standardized only numerical features (excluding already dummy-encoded variables like `Reason_1`–`Reason_4`).
- Split the dataset into training and test sets (80/20) and trained a **Logistic Regression** model.
- Achieved solid accuracy on both training and test data.
- Interpreted model coefficients and calculated odds ratios.

### 🗂️ Deployment Preparation
- Extracted model intercept and coefficients.
- Generated **predicted probabilities** for the test set.
- Finalized the model and prepared it for deployment using serialization (`pickle`).

---

## 💡 Key Insights

- No strong predictor of absenteeism time in hours was identified — absenteeism seems multifactorial and noisy.
- Logistic regression is a reasonable baseline due to its simplicity and interpretability.
- Absenteeism patterns show behavioral trends (e.g., weekend spillovers, checkups on Mondays/Fridays) rather than purely health-related causes.
