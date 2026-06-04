# Employee Analytics — Data Visualizations

A comprehensive data visualization project that explores employee analytics data using **20 different chart types** with Python. The project covers everything from basic bar charts to advanced cluster maps, providing deep insights into salary trends, department distribution, attrition patterns, and workforce demographics.

## Project Overview

| Item | Detail |
|---|---|
| **Dataset** | Employee Analytics — `employee_analytics.csv` |
| **Goal** | Create and understand 20 types of data visualizations |
| **Key Insights** | Salary trends, gender distribution, department attrition, experience vs salary |
| **Libraries** | Pandas, NumPy, Matplotlib, Seaborn |


## Project Structure

├── Create_Data_Visualizations.ipynb   
├── employee_analytics.csv            
└── README.md

## Dataset Features

| Column | Description |
|---|---|
| `Employee_ID` | Unique employee identifier |
| `Department` | Department name |
| `Gender` | Employee gender |
| `Age` | Employee age |
| `Salary` | Monthly salary |
| `Experience_Years` | Years of work experience |
| `Performance_Rating` | Performance score |
| `Attrition` | Whether employee left (Yes/No) |

## Getting Started

### Prerequisites

```bash
pip install pandas numpy matplotlib seaborn
```

### Running the Notebook

1. Clone this repository
   ```bash
   gh repo clone dhanasekaran65/Data-Science-Basic-Real-Time
   cd Data-Science-Basic-Real-Time
   ```

2. Place `employee_analytics.csv` in the project root (or update the path in the notebook).

3. Launch Jupyter
   ```bash
   jupyter notebook Create_Data_Visualizations.ipynb
   ```

> **Google Colab users:** Upload `employee_analytics.csv` to your Colab session before running.


## 20 Visualizations Covered

### 📊 Comparison Charts
| # | Chart Type | Purpose |
|---|---|---|
| 1 | **Bar Chart** | Average salary by department |
| 2 | **Count Plot** | Number of employees per department |
| 13 | **Stacked Bar Chart** | Department vs attrition breakdown |

### 🥧 Distribution Charts
| # | Chart Type | Purpose |
|---|---|---|
| 3 | **Pie Chart** | Gender distribution |
| 4 | **Histogram** | Age distribution |
| 14 | **Donut Chart** | Department distribution |

### 📈 Trend & Density Charts
| # | Chart Type | Purpose |
|---|---|---|
| 5 | **KDE Plot** | Salary density curve |
| 9 | **Line Chart** | Salary trend across employees |
| 12 | **Area Chart** | Age and experience comparison |

### 🔍 Spread & Outlier Detection
| # | Chart Type | Purpose |
|---|---|---|
| 6 | **Box Plot** | Detect salary outliers |
| 7 | **Violin Plot** | Salary distribution by gender |
| 15 | **Swarm Plot** | Salary spread by department (sampled) |
| 16 | **Strip Plot** | Salary spread by department (jittered) |

### 🔗 Relationship Charts
| # | Chart Type | Purpose |
|---|---|---|
| 8 | **Scatter Plot** | Experience vs salary |
| 10 | **Pair Plot** | Relationships between numeric variables |
| 17 | **Joint Plot** | Experience vs salary (combined view) |
| 18 | **Regression Plot** | Experience vs salary with trend line |
| 20 | **Hexbin Plot** | Dense scatter for experience vs salary |

### 🌡️ Correlation Charts
| # | Chart Type | Purpose |
|---|---|---|
| 11 | **Heatmap** | Correlation matrix of numeric features |
| 19 | **Cluster Map** | Clustered correlation matrix |

## Key Insights

- **Salary vs Experience** — positive correlation confirmed via regression and joint plots
- **Department Attrition** — stacked bar chart reveals which departments have higher turnover
- **Gender Distribution** — pie chart shows workforce diversity split
- **Salary Outliers** — box plot and violin plot identify high-salary anomalies
- **Age Distribution** — histogram shows the majority age band of the workforce

## Libraries Used

- [Pandas](https://pandas.pydata.org/) — data loading and manipulation
- [NumPy](https://numpy.org/) — numerical operations
- [Matplotlib](https://matplotlib.org/) — base chart rendering
- [Seaborn](https://seaborn.pydata.org/) — statistical and advanced visualizations

## Learning Outcomes

- Create 20 different types of data visualizations in Python
- Choose the right chart type for each data question
- Detect outliers, trends, and correlations visually
- Build reusable visualization code for any dataset
- Understand workforce analytics through data storytelling
