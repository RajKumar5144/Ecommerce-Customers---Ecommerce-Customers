# 🛍️ Ecommerce Customer Spending Prediction

## 📘 Project Overview
This project explores customer behavior for an **Ecommerce company based in New York City**.  
The company sells clothing online and also offers **in-store personal styling sessions**.  

The goal is to determine whether the company should **focus on improving the Mobile App or the Website experience** to increase customer spending.  
Using **Linear Regression**, we analyze how different factors such as time spent on the website, time spent on the app, and length of membership influence the **Yearly Amount Spent**.

---

## 📂 Dataset Description
The dataset contains customer-level information, including demographics and activity details.

| Feature | Description |
|----------|-------------|
| `Email` | Customer email ID |
| `Address` | Customer address |
| `Avatar` | Customer avatar color |
| `Avg. Session Length` | Average length of in-store style advice sessions |
| `Time on App` | Average time spent on the app (in minutes) |
| `Time on Website` | Average time spent on the website (in minutes) |
| `Length of Membership` | Number of years the customer has been a member |
| `Yearly Amount Spent` | Total yearly expenditure by the customer (Target variable) |

---

## 🎯 Objective
To **build a Linear Regression model** that predicts a customer’s **Yearly Amount Spent** based on their usage patterns and membership history.  
Additionally, to derive insights about whether the company should prioritize **mobile app** or **website** development.

---

## 🧩 Approach

### 1. **Data Exploration (EDA)**
- Visualized relationships between variables using **Seaborn** (`pairplot`, `jointplot`, `heatmap`).
- Checked correlations between features and target variable.
- Found that **Length of Membership** had the highest correlation with **Yearly Amount Spent**.

### 2. **Feature Selection**
- Selected relevant numerical features:



### 3. **Model Building**
- Split data into **train (70%)** and **test (30%)** using `train_test_split`.
- Trained a **Linear Regression** model using `sklearn.linear_model.LinearRegression`.

### 4. **Model Evaluation**
- Predicted customer spending on the test dataset.
- Evaluated using:
- **MAE (Mean Absolute Error)**
- **MSE (Mean Squared Error)**
- **RMSE (Root Mean Squared Error)**
- **R² Score (Goodness of fit)**
- Visualized actual vs predicted values using scatterplots.

### 5. **Interpretation**
- The model performed well, with low error metrics and normally distributed residuals.
- Coefficients were analyzed to interpret variable importance.

---

## 📊 Results & Insights
| Feature | Coefficient | Insight |
|----------|-------------|----------|
| Avg. Session Length | + | Small positive impact |
| Time on App | + | Strong positive impact |
| Time on Website | + | Weak positive impact |
| Length of Membership | + | Strongest predictor |

✅ **Conclusion:** The analysis shows that **Time on App** and **Length of Membership** have the most influence on customer spending.  
Hence, the company should **focus more on improving the Mobile App experience** and **retain long-term members**.

---

## 🧰 Tools & Libraries Used
- **Python** 🐍  
- **Pandas**, **NumPy** – Data handling  
- **Matplotlib**, **Seaborn** – Visualization  
- **Scikit-learn** – Linear Regression model & evaluation  
- **Google Colab / Jupyter Notebook** – Environment  

---

## 📅 Future Improvements
- Use advanced models like **Polynomial Regression**, **Ridge/Lasso Regression**, or **Random Forest** for comparison.  
- Include more customer behavior variables (e.g., product type, order frequency).  
- Deploy the model as a simple dashboard or Flask app for real-time predictions.  

---

## 👨‍💻 Author
**Raj Kumar**  
NIT Warangal | Data Science & Machine Learning Enthusiast  

---

## 🧾 Acknowledgment
This project is inspired by a classic **Linear Regression exercise** commonly used in data science learning paths (originally from a Udemy course dataset).
