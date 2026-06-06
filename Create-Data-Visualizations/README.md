# 📊 Python Data Science Basic & Visualization Portfolio

> A complete hands-on learning series covering Data Visualization, Trend Analysis, and Correlation Analysis using Python — built with real-world datasets.

---

## 🗂️ Repository Structure

```
📦 Data-Science-Basic-Real-Time
 ┣ 📦Data-Visualization
    ┣ 📓 Analyze_trends_in_datasets.ipynb
    ┣ 📓 Build_Heatmaps.ipynb
    ┣ 📓 Create_Data_Visualizations.ipynb
    ┣ 📓 Create_Scatter_Plot.ipynb
    ┣ 📓 Develop_Box_Plot.ipynb
    ┣ 📓 Generate_Histogram.ipynb
    ┣ 📓 Perform_Correlation_Analysis.ipynb
    ┣ 📄 employee_analytics.csv
    ┣ 📄 mtcars.csv
    ┣ 📄 sales_data.csv
    ┗ 📄 README.md
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3 | Core programming language |
| Jupyter Notebook | Interactive development environment |
| pandas | Data loading, manipulation, groupby |
| numpy | Numerical operations, random data |
| matplotlib | Core plotting engine |
| seaborn | Statistical visualizations |

### Install dependencies

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

---

## 📚 Notebooks

---

### 1. 📈 Analyze Trends in Datasets
**File:** `Analyze_trends_in_datasets.ipynb`

Trend analysis identifies **patterns, growth, and decline over time**.

| Technique | Code | Purpose |
|---|---|---|
| Line chart | `plt.plot(month, sales, marker='o')` | Visualize direction |
| Grid overlay | `plt.grid(True)` | Readability |
| Growth rate | `sales.pct_change() * 100` | Monthly % change |
| Moving average | `sales.rolling(window=3).mean()` | Smooth fluctuations |
| MoM difference | `sales.diff()` | Absolute change per period |
| Peak detection | `df.loc[df['Sales'].idxmax()]` | Find best month |
| Summary stats | `df.describe()` | Mean, std, quartiles |
| Overlaid chart | Actual + Moving Avg + Growth Rate | Full trend picture |

**Real data — sales_data.csv (Jan–Dec):**

| Metric | Value |
|---|---|
| Lowest month | January → ₹12,000 |
| Highest month | December → ₹30,000 |
| Annual growth | +150% |
| Best growth rate | December → +15.38% |
| Decline months | June (−2.77%), September (−4.54%) |
| Average monthly sales | ₹19,583 |
| Largest MoM jump | October → +₹3,000 |

**Moving average windows:**

| Window | Use case |
|---|---|
| `window=3` | Short-term smoothing |
| `window=6` | Half-year trend |
| `window=12` | Full-year trend |

**Trend interpretation:**
- ↗ Upward line = Growth trend
- ↘ Downward line = Declining trend
- → Flat line = Stable trend

**When to use:** Sales forecasting, business performance tracking, time-series analysis.

---

### 2. 🔥 Build Heatmaps
**File:** `Build_Heatmaps.ipynb`

Heatmaps show **all variable relationships simultaneously** using color intensity.

| Technique | Code | Purpose |
|---|---|---|
| Basic heatmap | `sns.heatmap(data)` | Color-coded grid |
| Annotations | `annot=True` | Show values on cells |
| Coolwarm palette | `cmap='coolwarm'` | Red=high, Blue=low |
| Viridis palette | `cmap='viridis'` | Sequential color scale |
| YlGnBu palette | `cmap='YlGnBu'` | Yellow to Blue |
| Reds palette | `cmap='Reds'` | Single-tone scale |
| DataFrame heatmap | `sns.heatmap(df, annot=True)` | Direct DataFrame |
| Correlation heatmap | `sns.heatmap(df.corr())` | Variable relationships |
| Professional format | `linewidths=1, fmt='.2f', figsize=(8,6)` | Publication-ready |
| mtcars heatmap | `mt_cars.corr(numeric_only=True)` | 11-feature analysis |

**Real correlation results (Age, Salary, Experience):**

| Pair | Correlation | Meaning |
|---|---|---|
| Age ↔ Salary | 0.94 | Strong positive |
| Age ↔ Experience | 0.98 | Very strong positive |
| Salary ↔ Experience | 0.98 | Very strong positive |

**Correlation value guide:**

| Value | Meaning |
|---|---|
| 1.0 | Perfect positive |
| 0.8 | High positive |
| 0.5 | Moderate positive |
| 0.0 | No relationship |
| -0.5 | Moderate negative |
| -1.0 | Perfect negative |

**When to use:** Feature selection, understanding variable relationships before ML modeling.

---

### 3. 🎨 Create Data Visualizations (20 Charts)
**File:** `Create_Data_Visualizations.ipynb`

A comprehensive EDA notebook with **20 chart types** on a real employee analytics dataset.

**Dataset:** `employee_analytics.csv`

| Column | Type | Description |
|---|---|---|
| Employee_ID | int | Unique identifier |
| Age | int | Employee age |
| Gender | str | Male / Female |
| Department | str | HR, IT, Finance, etc. |
| Job_Role | str | Role title |
| Salary | float | Monthly salary |
| Experience_Years | int | Years of experience |
| Performance_Rating | float | Rating score |
| Attrition | str | Yes / No |

**All 20 Charts:**

| # | Chart Type | Code | Use Case |
|---|---|---|---|
| 1 | Bar Chart | `df.groupby('Department')['Salary'].mean().plot(kind='bar')` | Avg salary by dept |
| 2 | Count Plot | `sns.countplot(x='Department', data=df)` | Employee count per dept |
| 3 | Pie Chart | `plt.pie(gender_counts, autopct='%1.1f%%')` | Gender distribution |
| 4 | Histogram | `plt.hist(df['Age'], bins=5)` | Age distribution |
| 5 | KDE Plot | `sns.kdeplot(df['Salary'], fill=True)` | Salary density |
| 6 | Box Plot | `sns.boxplot(y='Salary', data=df)` | Salary outliers |
| 7 | Violin Plot | `sns.violinplot(x='Gender', y='Salary', data=df)` | Salary by gender |
| 8 | Scatter Plot | `sns.scatterplot(x='Experience_Years', y='Salary', data=df)` | Experience vs Salary |
| 9 | Line Chart | `plt.plot(df['Employee_ID'], df['Salary'])` | Salary trend |
| 10 | Pair Plot | `sns.pairplot(df[['Age','Salary','Experience_Years','Performance_Rating']])` | All relationships |
| 11 | Heatmap | `sns.heatmap(corr, annot=True, cmap='coolwarm')` | Correlation matrix |
| 12 | Area Chart | `df[['Age','Experience_Years']].head(50).plot.area()` | Age vs Experience |
| 13 | Stacked Bar | `pd.crosstab(df['Department'], df['Attrition']).plot(kind='bar', stacked=True)` | Dept vs Attrition |
| 14 | Donut Chart | Pie + `plt.Circle((0,0), 0.70, fc='white')` | Dept distribution |
| 15 | Swarm Plot | `sns.swarmplot(x='Department', y='Salary', data=sample_df)` | Salary spread |
| 16 | Strip Plot | `sns.stripplot(x='Department', y='Salary', jitter=True)` | Salary by dept |
| 17 | Joint Plot | `sns.jointplot(x='Experience_Years', y='Salary', kind='scatter')` | Combined view |
| 18 | Regression Plot | `sns.regplot(x='Experience_Years', y='Salary', data=df)` | Trend line |
| 19 | Cluster Map | `sns.clustermap(corr, annot=True)` | Clustered correlation |
| 20 | Hexbin Plot | `df.plot.hexbin(x='Experience_Years', y='Salary', gridsize=20)` | Dense scatter |

**Chart categories:**

| Category | Charts |
|---|---|
| Distribution | Histogram, KDE Plot, Box Plot, Violin Plot |
| Comparison | Bar Chart, Count Plot, Stacked Bar, Area Chart |
| Relationship | Scatter, Pair Plot, Joint Plot, Regression, Hexbin |
| Statistical | Heatmap, Cluster Map, Swarm Plot, Strip Plot |
| Part-to-Whole | Pie Chart, Donut Chart, Line Chart |

---

### 4. 🔵 Create Scatter Plot
**File:** `Create_Scatter_Plot.ipynb`

Scatter plots answer: **"Do X and Y move together?"**

| Technique | Code | Purpose |
|---|---|---|
| Basic scatter | `ax.scatter(x, y)` | Simple X vs Y |
| Compare 2 datasets | Two `plt.scatter()` calls | Overlay comparison |
| Custom color per series | `color='green'` / `color='blue'` | Differentiate groups |
| Color per dot | `c=['red','blue','green'...]` | Encode extra variable |
| Color maps | `cmap='viridis'` / `cmap='nipy_spectral'` | 100+ palettes available |
| Custom marker | `marker='*'` | Style the dots |
| Bubble chart | `s=size_array` | Dot size = data value |
| Transparency | `alpha=0.5` | Show overlapping points |
| Colorbar | `plt.colorbar()` | Legend for color scale |
| Random scatter | `np.random.randint(100, size=100)` | 100-point simulation |
| Seaborn scatter | `sns.scatterplot(data=df, x='x', y='y')` | DataFrame-based |

**When to use:** Finding relationships, validating correlations, pre-regression analysis.

---

### 5. 📦 Develop Box Plot
**File:** `Develop_Box_Plot.ipynb`

Box Plots reveal **outliers, spread, and median** in a single chart.

| Technique | Code | Purpose |
|---|---|---|
| Vertical box plot | `plt.boxplot(data)` | Default orientation |
| Horizontal box plot | `vert=False` | Alternative layout |
| Colored box | `patch_artist=True, facecolor='green'` | Visual styling |
| Show mean | `showmeans=True` | Display mean marker |
| Notch plot | `notch=True` | Confidence interval |
| Outlier detection | Dataset with value `200` in range `20–90` | Spot anomalies |
| Multi-group comparison | `[maths, science, english]` | Side-by-side comparison |
| Seaborn box plot | `sns.boxplot(x='Subject', y='Marks', data=df)` | DataFrame-based |

**Datasets used:** Student marks | `mtcars.csv` (HP analysis, Auto vs Manual mileage)

**Key insight:** Value `200` detected as a clear outlier in a dataset ranging 20–90.

**When to use:** Outlier detection, comparing distributions across groups.

---

### 6. 📊 Generate Histogram
**File:** `Generate_Histogram.ipynb`

Histograms answer one question: **"How is my data distributed?"**

| Technique | Code | Purpose |
|---|---|---|
| Basic histogram | `ax.hist(data)` | Frequency distribution |
| Custom bins | `ax.hist(data, [0,35,60,80,100])` | Grade-based ranges |
| Face & edge color | `fc='green', ec='black'` | Visual styling |
| Multi-subject overlay | 3 `ax.hist()` on one plot | Compare distributions |
| Bin control | `bins=6` | Group data into N buckets |
| Normal distribution | `np.random.normal(170, 500, 200)` | Simulate real-world data |

**Datasets used:** Student marks — Maths, Science, English

**When to use:** Understanding shape of data before any analysis or modeling.

---

### 7. 🔗 Perform Correlation Analysis
**File:** `Perform_Correlation_Analysis.ipynb`

Correlation analysis **quantifies relationships** between variables.

| Technique | Code | Purpose |
|---|---|---|
| Correlation matrix | `df.corr()` | All-vs-all relationships |
| Coolwarm heatmap | `sns.heatmap(corr, annot=True, cmap='coolwarm', fmt='.2f')` | Student marks |
| Viridis heatmap | `sns.heatmap(corr_matrix, cmap='viridis', linecolor='red')` | mtcars data |
| Ranked correlation | `corr['Marks'].sort_values(ascending=False)` | Feature importance |
| Filter strong pairs | `corr[(corr > 0.7) & (corr < 1.0)]` | Extract meaningful only |
| Numeric columns only | `select_dtypes(include='number')` | Auto-filter |
| Scatter validation | `sns.scatterplot(df, x='Study_Hours', y='Marks')` | Visual confirmation |

**Real results — Student dataset:**

| Pair | Correlation | Insight |
|---|---|---|
| Study_Hours ↔ Marks | **+0.99** | Near-perfect positive |
| Sleep_Hours ↔ Marks | **-0.99** | Strong negative trade-off |
| Study_Hours ↔ Sleep_Hours | **-1.00** | Perfect inverse |

**Real results — mtcars dataset (pairs with r > 0.70):**

| Pair | Correlation | Insight |
|---|---|---|
| cyl ↔ disp | 0.90 | More cylinders = larger engine |
| wt ↔ disp | 0.89 | Heavier car = bigger engine |
| cyl ↔ hp | 0.83 | More cylinders = more horsepower |
| disp ↔ hp | 0.79 | Bigger engine = more power |
| am ↔ gear | 0.79 | Transmission linked to gear count |
| drat ↔ am | 0.71 | Gear ratio linked to transmission |

> ⚠️ **Remember:** Correlation ≠ Causation. Always validate with a scatter plot!

---

## 📁 Datasets

| File | Used In | Description |
|---|---|---|
| `employee_analytics.csv` | Create_Data_Visualizations | 9 columns — salary, dept, attrition, performance |
| `mtcars.csv` | Develop_Box_Plot, Build_Heatmaps, Perform_Correlation_Analysis | 32 cars, 11 features (mpg, cyl, hp, wt...) |
| `sales_data.csv` | Analyze_trends_in_datasets | 12 months Jan–Dec sales figures |

---

## 🚀 How to Run

```bash
# Clone the repository
gh repo clone dhanasekaran65/Data-Science-Basic-Real-Time
cd Data-Science-Basic-Real-Time

# Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# Launch Jupyter
jupyter notebook
```

Open any `.ipynb` file to run the notebooks.

---

## 📌 Key Concepts Summary

| Concept | Best Chart | Key Function |
|---|---|---|
| Data distribution | Histogram | `ax.hist()` |
| Outlier detection | Box Plot | `plt.boxplot()` |
| Variable relationship | Scatter Plot | `ax.scatter()` |
| All correlations | Heatmap | `sns.heatmap(df.corr())` |
| Time-based trends | Line Chart + Moving Avg | `pct_change()`, `rolling().mean()` |
| Feature correlation | Correlation Analysis | `df.corr()`, filter `> 0.7` |
| Full EDA | Pair Plot | `sns.pairplot()` |

---

## 🙏 Acknowledgements

Special thanks to **Boopathi Kumar K** for the exceptional guidance, real-world examples, and consistent mentorship throughout this Data Science learning journey.

---
