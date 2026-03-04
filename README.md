# 📊 Job Market Demand Intelligence Dashboard

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Azure](https://img.shields.io/badge/Azure-Databricks-0078D4)
![PowerBI](https://img.shields.io/badge/Visualization-PowerBI-yellow)
![PySpark](https://img.shields.io/badge/Processing-PySpark-orange)
![DataAnalytics](https://img.shields.io/badge/Domain-Data%20Analytics-green)

**Job Market Demand Intelligence** is an end-to-end cloud data analytics project designed to analyze real-world job postings and uncover trends in **salary distribution, experience demand, hiring companies, remote work patterns, and technical skill requirements**.

The project demonstrates a **modern cloud data pipeline** using **Azure Databricks, Python EDA, and Power BI** to transform raw job posting data into actionable insights about the evolving AI and technology job market.

---

# 🌟 Key Features

### 📊 Comprehensive Job Market Analysis
Analyze hiring patterns across thousands of job postings including:

- Salary trends across experience levels
- Demand distribution by experience level
- Top hiring companies
- Remote vs onsite job trends
- Most requested technical skills

---

### ☁️ Cloud Data Processing

Data is processed using **Azure Databricks** following the **Medallion Architecture**:

- Bronze Layer → Raw data ingestion  
- Silver Layer → Data cleaning and transformation  
- Gold Layer → Analytical feature engineering  

---

### 📈 Interactive Business Intelligence Dashboard

Power BI dashboard provides visual insights into:

- Experience vs Salary
- Job Distribution by Experience Level
- Skill Demand Trends
- Hiring Company Activity
- Job Posting Trends

---

### 🧠 Skill Demand Intelligence

Identifies emerging skill clusters including:

- Python
- Computer Vision
- NLP
- Cloud Platforms (Azure, AWS, GCP)
- Modern AI frameworks and tools

---

# 🧱 Architecture


Open Source Job Dataset
↓
Azure Data Lake Storage
↓
Azure Databricks (PySpark Processing)
↓
Gold Analytical Dataset
↓
Databricks SQL Warehouse
↓
Jupyter Notebook (EDA)
↓
Power BI Dashboard

<img width="1536" height="1024" alt="Job Market Demand Intelligence Architecture" src="https://github.com/user-attachments/assets/325bdc56-57e9-4cfd-a440-701f7fb4d560" />


---

# 🛠️ Technology Stack

| Technology | Purpose |
|-----------|--------|
| **Azure Databricks** | Data engineering & transformation |
| **Azure Data Lake Storage** | Cloud data storage |
| **PySpark** | Data processing |
| **Python (Pandas, Matplotlib)** | Exploratory Data Analysis |
| **Databricks SQL Warehouse** | Data serving layer |
| **Power BI** | Data visualization dashboard |

---

# 📂 Project Structure

```
Job-Market-Intelligence/
│
├── notebooks/
│ └── job_market_eda.ipynb
│
├── data/
│ └── jobs_data_2026.csv
│
├── dashboard/
│ └── powerbi_dashboard.pbix
│
├── images/
│ └── dashboard_preview.png
│
├── README.md
└── requirements.txt
```


---

# 🚀 Installation & Setup

Follow these steps to run the analysis locally.

## 1️⃣ Clone the Repository


git clone https://github.com/prathamehaphale-007/Job-Market-Demand-Intelligence-Dashboard.git

cd job-market-intelligence


---

## 2️⃣ Install Dependencies


pip install pandas matplotlib seaborn databricks-sql-connector


---

## 3️⃣ Connect to Azure Databricks

Example Python connection code:

```
from databricks import sql
import pandas as pd

connection = sql.connect(
server_hostname="your-databricks-host",
http_path="your-sql-warehouse-path",
access_token="your-access-token"
)

query = "SELECT * FROM analytics_view"
df = pd.read_sql(query, connection)
```

---

## 4️⃣ Run the Jupyter Notebook

Launch Jupyter:


jupyter notebook


Open:


job_market_eda.ipynb


Run all cells to reproduce the analysis.

---

# 📊 Exploratory Data Analysis

The project includes multiple EDA modules:

### 🔎 Missing Value Analysis

Identifies incomplete fields across the dataset.

**Finding**

Salary fields contain ~43% missing values because many companies do not publicly disclose salary ranges.

---

### 💰 Salary Analysis

Key statistics:

- Average Salary → **$114K**
- Median Salary → **$102K**
- Maximum Salary → **$565K**

Senior roles show the highest compensation levels.

---

### 📊 Experience Level Distribution

Most job postings target **Mid-level professionals**.

Distribution pattern:

- Mid-level → dominant hiring demand  
- Senior → second largest segment  
- Junior → limited opportunities

This reflects industry preference for experienced candidates.

---

### 🌍 Remote Work Trends

Remote distribution:

- Remote → ~10%
- Hybrid → ~6%
- Onsite → ~2%
- Unspecified → majority

Many listings leave remote policy unspecified.

---

### 🏢 Top Hiring Companies

Organizations with highest posting counts include:

- Instacart
- Mercor
- Meta
- Oracle
- Lockheed Martin

Indicating strong hiring activity across both startups and large enterprises.

---

### 🧠 Skill Demand Analysis

Top technical skills identified:

| Skill | Demand Count |
|------|-------------|
| Python | 298 |
| Computer Vision | 276 |
| NLP | 170 |
| Azure | 128 |
| R | 104 |
| SQL | 79 |
| AWS | 71 |

The dataset strongly reflects **AI/ML-driven hiring demand**.

---

### 📈 Job Posting Trends

Job postings increase sharply in **2025–2026**, reflecting recent growth in AI and technology hiring.

---

# 📊 Power BI Dashboard

The interactive dashboard visualizes key insights from the dataset.

### Dashboard Highlights

- Experience vs Salary comparison
- Job distribution by experience level
- Skill demand visualization
- Hiring company activity
- Job posting trend analysis

---

# 📌 Key Insights

- Mid-level professionals dominate hiring demand.
- Python remains the most required programming language.
- AI domains like **Computer Vision and NLP** are highly demanded.
- Cloud platforms such as **Azure and AWS** are frequently required.
- Salary is influenced by specialization more than experience alone.

---

# ⚠️ Limitations

- Salary data missing in ~43% of records.
- Dataset reflects recent scraping activity.
- Results represent job postings, not official labor statistics.

Despite this, the analysis provides meaningful insight into current technology hiring trends.

---

# 🔮 Future Improvements

Possible extensions of this project:

- Skill gap analysis against candidate resumes
- Automated job scraping pipeline
- Machine learning model to predict salary ranges
- Real-time job market monitoring dashboard
- Resume-job matching engine

---

# 👨‍💻 Author

**Prathmesh Aphale**

Data Analytics | Cloud Data Engineering | AI Enthusiast

---

# ⭐ Support

If you found this project useful, consider giving the repository a **star ⭐**.
