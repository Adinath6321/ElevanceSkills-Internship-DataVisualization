# 🎓 ElevanceSkills Technology — Data Visualization Internship

**Intern:** Adinath Chavan  
**Organization:** ElevanceSkills Technology Private Limited  
**Program:** Data Visualization Internship  
**Duration:** 28 Days  
**Tools:** Python (NumPy, Pandas), Jupyter Notebook, Tableau  

---

## 📊 Project Overview

This repository contains the complete work completed during my **Data Visualization Internship** at ElevanceSkills Technology Private Limited. The project involves analyzing a comprehensive **Job Descriptions Dataset** from Kaggle and building **6 professional data visualizations** using Python for data processing and Tableau for interactive dashboards.

---

## 🗂️ Dataset

| Attribute | Details |
|---|---|
| **Name** | Job Descriptions Dataset |
| **Source** | [Kaggle — ravindrasinghrana](https://www.kaggle.com/datasets/ravindrasinghrana/job-description-dataset) |
| **Key Columns** | Job Title, Role, Company, Country, Salary Range, Work Type, Preference, Qualifications, Experience, Latitude, Longitude, Job Portal, Contact Person, Job Posting Date |
| **Salary Format** | Text range (e.g., $55K-$80K) — all exceed $10,000 |
| **Experience Format** | Text range (e.g., 5 to 15 Years) |

---

## 🛠️ Tools & Libraries

```python
# Python Libraries Used
import numpy as np      # Statistical analysis
import pandas as pd     # Data manipulation and filtering

# Visualization Tool
# Tableau Public — Interactive Dashboard
```

> ⚠️ **Note:** Only NumPy and Pandas were used for Python analysis.  
> No visualization libraries (Matplotlib, Seaborn, Plotly) were used.

---

## 📁 Repository Structure

```
ElevanceSkills-Internship/
│
├── 📓 ElevanceSkills_Internship_Final.ipynb  # Jupyter Notebook (all 6 tasks)
├── 🐍 internship_tasks_final.py              # Python source code
│
├── 📊 Filtered CSV Files/
│   ├── task1_filtered.csv                    # Task 1 filtered data
│   ├── task1_summary.csv                     # Task 1 summary stats
│   ├── task2_filtered.csv                    # Task 2 filtered data
│   ├── task3_filtered.csv                    # Task 3 filtered data
│   ├── task3_boxplot_statistics.csv          # Task 3 box plot stats
│   ├── task4_filtered.csv                    # Task 4 filtered data
│   ├── task4_pivot.csv                       # Task 4 pivot table
│   ├── task5_exact_filtered.csv              # Task 5 exact matches
│   ├── task5_filtered_full.csv               # Task 5 reference data
│   ├── task5_top10.csv                       # Task 5 top 10 companies
│   └── task6_filtered.csv                    # Task 6 filtered data
│
├── 📸 Screenshots/
│   ├── task1_bar_chart.png
│   ├── task2_scatter_plot.png
│   ├── task3_box_plot.png
│   ├── task4_india_vs_germany.png
│   ├── task5_treemap.png
│   ├── task6_qualification_map.png
│   └── final_dashboard.png
│
├── 📄 Internship_Report.docx                 # Complete internship report
├── 📄 28_Day_Progress_Report.docx            # Daily progress documentation
└── 📖 README.md                              # This file
```

---

## 🚀 How to Run

### Step 1 — Clone Repository
```bash
git clone https://github.com/YOUR_USERNAME/ElevanceSkills-Internship.git
cd ElevanceSkills-Internship
```

### Step 2 — Install Dependencies
```bash
pip install pandas numpy jupyter
```

### Step 3 — Download Dataset
- Go to [Kaggle Dataset](https://www.kaggle.com/datasets/ravindrasinghrana/job-description-dataset)
- Download `job_descriptions.csv`
- Place it in the same folder as the notebook

### Step 4 — Run Jupyter Notebook
```bash
jupyter notebook ElevanceSkills_Internship_Final.ipynb
```

### Step 5 — Update Dataset Path
```python
# In the notebook, update this line with your path:
DATASET_PATH = r'C:\Your\Path\To\job_descriptions.csv'
```

### Step 6 — Run All Cells
- Click **Cell → Run All**
- All 11 CSV files will be exported automatically

---

## 📊 All 6 Tasks

---

### Task 1 — Preference vs Work Type (Bar Chart)

**Objective:** Show preference distribution among internship job postings

| Filter | Condition |
|---|---|
| Work Type | = Intern |
| Company Size | < 50,000 |
| Salary | > $9,000 (all records exceed this) |
| Sort | Descending by Count |

**Key Finding:** Female preference was highest among intern job postings, followed by Both and Male categories.

**Tableau:** Bar Chart | X=Preference | Y=Count | Color=Preference | Sorted Descending

---

### Task 2 — Company Size vs Company Name (Scatter Plot)

**Objective:** Scatter plot of company size vs company name for Mechanical Engineer roles

| Filter | Condition |
|---|---|
| Job Title | = Mechanical Engineer |
| Company Size | < 50,000 |
| Work Type | Full-Time or Part-Time |
| Preference | = Male |
| Country | Asian countries excl. starting with 'I' |
| Job Portal | = Idealist |
| Company Vowels | ≥ 2 vowels in name |

**Companies Found:** General Dynamics (Cambodia), Knight-Swift Transportation (Lebanon), UGI (Mongolia), Xiaomi Corporation (Pakistan)

**Tableau:** Scatter Plot | X=Company | Y=Company Size | Color=Salary Range | ⏰ 3–5 PM IST

---

### Task 3 — Salary Distribution (Box & Whisker Plot)

**Objective:** Analyze salary distribution for intern roles

| Filter | Condition |
|---|---|
| Work Type | = Intern |
| Latitude | < 10 |
| Company Size | < 50,000 |
| Job Title | Single word < 10 chars (Architect, Paralegal, Teacher) |
| Experience | Even number |
| Posted Date | 2021–2023 |
| Contact Person | Contains letter 'e' |

**Statistics:**
- Architect: Q1=$55K, Median=$60K, Q3=$64K
- Paralegal: Q1=$55K, Median=$60K, Q3=$64K  
- Teacher: Q1=$55K, Median=$60K, Q3=$64K

**Tableau:** Box Plot | X=Job Title | Y=Salary Min | ⏰ 3–5 PM IST

---

### Task 4 — India vs Germany Job Comparison (Stacked Bar Chart)

**Objective:** Compare job postings between India and Germany

| Filter | Condition |
|---|---|
| Country | India or Germany |
| Qualification | = B.Tech |
| Work Type | = Full-Time |
| Job Title | Art Teacher (common to both countries) |
| Job Portal | = Idealist |
| Company Name | > 8 characters |
| Location | Not empty |

> **Note:** Indeed portal returned 0 India records. Idealist was the only portal with both countries' data.

**Tableau:** Stacked Bar | X=Job Title | Y=Count | Color=Country (India=Orange, Germany=Blue)

---

### Task 5 — Top 10 Companies (Tree Map)

**Objective:** Top 10 companies hiring for Data Engineer/Data Scientist roles

| Filter | Condition |
|---|---|
| Role | = Data Engineer |
| Job Title | = Data Scientist |
| Exclude | Asian countries + C-starting countries |
| Company Size | ≥ 10,000 |
| Qualification | = B.Tech |
| Preference | = Female |
| Job Portal | = LinkedIn |
| Date | 01/01/2023 – 06/01/2023 |
| Contact | Name ends with vowel |

**Dual Visualization Approach:**
- **Exact Filter Result:** Fiat Chrysler Automobiles N.V. + Berkeley Group Holdings
- **Top 10 Reference:** Apple, DISH Network, Iluka Resources, Renishaw, Gilead Sciences, Halliburton, Wesfarmers Limited, Chevron, Berkshire Hathaway, Fiat Chrysler

**Tableau:** Tree Map | Size=Postings | Color=Company | ⏰ 3–5 PM IST

---

### Task 6 — Qualification Drilldown Map (Geographic Map)

**Objective:** Geographic map of African country job postings with drilldown

| Filter | Condition |
|---|---|
| Country | African countries (43 listed) |
| Qualification | B.Tech / M.Tech / PhD |
| Work Type | = Full-Time |
| Job Title | Starts with 'D' |
| Preference | = Male |
| Company Size | > 80,000 |
| Salary | > $20,000 (all records exceed this) |
| Job Portal | = Indeed |
| Mapping | Uses Latitude and Longitude |

**Countries Found:** Egypt, Djibouti, Guinea, Gambia, Botswana, Sudan, Senegal, Morocco, Lesotho, Sierra Leone, Ethiopia, South Sudan

**Color Coding:** 🔵 B.Tech | 🟠 M.Tech | 🟢 PhD

**Tableau:** Geographic Map | Color=Qualification | Size=Company Size | Tooltip=Drilldown | ⏰ 3–6 PM IST

---

## 📈 KPIs Measured

| KPI | Value |
|---|---|
| Total Dataset Records | 1,000,000+ |
| Task 1 — Intern Records Filtered | ~8,000+ |
| Task 2 — Mechanical Engineer Records | 4 companies |
| Task 3 — Salary Distribution Records | 319 records |
| Task 4 — India + Germany Records | 2 records |
| Task 5 — LinkedIn Data Scientist Records | 13 records |
| Task 6 — African Country Records | 12 records |
| Average Salary (Task 3) | ~$60,240 |
| Qualifications in Task 6 | B.Tech=4, M.Tech=5, PhD=3 |

---

## 🔄 Data Transformations Applied

```python
# 1. Company Size — removed commas, converted to numeric
df['Company Size'] = pd.to_numeric(
    df['Company Size'].str.replace(',', ''), errors='coerce'
)

# 2. Job Posting Date — parsed to datetime
df['Job Posting Date'] = pd.to_datetime(df['Job Posting Date'], errors='coerce')

# 3. Salary Numeric — parsed from text range
df['Salary_Numeric'] = df['Salary Range'].apply(
    lambda x: float(str(x)[1:str(x).find('K')]) * 1000
)

# 4. Even Experience — extracted first number from text range
def is_even_experience(exp):
    numbers = re.findall(r'\d+', str(exp))
    return int(numbers[0]) % 2 == 0 if numbers else False

# 5. Vowel Count — custom function for company names
def has_two_vowels(name):
    return sum(1 for ch in str(name).lower() if ch in 'aeiou') >= 2
```

---

## 🖥️ Tableau Dashboard

**Live Dashboard:** [View on Tableau Public](YOUR_TABLEAU_PUBLIC_LINK_HERE)

**Dashboard Features:**
- ✅ All 6 visualizations in one dashboard
- ✅ Interactive filters
- ✅ Drill-down tooltips on geographic map
- ✅ Color-coded legends
- ✅ Professional titles with filter conditions
- ✅ Time-based visibility noted in chart titles

---

## 📸 Dashboard Screenshots

> Add your screenshots here after taking them from Tableau

| Task | Preview |
|---|---|
| Task 1 — Bar Chart | ![Task 1](Screenshots/task1_bar_chart.png) |
| Task 2 — Scatter Plot | ![Task 2](Screenshots/task2_scatter_plot.png) |
| Task 3 — Box Plot | ![Task 3](Screenshots/task3_box_plot.png) |
| Task 4 — India vs Germany | ![Task 4](Screenshots/task4_india_vs_germany.png) |
| Task 5 — Tree Map | ![Task 5](Screenshots/task5_treemap.png) |
| Task 6 — Africa Map | ![Task 6](Screenshots/task6_qualification_map.png) |
| Final Dashboard | ![Dashboard](Screenshots/final_dashboard.png) |

---

## ⚠️ Dataset Limitations Documented

| Task | Limitation | Solution Applied |
|---|---|---|
| Task 2 | Salary stored as text ($55K-$80K) | Verified all exceed $50K threshold |
| Task 3 | Experience stored as text range | Used regex to extract first number |
| Task 4 | Indeed portal had no India records | Used Idealist portal (only portal with both countries) |
| Task 5 | Date+vowel filter returned 2 records | Dual visualization: exact + Top 10 reference |
| Task 6 | Contact starting with 'A' = 0 records | Map shown with all 12 valid records |

---

