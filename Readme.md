# 🚖 Uber Trip Analysis (Machine Learning Project)

![Python](https://img.shields.io/badge/Python-3.12-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-orange)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Data%20Visualization-blueviolet)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Visualization-lightblue)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-yellow)

![Project](https://img.shields.io/badge/Data%20Analysis-Project-success)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Random%20Forest-brightgreen)
![Domain](https://img.shields.io/badge/Domain-Transportation-blue)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

# 📌 Project Overview

This project analyzes **Uber trip data** to discover patterns in ride demand and build a **machine learning model to predict trip counts**.

Using historical Uber trip data, the analysis identifies:

* Peak ride hours
* Busiest days of the week
* Demand patterns over time
* Predictive insights using machine learning

The project demonstrates **data preprocessing, exploratory data analysis (EDA), feature engineering, and predictive modeling**.

---

# 🎯 Project Objectives

* Analyze Uber trip demand patterns
* Identify peak hours and busy days
* Engineer useful time-based features
* Train a **Random Forest Machine Learning model**
* Predict the number of Uber trips
* Visualize actual vs predicted demand

---

# 📊 Dataset Information

The dataset contains Uber trip statistics collected from the **NYC Taxi & Limousine Commission (TLC)**. 

### Dataset Features

| Column                  | Description                    |
| ----------------------- | ------------------------------ |
| date                    | Date of the trip               |
| trips                   | Number of Uber trips           |
| active_vehicles         | Number of active Uber vehicles |
| dispatching_base_number | Uber base company code         |

Additional features were created from the **date column**.

---

# 🛠 Tools & Technologies

| Category         | Tools                      |
| ---------------- | -------------------------- |
| Programming      | Python                     |
| Data Analysis    | Pandas, NumPy              |
| Visualization    | Matplotlib, Seaborn        |
| Machine Learning | Scikit-Learn               |
| Development      | Jupyter Notebook / VS Code |

---

# ⚙️ Project Workflow

## 1️⃣ Data Loading

The dataset is loaded from Excel and converted to CSV format for easier processing.

```python
data = pd.read_excel("Uber-Jan-Feb-FOIL.xlsx")
```

---

# 🧹 Data Preprocessing

Steps performed:

* Convert date column to datetime format
* Inspect dataset structure
* Prepare dataset for analysis

```python
data['date'] = pd.to_datetime(data['date'])
```

---

# 🔧 Feature Engineering

New time-based features were created:

| Feature   | Description       |
| --------- | ----------------- |
| Hour      | Hour of the trip  |
| Day       | Day of the month  |
| DayOfWeek | Day of the week   |
| Month     | Month of the trip |

```python
data['Hour'] = data['date'].dt.hour
data['Day'] = data['date'].dt.day
data['DayOfWeek'] = data['date'].dt.dayofweek
data['Month'] = data['date'].dt.month
```

Dummy variables were also created for categorical features.

---

# 📊 Exploratory Data Analysis (EDA)

### Trips Per Hour

Shows the distribution of Uber rides throughout the day.

```python
sns.countplot(data['Hour'])
```

---

### Trips Per Day of the Week

Identifies the busiest days for Uber rides.

```python
sns.countplot(data['DayOfWeek'])
```

---

# 🤖 Machine Learning Model

A **Random Forest Classifier** was used to predict trip demand.

### Features Used

* Hour
* Day
* DayOfWeek
* Month
* Active Vehicles

### Target Variable

```
trips
```

---

# 🔍 Model Training

The dataset was split into **training and testing sets**.

```python
train_test_split(X, y, test_size=0.3, random_state=42)
```

Random Forest model was trained on the dataset.

```python
RandomForestClassifier()
```

---

# 📈 Model Evaluation

Performance was evaluated using:

* **Mean Squared Error (MSE)**
* **R² Score**

```python
Mean Squared Error
R² Score
```

These metrics help evaluate the prediction accuracy of the model.

---

# 📉 Visualization of Predictions

The relationship between **actual trips and predicted trips** was visualized.

```python
plt.scatter(y_test, y_pred)
```

This visualization helps assess the model’s predictive performance.

---

# 📁 Project Structure

```
uber_trip_analysis
│
├── csv_files
│   └── Uber-Jan-Feb-FOIL.csv
│
├── outputs
│   ├── number_of_trips-per-hour.png
│   ├── number_of_trips_per_day.png
│   └── trips_predictions.png
│
├── notebooks
│   └── uber_trip_analysis.ipynb
│
└── README.md
```

---

# 🚀 How to Run the Project

### 1️⃣ Clone the Repository

```
git clone https://github.com/Jiji-1905/uber-trip-analysis.git
```

---

### 2️⃣ Install Required Libraries

```
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

### 3️⃣ Run the Notebook

(https://colab.research.google.com/drive/1x0Jo6GWiG_bI7_WJtZdoufYfDS9HkE5B?usp=sharing)

---

# 📊 Key Insights

Important findings from the analysis:

✔ Uber demand varies significantly across **different hours of the day**

✔ Certain **days of the week have higher ride demand**

✔ Machine learning models can successfully **predict trip demand patterns**

✔ Time-based features such as **Hour and DayOfWeek are strong predictors**

---

# 🔮 Future Improvements

Possible improvements include:

* Using **XGBoost or Gradient Boosting models**
* Incorporating **location-based features**
* Building a **real-time Uber demand dashboard**
* Implementing **time-series forecasting models**

---

# 👨‍💻 Author

**Jiji Babu**
**Data Analyst**

Skills:

* Data Analysis
* Python
* Machine Learning
* SQL
* Data Visualization

---


