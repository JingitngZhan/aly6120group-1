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
# Models we employed and why?
To discover meaningful patterns in the NY Bank loan approval dataset, Exploratory, Predictive and Operational Efficiency Models models would be employed to contribute differently to understanding the data, improving decision quality, and optimizing operational efficiency.
. Exploratory Pattern-Discovery Models
Unsupervised models align with Provost & Fawcett’s (2013) emphasis on understanding data structure before prediction. K-means and PCA reveal borrower segments and underlying financial drivers, supporting Collier’s (2012) value-driven analytics approach. Saporito (2015) highlights operational insight, and these techniques help detect anomalies, fraud signals, and risk patterns essential for policy redesign and fair lending decisions
. Predictive Modelling for Loan Approval Decisions
These predictive models reflect Provost & Fawcett’s (2013) guidance that analytics must directly support decision quality. Logistic regression provides transparent, regulator-friendly insights, while random forests capture nonlinear relationships and reduce overfitting, aligning with Collier’s (2012) value-driven modeling approach. Gradient boosting delivers high accuracy on financial data, consistent with Saporito’s (2015) emphasis on models that enhance operational performance. Together, they support NY Bank’s goal of fast, fair, data-driven approval
. Operational Efficiency Models
The use of process mining and queuing models aligns closely with the analytical frameworks emphasized in Collier (2012), Provost & Fawcett (2013), and Saporito (2015). Process mining and queuing models directly reflect the guidance of Collier (2012), Provost & Fawcett (2013), and Saporito (2015). These authors emphasize understanding real workflows before modeling outcomes. Process mining uncovers operational inefficiencies, while queuing theory predicts performance under varying conditions. Together, they strengthen decision-making, improve service speed, and support NY Bank’s evidence-based process transformation
. Why These Models Are Optimal?
This model combination is optimal because it aligns analytics directly with operational decision-making. Provost & Fawcett (2013) emphasize selecting models that improve real decisions, while Collier (2012) advocates iterative, value-driven development. Saporito (2015) reinforces using models that enhance both accuracy and operational performance. Together, these approaches deepen insight, streamline workflows, and strengthen NY Bank’s data-driven transformation.
# References
Collier, K. (2012). Agile analytics: A value-driven approach to business intelligence and data warehousing. Pearson Education.

Provost, F., & Fawcett, T. (2013). Data science for business: What you need to know about data mining and data-analytic thinking. O’Reilly Media.

Saporito, P. (2015). Applied insurance analytics: A framework for driving more value from data assets, technologies, and tools. Pearson FT Press.

Kaggle. (n.d.). Loan Approval Dataset [Data set]. MIT License. https://www.kaggle.com
