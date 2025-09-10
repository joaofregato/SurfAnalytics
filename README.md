# SurfAnalytics 🏄‍♂️📊  
**World Surf League Data Analysis with Databricks & Power BI**

---

## 📌 Project Overview  
**SurfAnalytics** is a data project that combines **Databricks** for processing and **Power BI** for visualization, delivering insights into **World Surf League (WSL)** results, events, and athletes.  

---

## 🎯 Objectives
- Build an **interactive dashboard** answering real business questions:  
  - Who are the most frequent champions?  
  - Which nationalities dominate the sport?  
  - How do surfers perform across seasons and events?  
- Demonstrate a **data pipeline workflow**: extraction → transformation → modeling → visualization.  
- Showcase practical proficiency in:  
  - **Power BI** (data modeling, DAX, report design)  
  - **Databricks** (ETL & SQL processing)  
  - **GitHub** (project documentation & version control).  

---

## 🛠️ Languages & Tools
- **SQL** → data queries & manipulation in Databricks  
- **DAX** → metrics and calculations in Power BI  
- **Power BI** → dashboard design & storytelling  
- **Databricks** → ETL and notebook-based data processing  

---

## 📂 Data Sources
- **Official WSL site** → [worldsurfleague.com](https://www.worldsurfleague.com)  

Raw datasets include:  
1. `raw_wsl_championships` → world champions since 1976  
2. `raw_wsl_results_events` → all CT events (2011–2024)  
3. `raw_wsl_surfers` → surfer profiles (stance, hometown, nationality)  

---

## 🔄 Project Workflow
### 1. **Data Collection**
- Data extracted from WSL’s official site and stored in CSV format.  

### 2. **Data Processing (Databricks)**
- ETL pipeline for cleaning and transformation.  
- Located under `/databricks`, three notebooks handle extraction and processing before exporting to Power BI.  

### 3. **Data Modeling (Power BI)**
- Star schema design for performance and clarity.  
- A **secondary relationship** was implemented between `d_wslsurfers` and `f_wslevents` to calculate finals reached per surfer.  
- The `USERELATIONSHIP()` DAX function activates this relationship when required.  
- Alternative → create an additional dimension table, but the chosen approach is simpler and cleaner for this dataset.  

### 4. **Visualization (Power BI Dashboard)**
- Two main report pages:  

#### 🏆 **WSL Champions**
- List of all world champions since 1976.  
- Top 3 surfers with the most world titles.  
- Nationalities with the highest number of championships.  

#### 🌍 **WSL Events**
- CT events from 2011 to 2024.  
- Top 3 surfers with most event wins.  
- Nationalities with the most event titles.  
- Full event list with filters (e.g., “Brazilian titles only” or “best-performing surfer per location”).  

💡 **Tooltip Feature**:  
Hovering on champions or events provides extra surfer details, enhancing the analysis depth.  

---

## 📁 Repository Structure
```plaintext
/SurfAnalytics
│── /databricks       # Databricks notebooks (ETL)
│── /power bi         # Power BI report (.pbix)
│── /raw data         # Original datasets (CSV)
│── /images           # Dashboard screenshots
│── README.md         # Documentation


🚀 How to Use

Clone/download this repository.

Open SurfAnalytics.pbix in Power BI Desktop.

Explore dashboards and interact with filters/tooltips.

📸 Dashboard Preview

(Add screenshots from your Power BI dashboard in /images folder)














