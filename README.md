# aly6120group-1
# Our Group Project
<img width="945" height="310" alt="image" src="https://github.com/user-attachments/assets/8079a2f9-05d9-458b-9b19-9f321d10f149" />

# Backgound
NY Bank is experiencing operational inefficiencies in its loan approval process, resulting in delayed turnaround times, inconsistent decisions, and low customer satisfaction. These inefficiencies stem from manual documentation checks, disjointed digital systems, and a lack of data-driven insight into workflow bottlenecks. The growing competition in digital banking adds pressure to improve decision speed without compromising risk assessment accuracy. To remain competitive and retain customer trust, NY Bank must transition from reactive decision-making to a proactive, analytics-driven model.
As a transformational leader, I aim to create a culture where data analytics drives decisions and empowers employees to innovate. The goal is to use analytics not only as a technical solution but as a strategic enabler of business improvement, aligning process efficiency with customer-centric outcomes.

# About the Campony

NY Bank is a regional commercial bank with a strong focus on retail loans, personal credit, and SME financing. Its loan approval process evaluates multiple risk-related factors such as credit score, applicant income, employment status, loan term, loan amount, and asset value. The bank seeks to modernize and optimize this process through predictive analytics and workflow redesign.

# Data Source

The dataset used in this project comes from Kaggle, published under the MIT Open Source License, making it freely available for analysis and model development.
The dataset—loan_approval_dataset.csv—contains essential financial and demographic variables commonly used to predict loan approval outcomes. It is widely utilized for machine learning tasks such as classification modeling, risk scoring, and operational workflow simulations. \\

 Dataset uploaded:
/mnt/data/loan_approval_dataset.csv
(Source: Kaggle, MIT License)

# Team Collaboration
To ensure responsible use of this external dataset, collaboration would be required with multiple team members. Data engineers validate the structure, schema, and formatting of the CSV file. Business analysts interpret each variable to align it with real-world financial concepts and avoid misapplication. Data stewards help validate whether field definitions match typical industry standards (e.g., credit score ranges, DTI ratios). Even when using open-source data, cross-functional collaboration is essential to ensure contextual accuracy before modeling.

# **Data Preparation and Quality Issues**
The Kaggle dataset contains several quality challenges typical of open-source financial data. Missing values appear in credit scores, income, and loan purpose fields, requiring investigation to determine if they result from incomplete reporting or synthetic generation. Incorrect or unrealistic data points such as extremely high income values or negative loan amounts must be flagged and treated carefully. Outliers are expected, especially in financial datasets, and require domain-aware decisions about whether they represent legitimate rare events or noise.
Data preparation steps will include:
•	Standardizing categorical fields (e.g., employment status)
•	Normalizing continuous variables where necessary
•	Inspecting missing value mechanisms and selecting imputation methods
•	Removing or correcting obvious errors
•	Creating engineered features such as debt-to-income ratio or processing time
Throughout this process, a version-controlled data dictionary will be maintained to ensure transparency and traceability into modeling.

