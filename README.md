# Customer Feedback Automation using Rule-Based Filtering & Generative AI

## Project Overview

This project was developed as part of the **Imarticus Learning Data Science Internship Assessment (Python Foundations & Generative AI)**.

The project focuses on analyzing customer feedback, identifying critical reviews using a rule-based approach, and generating personalized apology emails using a Large Language Model (LLM) through the **Groq API**. It demonstrates how Python and Generative AI can be combined to automate customer support tasks and improve the overall customer experience.

---

## Objectives

- Clean and preprocess customer review data.
- Identify critical customer reviews using rule-based filtering.
- Analyze complaint keywords from negative reviews.
- Select the most critical and detailed customer reviews.
- Generate personalized and empathetic apology emails using Generative AI.

---

## Dataset

This project uses the **Amazon Fine Food Reviews** dataset, which contains Amazon customer reviews, review summaries, ratings, and related product information.

**Dataset Source:**  
https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews

> **Note:** The dataset is not included in this repository because it exceeds GitHub's file upload limit. Please download the dataset from the above source and place the `Reviews.csv` file in the project directory before running the notebook.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Collections (Counter)
- HTML Library
- Groq API
- Jupyter Notebook

---

## Project Workflow

```
Customer Review Dataset
        │
        ▼
Load Dataset
        │
        ▼
Data Cleaning
        │
        ▼
Rule-Based Filtering
(Score ≤ 2)
        │
        ▼
Complaint Keyword Analysis
        │
        ▼
Select Top 3 Critical Reviews
        │
        ▼
Generate Personalized Apology Emails
using Groq API
```

---

## Data Cleaning

The dataset was preprocessed before analysis by:

- Loaded the dataset using Pandas.
- Inspected the dataset structure and data types.
- Checked for missing values.
- Removed unnecessary HTML tags from review text.
- Removed leading and trailing whitespaces.
- Standardized inconsistent text values.
- Converted time-related values into a readable datetime format.
- Prepared the cleaned dataset for keyword analysis and AI processing.

---

## Rule-Based Filtering

Instead of using Machine Learning, a rule-based approach was implemented.

The workflow includes:

- Filtering reviews with a **Score ≤ 2** to identify critical reviews.
- Creating a custom Python function to identify the most common complaint keywords.
- Using **collections.Counter** to calculate keyword frequencies.
- Selecting the most critical reviews based on:
  - Complaint keywords
  - Lowest customer rating
  - Longest review length
---

## Generative AI

The selected critical reviews were sent to the **Groq API**, where the Large Language Model was instructed to act as a professional Customer Support Agent.

The model generated:

- Personalized apology emails
- Empathetic customer responses
- Complaint-specific acknowledgements
- Professional customer support communication

---

## Output

The notebook produces:

- Cleaned customer review dataset
- Critical reviews
- Most common complaint keywords
- Top 3 critical customer reviews
- AI-generated personalized apology emails

---

## API Key Setup

!pip install groq

Create a free API key from the **Groq Console**.

Replace:

```python
client = Groq(api_key="YOUR_API_KEY")
```

with your own API key before running the notebook.

---

## How to Run

1. Clone or download this repository.
2. Download the **Amazon Fine Food Reviews** dataset from Kaggle.
3. Place `Reviews.csv` in the project directory.
4. Install the required libraries.
5. Add your Groq API key.
6. Open the notebook in Jupyter Notebook.
7. Run all cells sequentially.

---

## Project Structure

```
Customer_Feedback_Analysis/

│── Customer_Feedback_GenAI.ipynb
│── README.md
```

---

## Skills Demonstrated

- Python Programming
- Data Cleaning
- Data Wrangling
- Rule-Based Filtering
- Text Processing
- Keyword Frequency Analysis
- Prompt Engineering
- Groq API Integration
- Large Language Models (LLMs)
- Customer Feedback Analysis
- Business Problem Solving

---

## Conclusion

This project demonstrates how Python and Generative AI can be integrated to automate customer feedback analysis and customer support. By combining rule-based filtering with an LLM, the solution efficiently identifies critical reviews and generates personalized, empathetic responses, showcasing practical skills in data preprocessing, text analysis, API integration, and AI-assisted business solutions.

