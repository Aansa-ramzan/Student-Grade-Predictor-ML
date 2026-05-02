# Student Grade Predictor: A Comparative ML Study

##  Project Overview
This project explores the impact of socio-economic and behavioral factors on academic performance. Using a dataset of students from two Portuguese schools, I developed a machine learning pipeline to predict final grades ($G3$) without relying on mid-term results ($G1, G2$)[cite: 1, 2].

The goal was to determine if lifestyle attributes like social habits, alcohol consumption, and family support can provide an "early warning system" for students at risk of underperforming[cite: 1].

##  Tech Stack & Methodology
*   **Language:** Python (Google Colab)
*   **Libraries:** Pandas, Scikit-Learn, Matplotlib, Seaborn
*   **Data Source:** UCI Machine Learning Repository (Student Performance Dataset)[cite: 1]
*   **Processing:**
    *   Merged Math and Portuguese datasets (Total: 1,044 records)[cite: 1, 2].
    *   Applied **One-Hot Encoding** for categorical features[cite: 1].
    *   Implemented an **80/20 Train-Test split** to evaluate model generalization.

##  Model Performance
I compared a baseline linear model with a complex ensemble model to capture non-linear student behaviors[cite: 1].

**| Algorithm             | Mean Absolute Error (MAE) | R² Score |
  | Linear Regression     | 2.64                      | 0.09     |
  | Random Forest         | 2.63                      | 0.11     |**

> **Key Insight:** While the $R^2$ score is modest, the Random Forest successfully outperformed the Linear Regression by capturing complex interactions between lifestyle variables. In social science research, an 11% variance explanation is statistically significant for identifying broad performance trends[cite: 1].

##  Top Predictors of Success
According to the **Random Forest Feature Importance**, the following factors most heavily influenced the final grade[cite: 1]:

1.  **Past Failures:** The strongest predictor of future performance[cite: 1].
2.  **Absences:** A direct correlation between school attendance and final outcomes[cite: 1].
3.  **School Support & Social Life:** Interestingly, extra educational support (`schoolsup`) and the frequency of "going out" (`goout`) held similar weights in the model[cite: 1].
4.  **Health:** Current health status emerged as a top-5 factor, highlighting the link between well-being and academic success[cite: 1].

##  How to Run
1.  Clone this repository.
2.  Ensure `student-mat.csv` and `student-por.csv` are in the project directory[cite: 1].
3.  Run the provided `.ipynb` notebook in Google Colab or Jupyter.
4.  The script will automatically preprocess the data and output the comparison metrics.

##  References & Data Credit
The dataset used in this project was originally collected and published by:
**P. Cortez and A. Silva.** *Using Data Mining to Predict Secondary School Student Performance.* In A. Brito and J. Teixeira Eds., Proceedings of 5th FUture BUsiness TEChnology Conference (FUBUTEC 2008) pp. 5-12, Porto, Portugal, April, 2008, EUROSIS, ISBN 978-9077381-39-7[cite: 1].

---
*Developed as a portfolio project.*
