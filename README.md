# 💼 LoanGPT: AI-Powered Loan Compliance & Policy Assistant

This project simulates a real-world FinTech scenario, where a company uses **AI-powered tools** to analyze user loan data and check if loan decisions comply with company policy.

It combines **structured data analysis** (CSV files) with **unstructured policy document understanding** using **LangChain, GPT-3.5, and Retrieval-Augmented Generation (RAG)**.

---

## 🚀 What This Project Does

- ✅ Analyzes  loan data from CSVs (users, loans, repayments)
- ✅ Answers natural language questions like:
  - "What is the default rate overall?"
  - "List users under 21 who received loans."
- ✅ Reads a policy document using RAG and answers questions like:
  - "What is the minimum income requirement?"
  - "What is the minimum age to get a loan?"
- ✅ Demonstrates both **AI + Data Analysis + Compliance logic**
- ✅ Validates business rules with GPT and cross-checks with SQL

---
Dataset Overview

The data is simulated using GPT and consists of:

| File                    | Description                                            |
| ----------------------- | ------------------------------------------------------ |
| `users.csv`             | 554 users (user\_id, age, gender, city)                |
| `loan_applications.csv` | 2,000 loans (loan\_id, user\_id, status, amount, date) |
| `repayments.csv`        | 2,500 repayments                                       |
| `loan_eligibility.txt`  | A plain-text policy document                           |


<img width="1194" height="670" alt="image" src="https://github.com/user-attachments/assets/6a749cac-140b-41d8-afe0-85509ca20632" />

📅 Date range: 2023–2025

📁 All files are stored in the data/ folder

---
## Project Structure

LoanGPT-Compliance-Assistant/
### data/

- users.csv
- loan_applications.csv
- repayments.csv
- loan_eligibility.txt

### notebook/

- loan_analysis_project.ipynb

### README.md

--- 
## 🧠 Example Stakeholder Questions

### 📊 Structured Data (via GPT Agent over Pandas)

| Question | Source |
|----------|--------|
| How many users defaulted in the past 12 months? | CSV |
| What is the average loan amount by city? | CSV |

### 📄 Policy Document (via RAG over loan_policy.txt)

| Question | Source |
|----------|--------|
| What is the minimum age? | Document |
| Can users reapply after being rejected? | Document |
| Are there penalties for late repayment? | Document |


---

## 🔍 Policy Summary from RAG

<img width="1383" height="122" alt="image" src="https://github.com/user-attachments/assets/cbefd133-1bdd-4026-82cd-6ffc310cd001" />

Using `doc_agent`, the following rules were extracted from the policy document:

- ✅ Minimum age: **21 years old**
- ✅ Must not have defaulted in the past 12 months
- ✅ Rejected applicants must wait **30 days** to reapply
- ✅ A default = **missed payments for over 60 days**

---

## ✅ GPT vs SQL Validation

To ensure accuracy, GPT responses were verified with SQL:

**Q: Any users under 21 who got approved?** 

<img width="1373" height="277" alt="image" src="https://github.com/user-attachments/assets/88256dba-6459-44b6-a415-b51923d11da7" />

➡️ GPT: 30 

<img width="1580" height="806" alt="image" src="https://github.com/user-attachments/assets/0c269bda-9fdd-4a39-babb-582d3ed6e2b4" />

➡️ SQL: ✅ 30 

✔️ GPT agent and database agreed.

--- 

## 📊 Key Metrics

| Metric | Value |
|--------|-------|
| **Approval Rate (overall)** | 64.6% |
| **Default Rate (overall)** | 26.6% |
| **Approved Loan Count** | 2,273 |
| **Defaulted Loan Count** | 826 |
| **Rejected Loan Count** | 401 |
| **Most Defaults by City** | Jakarta |
| **Highest Average Loan Amount** | Palembang |
| **Lowest Average Loan Amount** | Surabaya |
| **Users Defaulted in Last 12 Months** | 154 users |
| **Approval Rate (Female)** | 63.37% |
| **Approval Rate (Male)** | 66.69% |
| **Correlation (Loan vs Repayment)** | 0.597563 (moderate positive) |

---

## 🛠️ Tech Stack

- 🧠 [LangChain](https://www.langchain.com/)
- 💬 [OpenAI GPT-3.5](https://platform.openai.com/)
- 📚 Retrieval-Augmented Generation (RAG)
- 🔢 Pandas (data analysis)
- 🧪 Jupyter Notebook

---
