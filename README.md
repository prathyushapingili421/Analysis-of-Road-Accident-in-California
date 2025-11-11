
# 🚗 Analysis of Road Accidents in California  
**Data Engineering ▪️ ETL Pipeline ▪️ Data Warehouse ▪️ Dashboarding**  
*AWS Glue ▪️ AWS Redshift ▪️ PostgreSQL ▪️ S3 ▪️ MongoDB Charts*

---

## 📌 Project Overview

This project analyzes road accident trends in California using a **cloud-based data engineering pipeline**.  
The dataset was sourced from the **California Open Data Portal (Road Traffic Injuries dataset)** and processed using AWS services to uncover insights related to:

- Weather conditions  
- Time of day  
- Driver behavior (including cellphone usage)  
- Road and lighting conditions  

The goal: **identify patterns that support better road-safety decision-making.**

---

## 🛠 Tech Stack

| Component | Technology Used |
|----------|-----------------|
| **Data Source** | California Open Data Portal – Road Traffic Injuries dataset |
| **Database** | PostgreSQL → AWS RDS → AWS Redshift |
| **ETL & Data Pipeline** | AWS Glue (Crawler + ETL Jobs + Catalog), S3 |
| **Visualization** | AWS Redshift Dashboards, MongoDB Charts |
| **Programming / Querying** | Python, SQL |
| **Project Collaboration** | Jira Kanban, Zoom, Google Docs |
| **Version Control** | GitHub |

---

## 📂 Data Warehouse Schema

The Redshift data warehouse uses a **star schema** to optimize analytical queries.

### **Fact & Dimension Tables**

| Table | Type | Description |
|-------|------|-------------|
| `accidents` | Fact table | Weather, surface, lighting, severity, location, timestamp |
| `parties` | Dimension | Driver/party details — age, cellphone use, movement before collision |
| `victims` | Dimension | Victim demographics and injury type |

---

## 🧩 Entity Relationship Diagram (ERD)


<img width="1263" height="528" alt="image" src="https://github.com/user-attachments/assets/7b37b17c-1fa3-4c65-aece-d4f3e248f599" />



---

## ⭐ Star Schema

<img width="795" height="680" alt="image" src="https://github.com/user-attachments/assets/3a20f18c-76d6-485e-b8c5-3206f34c5b42" />

---

## 🌩 AWS Architecture



<img width="773" height="437" alt="image" src="https://github.com/user-attachments/assets/5376a036-d8fa-4313-97bd-20be8b6913ab" />


---

## 🚀 Steps Performed (End-to-End Pipeline)

1. Imported accident dataset from the California Open Data Portal
2. Cleaned the dataset (handled nulls, formatting, datatype alignment)
3. Loaded data into PostgreSQL (local staging)
4. Configured **AWS Glue Crawler** → discovered metadata → stored catalog in S3
5. Built **Glue ETL Job** → transformed data + loaded into **AWS Redshift**
6. Modeled warehouse into **star schema**
7. Built dashboards using **MongoDB Charts / AWS Redshift Dashboards**

---

## 📊 Key Insights

✅ Accidents peak during **evening commute hours (5–6 PM).**

✅ Fatal crashes occur mostly during **clear weather**, indicating human behavior over environment.

✅ **Cellphone distraction** correlates with higher accident counts.

✅ Majority of fatalities occur when vehicles are **moving straight**, not turning.


---



## ✅ Lessons Learned

* AWS Glue accelerates ETL over manual scripting in Python/Pandas.
* Debugging Redshift networking (VPC routing / endpoint settings) builds real cloud experience.
* Pair programming + Jira tracking improved productivity and collaboration.

---

## 📁 Repository Structure

```
/data             — dataset files or link to dataset source
/scripts          — ETL SQL scripts / Glue jobs
/visualizations   — dashboard screenshots, ERD, star schema, architecture diagrams
/report           — academic project documentation
README.md         — project overview (this file)
```

---

## 📜 Dataset Reference

Dataset Source:
🔗 [https://data.ca.gov/dataset/road-traffic-injuries](https://data.ca.gov/dataset/road-traffic-injuries)

---



### 📄 License

This project is open for educational and learning use.
Feel free to fork, clone, and build upon it.


