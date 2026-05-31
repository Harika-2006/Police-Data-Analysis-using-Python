# 🚔 Police Data Analysis using Python & Pandas

## 📌 Project Overview

This project focuses on analyzing police stop records using **Python** and **Pandas**. The dataset contains information about traffic stops, driver demographics, violations, searches conducted, and stop durations.

The objective is to perform data cleaning, data exploration, and answer business-related questions using Pandas operations such as filtering, grouping, mapping, aggregation, and descriptive statistics.

---

## 🛠️ Technologies Used

* Python
* Pandas
* Jupyter Notebook

---

## 📂 Dataset Information

The dataset contains information such as:

* Driver Gender
* Driver Age
* Violation Type
* Search Conducted
* Stop Duration
* Country Name
* Other traffic stop details

---

## 📊 Data Cleaning

### Remove Columns with Missing Values

Identified columns containing only missing values and removed them from the dataset.

```python
data.drop(columns='country_name', inplace=True)
```

---

## 🔍 Analysis Performed

### 1. Remove Columns that Contain Only Missing Values

* Checked null values in all columns.
* Removed unnecessary columns containing only missing values.

---

### 2. For Speeding Violations, Were Men or Women Stopped More Often?

Used filtering and value counts to determine which gender was stopped more frequently for speeding violations.

```python
data[data.violation == 'Speeding'].driver_gender.value_counts()
```

**Concepts Used:**

* Filtering
* Value Counts

---

### 3. Does Gender Affect Who Gets Searched During a Stop?

Analyzed the number of searches conducted based on driver gender.

```python
data.groupby('driver_gender').search_conducted.sum()
```

**Concepts Used:**

* GroupBy
* Aggregation

---

### 4. What is the Mean Stop Duration?

Converted categorical stop durations into numerical values using mapping and calculated the average stop duration.

```python
data['stop_duration'] = data['stop_duration'].map({
    '0-15 Min': 7.5,
    '16-30 Min': 24,
    '30+ Min': 45
})
```

```python
data['stop_duration'].mean()
```

**Concepts Used:**

* Mapping
* Data Type Conversion
* Mean Calculation

---

### 5. Compare Age Distribution for Each Violation

Compared driver age statistics across different violation categories.

```python
data.groupby('violation').driver_age.describe()
```

**Concepts Used:**

* GroupBy
* Describe
* Statistical Analysis

---

## 📈 Key Pandas Concepts Practiced

* Data Cleaning
* Handling Missing Values
* Filtering Data
* Value Counts
* GroupBy Operations
* Aggregation Functions
* Mapping Values
* Descriptive Statistics
* Data Exploration

---

## 🎯 Learning Outcomes

By completing this project, I gained hands-on experience in:

* Cleaning real-world datasets
* Performing exploratory data analysis (EDA)
* Answering business questions using data
* Applying Pandas functions efficiently
* Understanding data-driven decision making

---

## 🚀 How to Run

1. Clone the repository

```bash
git clone <repository-link>
```

2. Install required libraries

```bash
pip install pandas
```

3. Open the Jupyter Notebook

```bash
jupyter notebook
```

4. Run all cells in **Police data analysis.ipynb**

---

## 👩‍💻 Author

**Harika Posina**

Data Analytics | Python | SQL | Power BI | Excel

Learning through hands-on projects and real-world datasets.
