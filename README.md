# HR Analytics — Employee Attrition EDA

Exploratory Data Analysis (EDA) on an HR employee dataset to understand what drives employee attrition.

## Project Overview

This notebook analyzes ~15,000 employee records to identify patterns behind why employees leave the company. The target variable is `left` (1 = employee left, 0 = stayed).

The analysis covers:
- Data loading and inspection
- Distribution analysis of numeric features
- Outlier detection using IQR method
- Attrition comparison across every feature
- Correlation heatmap to find strongest drivers

## Dataset

- File: `data123.xlsx`
- Rows: 14,999 employees
- Columns: 18 (10 used in analysis)

| Column | Description |
|---|---|
| satisfactoryLevel | Employee satisfaction score (0–1) |
| lastEvaluation | Last performance evaluation score (0–1) |
| numberOfProjects | Number of projects assigned |
| avgMonthlyHours | Average monthly working hours |
| timeSpent.company | Years spent at the company |
| workAccident | Whether employee had a work accident (0/1) |
| left | Target — left the company (0/1) |
| promotionInLast5years | Promoted in last 5 years (0/1) |
| dept | Department |
| salary | Salary band (low/medium/high) |

## Tools Used

- Python
- Pandas — data loading and inspection
- Matplotlib — base plotting
- Seaborn — boxplots, countplots, heatmap
- Jupyter / Google Colab

## Analysis Steps

1. **Load and inspect** — `head()`, `shape`, `describe()`, `info()`
2. **Boxplots** — visualise spread and outliers for each numeric column
3. **IQR outlier check** — calculate q1, q3, IQR, upper/lower limits
4. **Countplots** — compare each feature split by `left` (attrition)
5. **Correlation heatmap** — find which features correlate with attrition

## Key Findings

- **Satisfaction level is the strongest driver of attrition** — correlation of **-0.35** with `left`. Lower satisfaction → higher chance of leaving.
- `numberOfProjects` and `avgMonthlyHours` are positively correlated (**0.33**) — employees with more projects work longer hours.
- `lastEvaluation` correlates with `numberOfProjects` (**0.27**) — more projects tend to mean higher evaluations.
- Most employees stay (class imbalance) — visible in the countplots where `left = 0` dominates.

## How to Run

1. Clone the repo:

2. Install dependencies:
pip install pandas numpy matplotlib seaborn openpyxl jupyter
3. Place `data123.xlsx` in the same folder as the notebook.
4. Open the notebook:


## Author

**Junaid Narkar**
Data Analyst | SQL · Power BI · Python
Kuwait

- LinkedIn: [linkedin.com/in/junaidnarkar-analyst](https://www.linkedin.com/in/junaidnarkar-analyst)
- GitHub: [github.com/Junaid-Narkar](https://github.com/Junaid-Narkar)
