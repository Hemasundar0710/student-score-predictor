# Student Score Predictor — Linear Regression

A machine learning project that predicts a student's exam score based on the number of hours studied, built using Python and Scikit-learn.

> **Internship Project** | YBI Foundation | May–Jun 2024

---

## Project Overview

Predicting academic performance is a classic regression problem. This project builds a supervised ML pipeline — from raw data to a trained model — that estimates a student's score given their study hours.

The model achieves an **R² score of 0.93**, meaning it explains ~93% of the variance in student scores from study hours alone.

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.x | Core language |
| Pandas | Data loading and manipulation |
| Matplotlib / Seaborn | Data visualization |
| Scikit-learn | Model building and evaluation |
| Google Colab | Development environment |

---

## Project Structure

```
student-score-predictor/
│
├── dataset.csv              # Study hours vs scores dataset
├── student_score_predictor.ipynb  # Main Jupyter notebook
└── README.md
```

---

## ML Pipeline

```
Load Data → Visualize → Preprocess → Train/Test Split → Train Model → Evaluate → Predict
```

**Steps in detail:**

1. **Data Loading** — Read CSV with Pandas; inspect structure and sample rows
2. **Exploratory Visualization** — Scatter plot to confirm linear relationship between hours and scores
3. **Data Preprocessing** — Separate features (`Hours`) from target (`Scores`)
4. **Train/Test Split** — 80% training, 20% testing (`random_state=42`)
5. **Model Training** — Fit `LinearRegression` from Scikit-learn on training data
6. **Prediction & Visualization** — Plot regression line against actual test points
7. **Evaluation** — Measure performance with MSE and R² Score
8. **Custom Prediction** — Predict score for any input study hours

---

##  Results

| Metric | Value |
|--------|-------|
| Mean Squared Error (MSE) | 22.66 |
| R² Score | 0.9335 |

**Sample Prediction:**
```
Input  → 6.5 study hours
Output → Predicted score: 63.73
```

---

##  Visualizations

The notebook includes:
- Scatter plot of `Hours vs Scores` (raw data)
- Regression line plotted over test data points

---

##  How to Run

**Option 1 — Google Colab (recommended)**

Click the badge at the top or open the `.ipynb` file directly in Colab.

**Option 2 — Local setup**

```bash
git clone https://github.com/your-username/student-score-predictor
cd student-score-predictor
pip install pandas matplotlib seaborn scikit-learn
jupyter notebook student_score_predictor.ipynb
```

---

## Key Learnings

- Building an end-to-end supervised ML pipeline from scratch
- Evaluating regression models using MSE and R² metrics
- Visualizing model performance with Matplotlib
- Understanding train/test split to prevent overfitting

---

## Possible Improvements

- Use a larger, real-world dataset with multiple features (sleep hours, attendance, etc.)
- Compare with other regression models (Ridge, Polynomial Regression)
- Deploy as a simple web app using Streamlit or Flask

---

## License

This project is open source under the [MIT License](LICENSE).

---

*Built with ❤️ during internship at [YBI Foundation](https://ybifoundation.org)*
