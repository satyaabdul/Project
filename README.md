# Capstone Project: Customer Support Classification and Summarization using IBM Granite

This project aims to classify and summarize real customer support messages using IBM Granite via the Replicate platform. It is part of a capstone assignment to demonstrate the use of large language models (LLMs) for intelligent customer service analytics.

---

## 🎯 Project Overview

- **Objective:** Automatically classify customer support queries into predefined categories and summarize the content in one short sentence.
- **Use Case:** Improve customer service workflow by routing tickets and surfacing insights faster.
- **Model Used:** [IBM Granite 3.3-8B Instruct](https://replicate.com/ibm-granite/granite-3.3-8b-instruct) via [Replicate](https://replicate.com)
- **Platform:** Google Colab + Python

---

## 🗃️ Dataset

- **Source:** [Customer Support on Twitter – Kaggle](https://www.kaggle.com/datasets/thoughtvector/customer-support-on-twitter)
- **Access via:** [`kagglehub`](https://pypi.org/project/kagglehub/)
- **Description:** Tweets between customers and support teams across various brands. Only inbound messages (from customers) are used for classification and summarization.

---

## 🧪 Task Description

For each customer message, the model performs:

1. **Classification** into one of:
   - Technical  
   - Payment  
   - Product Request  
   - Other

2. **Summarization** in **no more than one sentence**

---

## 🛠️ Tech Stack

- `kagglehub` – for dataset loading from Kaggle  
- `langchain_community.llms.Replicate` – to access IBM Granite  
- `pandas` – for data processing and comparison  
- `Google Colab` – as interactive notebook environment

---

## 📊 Results and Output

- The notebook compares two outputs:
  - `response` → without generation parameters
  - `response_param` → with adjusted decoding parameters (e.g., `max_tokens`, `top_p`, etc.)
- Results are shown side by side in a table for evaluation and interpretation.

---

## 📁 Files

- `Capstone_Project_Customer_Support_Classification_and_Summarization.ipynb` — Main analysis notebook

---

## ✅ How to Run

1. Upload your Replicate API token to Google Colab using:
   ```python
   from google.colab import userdata
   userdata.set("api_token", "your_replicate_token")
2. Run all cells from top to bottom.

The notebook will:

- Load the dataset from Kaggle

- Generate prompts per tweet

- Send them to IBM Granite

- Compare outputs with and without parameters


Author
Satya Abdul Halim Bahtiar
