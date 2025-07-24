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

---
Dataset Overview

This data is stimulated using Chat GPT, consist of 3 table (User: 554 rows, Loan Application: 2000 rows, Repayment 2500 row) from 2023-2025

<img width="1194" height="670" alt="image" src="https://github.com/user-attachments/assets/6a749cac-140b-41d8-afe0-85509ca20632" />

---

## 🧠 Example Stakeholder Questions

### 📊 Structured Data (via GPT Agent over Pandas)

| Question | Source |
|----------|--------|
| How many users defaulted in the past 12 months? | CSV |
| What is the average loan amount by city? | CSV |
| How many users were approved within 30 days after rejection? | CSV |
| List users under 21 with loans over 10M. | CSV |
| Show approval rate by gender. | CSV |

### 📄 Policy Document (via RAG over loan_policy.txt)

| Question | Source |
|----------|--------|
| What is the minimum income to apply? | Document |
| Can users reapply after being rejected? | Document |
| Are there penalties for late repayment? | Document |
| What documentation is required for high-value loans? | Document |

---

## 🗂 Project Structure


## 🛠️ Technologies Used

- **LangChain**
- **OpenAI GPT-3.5**
- **RAG (Retrieval-Augmented Generation)**
- **Chroma Vector Store**
- **Pandas**
- **Jupyter Notebook**
