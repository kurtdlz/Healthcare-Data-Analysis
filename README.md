# Healthcare Patient Data Analysis

## 📌 Project Overview

This project performs an exploratory data analysis (EDA) of healthcare patient data to identify patterns in patient demographics, healthcare services, treatment costs, length of stay, recovery outcomes, and readmission risk.

The analysis uses Python to prepare, explore, visualize, and evaluate relationships within a dataset of **5,000 patient records**.

The goal is to demonstrate how healthcare data can be examined to uncover useful patterns and support data-driven interpretation of patient and operational metrics.

---

## 🎯 Objectives

* Understand the demographic and healthcare characteristics of the patients.
* Examine the distribution of healthcare-related numerical variables.
* Identify potential outliers in key numerical measures.
* Analyze patient distribution across regions, departments, treatments, and visit types.
* Examine relationships between treatment cost, length of stay, recovery score, and readmission risk.
* Compare treatment costs across departments.
* Compare average readmission risk across treatment types.
* Compare recovery scores between visit types.
* Examine average length of stay across age groups.

---

## 📊 Dataset

The dataset contains **5,000 patient records** and **11 variables**.

| Variable              | Description                        |
| --------------------- | ---------------------------------- |
| `patient_id`          | Unique identifier for each patient |
| `age_group`           | Patient age category               |
| `gender`              | Patient gender                     |
| `region`              | Patient region                     |
| `department`          | Healthcare department              |
| `treatment_type`      | Type of treatment received         |
| `visit_type`          | Type of patient visit              |
| `length_of_stay_days` | Length of hospital stay in days    |
| `treatment_cost`      | Cost associated with treatment     |
| `recovery_score`      | Patient recovery score             |
| `readmission_risk`    | Patient readmission risk           |

### Data Quality

The dataset was checked for:

* Missing values
* Duplicate records
* Data types
* Descriptive statistics
* Categorical distributions
* Numerical ranges
* Potential outliers

**Results:**

* Records: **5,000**
* Variables: **11**
* Missing values: **0**
* Duplicate records: **0**

---

## 🛠️ Tools & Technologies

* **Python**
* **Pandas** – data loading, cleaning, aggregation, and analysis
* **NumPy** – numerical computation
* **Matplotlib** – data visualization
* **Seaborn** – statistical visualization
* **SciPy** – statistical analysis
* **Dython** – mixed-variable association analysis
* **Jupyter Notebook / Google Colab**

---

## 🔎 Analysis Workflow

### 1. Data Preparation

The dataset was loaded using Pandas and examined through:

* Data type inspection
* Descriptive statistics
* Missing-value checks
* Duplicate checks
* Categorical value counts
* Percentage distributions
* Minimum and maximum value checks

No missing or duplicate records were identified in the dataset.

### 2. Exploratory Data Analysis

The analysis examined both categorical and numerical variables.

#### Categorical Analysis

Patient distributions were analyzed across:

* Age groups
* Gender
* Region
* Department
* Treatment type
* Visit type

The dataset contains:

* **31–45** as the largest age group
* A nearly balanced gender distribution
* Relatively balanced patient distribution across regions
* **Orthopedics** as the department with the highest number of records
* **Observation** as the most common treatment type
* **Routine visits** as the most common visit type

### 3. Numerical Analysis

The following numerical variables were analyzed:

* Length of stay
* Treatment cost
* Recovery score
* Readmission risk

The analysis used:

* Histograms
* Boxplots
* Descriptive statistics
* IQR-based outlier detection

### 4. Relationship Analysis

Scatter plots and correlation analysis were used to examine relationships between:

* Treatment cost ↔ Length of stay
* Recovery score ↔ Readmission risk
* Treatment cost ↔ Readmission risk
* Recovery score ↔ Treatment cost
* Readmission risk ↔ Length of stay

A numerical correlation matrix was also generated.

Categorical relationships were examined using **Cramér's V**, while mixed categorical/numerical associations were explored using Dython's association analysis.

---

## 📈 Key Findings

### Patient Distribution

The largest age group is **31–45**, with 1,716 patients.

The gender distribution is almost evenly split:

* Male: **2,508**
* Female: **2,492**

Routine visits account for **3,432 records (68.6%)**, while emergency visits account for **1,568 records (31.4%)**.

### Department Costs

**Orthopedics** recorded the highest total treatment cost at approximately **58.1M**, followed by:

1. Orthopedics — **58.1M**
2. Cardiology — **55.4M**
3. Pediatrics — **54.2M**
4. Neurology — **53.9M**
5. General Medicine — **53.0M**

This indicates that Orthopedics contributed the highest overall treatment expenditure within the dataset.

### Readmission Risk by Treatment

Average readmission risk was relatively similar across treatment types:

| Treatment Type | Average Readmission Risk |
| -------------- | -----------------------: |
| Observation    |                    0.283 |
| Therapy        |                    0.283 |
| Surgery        |                    0.280 |
| Medication     |                    0.279 |

The small differences suggest that treatment type alone does not show a substantial difference in average readmission risk within this dataset.

### Recovery Score by Visit Type

Average recovery scores were also very similar:

| Visit Type | Average Recovery Score |
| ---------- | ---------------------: |
| Routine    |                  74.89 |
| Emergency  |                  74.35 |

Routine visits had a slightly higher average recovery score, but the difference was small.

### Age Group and Length of Stay

Average length of stay was relatively consistent across age groups:

| Age Group | Average Length of Stay |
| --------- | ---------------------: |
| 18–30     |              4.11 days |
| 31–45     |              4.09 days |
| 46–60     |              4.02 days |
| 60+       |              3.95 days |

The results do not indicate a substantial difference in average length of stay based on age group alone.

### Numerical Relationships

The correlation analysis showed **very weak or negligible linear relationships** among the examined numerical variables.

Examples:

* Treatment Cost ↔ Length of Stay: **-0.022**
* Recovery Score ↔ Readmission Risk: **0.002**
* Treatment Cost ↔ Readmission Risk: **0.018**
* Recovery Score ↔ Treatment Cost: **-0.015**
* Readmission Risk ↔ Length of Stay: **-0.001**

These results indicate that the variables do not have meaningful linear relationships in this dataset.

---

## 📊 Visualizations

The notebook includes:

* Age group distribution
* Gender distribution
* Regional distribution
* Department distribution
* Treatment type distribution
* Visit type distribution
* Numerical variable distributions
* Boxplots for numerical variables
* Treatment cost vs. length of stay
* Recovery score vs. readmission risk
* Treatment cost vs. readmission risk
* Recovery score vs. treatment cost
* Readmission risk vs. length of stay
* Numerical correlation heatmap
* Cramér's V categorical association heatmap
* Mixed-variable association analysis
* Total treatment cost by department
* Average readmission risk by treatment type

---

## 💡 Business / Analytical Takeaways

From an analytical perspective, the project highlights several observations:

* **Orthopedics has the highest total treatment cost**, making it an important area for further cost analysis.
* **Routine visits dominate the dataset**, accounting for more than two-thirds of all visits.
* **Treatment types have similar average readmission risks**, suggesting that additional patient or clinical variables may be needed to explain differences in readmission risk.
* **Recovery scores are similar between routine and emergency visits**, indicating that visit type alone may not strongly differentiate recovery outcomes.
* **Length of stay is relatively consistent across age groups.**
* The numerical variables show **negligible linear correlations**, suggesting that more advanced analysis or additional variables would be needed to identify stronger predictive relationships.

> **Note:** Correlation does not imply causation, and weak linear correlation does not necessarily mean that no relationship exists. The results indicate that the analyzed variables do not show meaningful *linear* relationships in this dataset.

---


## ▶️ How to Run

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd Healthcare-Patient-Data-Analysis
```

### 2. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn scipy dython jupyter
```

### 3. Open the notebook

```bash
jupyter notebook HEALTHCARE_DATA_ANALYSIS.ipynb
```

Alternatively, the notebook can be opened and executed using **Google Colab**.

### 4. Update the dataset path

The notebook currently loads the dataset using a Google Colab path:

```python
df = pd.read_csv("/content/healthcare_patient_data/healthcare_patient_data.csv")
```

If running locally, update the path to the location of `healthcare_patient_data.csv`.

---

## 📚 Skills Demonstrated

This project demonstrates practical skills in:

* Data loading and preparation
* Data quality checking
* Exploratory Data Analysis
* Descriptive statistics
* Categorical data analysis
* Numerical data analysis
* Data visualization
* Outlier detection using IQR
* Correlation analysis
* Categorical association analysis
* Group-by analysis
* Statistical interpretation
* Healthcare data analysis
* Communicating analytical findings

---

## 👤 Author

**Kurt Aaron Delizo**

Aspiring Data Analyst | Computer Engineering Graduate

### Focus Areas

* Data Analysis
* Python
* Exploratory Data Analysis
* Data Visualization

