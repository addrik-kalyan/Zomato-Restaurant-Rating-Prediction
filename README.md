# 🍔 Zomato Delivery Data Analysis

A data analysis project that explores delivery performance using the Zomato dataset. This notebook analyzes delivery times, traffic conditions, weather impact, and vehicle usage patterns to uncover operational insights.

Think of it as a control room for food logistics where every order leaves a breadcrumb trail of data. 📦⚡

---

# 📌 Project Overview

The notebook performs several analytical tasks on the Zomato delivery dataset:

* Loads delivery data using Pandas
* Calculates average delivery times
* Identifies cities with the highest number of orders
* Analyzes traffic density impact on delivery time
* Examines weather effects on deliveries
* Finds the most commonly used delivery vehicle types

---

# 📊 Analysis Performed

## 1. Average Delivery Time

Calculates the overall average time taken for food deliveries.

```python
average_time_taken = df["Time_taken (min)"].mean()
```

---

## 2. City With Highest Orders

Finds which city generated the highest number of orders.

```python
city_with_most_orders = df["City"].value_counts().idxmax()
```

---

## 3. Traffic Density vs Delivery Time

Analyzes how traffic conditions affect delivery performance.

```python
traffic_density_avg_time = df.groupby(
    "Road_traffic_density"
)["Time_taken (min)"].mean()
```

---

## 4. Weather Conditions Impact

Measures delivery times under different weather conditions.

```python
weather_avg_time = df.groupby(
    "Weather_conditions"
)["Time_taken (min)"].mean()
```

---

## 5. Top Delivery Vehicle Types

Identifies the most frequently used delivery vehicles.

```python
top_vehicles = df["Type_of_vehicle"].value_counts().head(3)
```

---

# 🛠️ Technologies Used

* Python
* Pandas
* Google Colab
* Jupyter Notebook

---

# 📂 Project Structure

```bash
Zomato-Delivery-Analysis/
│
├── zomato.ipynb
├── Zomato Dataset.csv
└── README.md
```

---

# ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/your-username/Zomato-Delivery-Analysis.git
cd Zomato-Delivery-Analysis
```

Install required libraries:

```bash
pip install pandas
```

---

# ▶️ Running the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open the notebook:

```bash
zomato.ipynb
```

Run all cells to generate the analysis results.

---

# 📈 Sample Insights

The project helps answer questions such as:

* Which city receives the most food orders?
* How much does traffic affect delivery time?
* Do weather conditions slow down deliveries?
* Which delivery vehicles are most commonly used?

---

# 🚀 Future Improvements

Possible upgrades for the project:

* Add data visualizations using Matplotlib or Plotly
* Create interactive dashboards
* Predict delivery time using machine learning
* Analyze customer ratings and satisfaction
* Build a real-time delivery monitoring system

---

# 📊 Dataset Information

The dataset contains delivery-related information such as:

| Column                 | Description               |
| ---------------------- | ------------------------- |
| `City`                 | Delivery city             |
| `Time_taken (min)`     | Delivery duration         |
| `Road_traffic_density` | Traffic conditions        |
| `Weather_conditions`   | Weather during delivery   |
| `Type_of_vehicle`      | Vehicle used for delivery |

---
