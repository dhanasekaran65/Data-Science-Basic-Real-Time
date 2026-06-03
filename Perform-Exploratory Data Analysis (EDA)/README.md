# IBM HR Analytics — Employee Attrition & EDA Basic Concept

A data analytics project that performs Exploratory Data Analysis (EDA) on the IBM HR Analytics Employee Attrition dataset. The project uncovers key workforce insights — attrition patterns, salary trends, gender distribution, and department-level comparisons — using Python visualization libraries.

## Project Overview

| Item | Detail |
|---|---|
| **Dataset** | IBM HR Analytics — `HR-Employee-Attrition.csv` |
| **Goal** | Understand employee attrition through exploratory data analysis |
| **Key Focus Areas** | Attrition patterns, overtime impact, salary vs experience, gender distribution, department comparison |
| **Libraries** | Pandas, NumPy, Matplotlib, Seaborn |

## Project Structure

├── IBM-HR-Analytics-Employee-Attrition-Dataset.ipynb   
├── Perform_EDA.ipynb                                    
├── HR-Employee-Attrition.csv                           
├── datasets.csv                                       
└── README.md

## Getting Started

### Prerequisites

```bash
pip install pandas numpy matplotlib seaborn
```

### Running the Notebooks

1. Clone this repository
   ```bash
   gh repo clone dhanasekaran65/Data-Science-Basic-Real-Time
   cd Data-Science-Basic-Real-Time
   ```

2. Place `HR-Employee-Attrition.csv` in the path referenced in the notebook.

3. Launch Jupyter
   ```bash
   jupyter notebook
   ```

> **Google Colab users:** Upload the CSV file to your Colab session and update the file path accordingly.

---

## IBM HR Attrition Analysis

### EDA Workflow

| Step | Description |
|---|---|
| Load dataset | Read CSV using Pandas |
| Inspect data | `.head()`, `.info()`, `.describe()` |
| Correlation heatmap | Identify relationships between numeric features |
| Attrition count plot | Visualize Yes vs No attrition |
| Monthly income distribution | Histogram with KDE curve |

### Key Business Questions Answered

**1. Which department has the highest attrition?**
Cross-tabulation and count plot to compare attrition across departments.

**2. Does overtime affect attrition?**
Percentage breakdown of attrition by overtime status.

**3. Relationship between salary and experience**
Scatter plot of `YearsAtCompany` vs `MonthlyIncome` with correlation analysis.

**4. Gender distribution**
Pie chart showing workforce diversity.

**5. Average salary by department**
Bar chart comparing department-wise compensation.

---

## General EDA Framework

A step-by-step EDA template applicable to any dataset.

| Step | Method |
|---|---|
| Import libraries | Pandas, NumPy, Matplotlib, Seaborn |
| Load dataset | `pd.read_csv()` |
| View data | `.head()`, `.tail()`, `.shape` |
| Dataset info | `.info()` |
| Statistical summary | `.describe()` |
| Missing values | `.isnull().sum()` |
| Duplicate records | `.duplicated().sum()` |
| Numerical analysis | Histogram, Boxplot |
| Categorical analysis | Value counts, Count plot |
| Correlation analysis | Heatmap |
| Relationship analysis | Scatter plot |
| Pair plot | `sns.pairplot()` |
| Outlier detection | Boxplot + IQR method |

---

## Visualizations

- Correlation heatmap (coolwarm)
- Employee attrition count plot
- Monthly income distribution (histogram + KDE)
- Department-wise attrition (grouped bar chart)
- Experience vs salary scatter plot
- Gender distribution pie chart
- Average salary by department bar chart
- Revenue histogram and boxplot
- Market capitalization count plot
- Pair plot
- Outlier detection boxplot

## Key Insights

- Employees working **overtime** show significantly higher attrition rates
- **Monthly income** has a positive correlation with years at the company
- Certain **departments** experience higher turnover than others
- **Gender distribution** and **salary benchmarks** across departments provide diversity and compensation insights

## Libraries Used

- [Pandas](https://pandas.pydata.org/) — data loading and manipulation
- [NumPy](https://numpy.org/) — numerical operations
- [Matplotlib](https://matplotlib.org/) — base visualizations
- [Seaborn](https://seaborn.pydata.org/) — statistical visualizations

## Dataset

The IBM HR Analytics Employee Attrition dataset is a fictional dataset created by IBM data scientists. It is publicly available on [Kaggle](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset).

## Learning Outcomes

- Understand the complete EDA workflow
- Identify patterns and anomalies in HR data
- Detect outliers using the IQR method
- Create meaningful business insights from raw data
- Build reusable EDA templates for any dataset
