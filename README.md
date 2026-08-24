# E-Commerce Data Analysis & EDA

## 📌 Assignment Information

**Organization:** Calibo
**Assignment Date:** 22 August 2026
**Assignment Type:** Exploratory Data Analysis (EDA)
**Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook

---

## 📊 Project Overview

This project was completed as part of an **E-Commerce Data Analysis assignment provided by Calibo on 22 August 2026**.

The objective of this assignment is to perform a complete **Exploratory Data Analysis (EDA)** on a messy e-commerce dataset, identify and handle data-quality issues, analyze customer and transaction patterns, visualize relationships between variables, and derive meaningful business insights.

The analysis is performed using Python and popular data-analysis and visualization libraries.

---

## 📁 Dataset

The notebook uses the following dataset:

```text
messy_ecommerce_15000_student_practice.csv
```

The original dataset is loaded only for analysis and is **not overwritten**.

The cleaned dataset is saved as:

```text
cleaned_ecommerce_dataset.csv
```

---

## 🛠️ Technologies Used

* **Python 3**
* **Jupyter Notebook**
* **Pandas** — data manipulation and analysis
* **NumPy** — numerical operations
* **Matplotlib** — data visualization
* **Seaborn** — statistical visualization

---

## 🔍 Analysis Performed

### 1. Numerical Data Analysis

The numerical columns were analyzed using:

* Mean
* Median
* Standard deviation
* Minimum
* Maximum
* 25th percentile
* 50th percentile
* 75th percentile
* Range

The analysis identified strong right-skewness in variables such as `Total_Amount` and unusually large ranges in `Unit_Price` and `Total_Amount`.

---

### 2. Categorical Data Analysis

Categorical variables were analyzed to identify:

* Number of unique values
* Most frequent categories
* Category frequencies
* Missing categorical values

Important categorical columns include:

* `Gender`
* `City`
* `Product_Category`
* `Payment_Method`
* `Returned`

---

### 3. Data Cleaning

Several data-quality issues were identified and addressed.

#### Categorical Standardization

Inconsistent representations such as:

```text
Male / male
Female / female
UPI / upi
Credit Card / credit card
Yes / yes
```

were standardized using string cleaning and title casing.

#### Missing Values

Missing values were handled using:

| Data Type   | Method |
| ----------- | ------ |
| Numeric     | Median |
| Categorical | Mode   |

Columns such as `Age`, `Discount`, `Rating`, and `Delivery_Days` use median imputation, while categorical columns use their most frequent valid category.

#### Duplicate Records

Exact duplicate records were detected and removed after verification.

The notebook also checks for duplicate `Order_ID` values.

---

## 📈 Outlier Detection

Outliers were investigated using two approaches:

### Seaborn Boxplots

Boxplots were created for:

* Age
* Unit Price
* Quantity
* Discount
* Rating
* Delivery Days
* Total Amount

### IQR Method

The Interquartile Range method was used to calculate:

* Q1
* Q3
* IQR
* Lower Bound
* Upper Bound
* Outlier Count

Importantly, statistical outliers were **not automatically deleted**. Legitimate high-value transactions can naturally appear as outliers in an e-commerce dataset.

---

## 🧮 Data Consistency Validation

The notebook calculates an expected order amount using:

```text
Unit Price × Quantity × (100 − Discount) / 100
```

This calculated value is compared against the recorded `Total_Amount`.

Records with differences greater than ₹1 are flagged for further investigation.

---

## 📊 Exploratory Data Visualization

### Univariate Analysis

The notebook includes:

* Age distribution
* Total amount distribution
* Unit price KDE distribution
* Total amount boxplot
* Orders by product category
* Orders by payment method
* Orders by gender

### Bivariate Analysis

Relationships investigated include:

* Age vs Total Amount
* Unit Price vs Total Amount
* Discount vs Total Amount
* Product Category vs Total Amount
* Gender vs Total Amount
* Payment Method vs Total Amount

### Multivariate Analysis

The notebook also includes:

* Pairplot of numerical variables
* Correlation heatmap
* Product Category vs Gender
* Product Category vs Return Status
* Payment Method vs Return Status

---

## 📌 Key Business Insights

The analysis produced several important findings:

1. **Electronics** receives the highest number of orders.
2. **Electronics** also has the highest average order value.
3. **Credit Card** is the most popular payment method.
4. **Kolkata** has the highest total sales in the cleaned dataset.
5. The `Other` gender group has the highest average spending, although it contains significantly fewer orders.
6. `Discount` has only a weak negative relationship with `Total_Amount`.
7. **Hair Dryer** has the highest average product rating.
8. Approximately **12% of orders are returned**.
9. Delivery time has almost no linear relationship with customer rating.
10. **Unit_Price** is the strongest numerical feature associated with `Total_Amount`.

---

## 📂 Project Structure

```text
E-Commerce-EDA/
│
├── Ecommerce_EDA_Student_Colorful.ipynb
├── messy_ecommerce_15000_student_practice.csv
├── cleaned_ecommerce_dataset.csv
└── README.md
```

> The `Ecommerce_EDA_Student_Colorful.ipynb` version contains enhanced visualization styling with more colorful and visually attractive graphs.

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd E-Commerce-EDA
```

### 2. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 3. Start Jupyter Notebook

```bash
jupyter notebook
```

### 4. Open the notebook

Open:

```text
Ecommerce_EDA_Student_Colorful.ipynb
```

Make sure the dataset is located in the same directory:

```text
messy_ecommerce_15000_student_practice.csv
```

Then run the notebook cells sequentially.

---

## 🎨 Visualization Enhancement

The submitted colorful version improves the visual presentation of the EDA by using more vibrant chart colors and enhanced Seaborn styling while retaining the original analytical workflow.

The goal is to make the graphs easier to interpret and more attractive for presentation and submission.

---

## ✅ Final Outcome

After completing the analysis, the dataset has been processed for:

* Missing values
* Duplicate records
* Categorical inconsistencies
* Date validation
* Outlier investigation
* Transaction amount consistency
* Numerical analysis
* Categorical analysis
* Correlation analysis
* Business insight generation

The final cleaned dataset is exported separately, while the original dataset remains unchanged.

---

## 👨‍💻 Author

**Bhavyesh Bhavye**

**Assignment:** E-Commerce Exploratory Data Analysis
**Assigned By:** Calibo
**Assignment Date:** 22 August 2026

---

## 📜 Note

This repository contains work completed for an academic/assessment assignment. The analysis focuses on demonstrating practical skills in **data cleaning, exploratory data analysis, statistical analysis, visualization, and business interpretation using Python**.
