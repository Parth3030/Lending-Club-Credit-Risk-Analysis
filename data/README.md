# 📁 Data Architecture & Dictionary

## 📌 Dataset Origin & Ingestion Policy
Due to GitHub file size limits, raw datasets (`.csv`) are excluded.

* **Primary Source:** Lending Club Open Dataset (2.26M+ Loan Records)
* **Storage Engine:** SQLite Database (`loans.db`)
* **Pipeline:** Raw CSV $\rightarrow$ Python Data Cleaning $\rightarrow$ SQLite Import $\rightarrow$ SQL Analytics $\rightarrow$ Power BI Dashboard

---

## 🗂️ Data Schema & Field Definitions

| Field Name | Data Type | Business Description |
|---|---|---|
| `id` | INTEGER | Unique identifier assigned to each loan application. |
| `loan_amnt` | REAL | Total capital funded by Lending Club ($). |
| `int_rate` | REAL | Interest rate charged on the loan (%). |
| `grade` | TEXT | Risk grade assigned by underwriters (Grade A through G). |
| `home_ownership` | TEXT | Housing status (`RENT`, `MORTGAGE`, `OWN`). |
| `annual_inc` | REAL | Self-reported annual income ($). |
| `loan_status` | TEXT | Current loan status (`Fully Paid`, `Charged Off`, `Default`). |
| `dti` | REAL | Debt-to-Income leverage ratio (%). |
