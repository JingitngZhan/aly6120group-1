# aly6120group-1
# Our Group Project
# Business Understanding: AI-Driven Loan Approval Optimization at NY Bank
## Section 1 - Overview of the Business Problem (Samuel)
NY Bank is experiencing operational inefficiencies in its loan approval process, resulting in delayed turnaround times, inconsistent decisions, and low customer satisfaction. These inefficiencies stem from manual documentation checks, disjointed digital systems, and a lack of data-driven insight into workflow bottlenecks. The growing competition in digital banking adds pressure to improve decision speed without compromising risk assessment accuracy. To remain competitive and retain customer trust, NY Bank must transition from reactive decision-making to a proactive, analytics-driven model.
As a transformational leader, I aim to create a culture where data analytics drives decisions and empowers employees to innovate. The goal is to use analytics not only as a technical solution but as a strategic enabler of business improvement, aligning process efficiency with customer-centric outcomes.

## Section 2 - Business Objectives and Leadership Requirements (Jonas) 
Business Objectives
From a business perspective, this analytics initiative will aim to:
i.	Reduce loan approval time by at least 40% through automation and workflow optimization.
ii.	Improve decision consistency and fairness by introducing data-driven risk scoring models.
iii.	Enhance customer satisfaction by delivering faster, transparent, and equitable loan decisions.
These objectives directly support NY Bank’s strategic goals of operational excellence, digital transformation, and long-term client retention

Leadership Requirements
To ensure successful implementation, three leadership requirements are essential:
i.	Cross-functional collaboration: Encouraging open communication between IT, analytics, and loan departments to ensure shared ownership of outcomes.
ii.	Ethical and transparent analytics culture: Building trust in AI-driven decisions by prioritizing explainability, fairness, and bias mitigation.
iii.	Continuous learning and adaptability: Fostering a mind-set of agility where teams view analytics as a dynamic process that evolves with feedback and performance data.
As a leader, I will guide this transformation by applying emotional intelligence, data literacy development, and empowerment strategies to ensure both technical and human alignment.

## Section 3 - Connecting the Business Problem to a Data Mining Solution (Jingting)
The problems that NY Bank is facing in its loan approval process can actually be solved quite effectively through data mining and artificial intelligence (AI) techniques. Basically, the approval process can be seen as a classification problem, where we want to predict whether an applicant should be approved or not based on past data. Using this kind of data-driven approach will help the bank make faster, fairer, and more accurate decisions. Instead of relying too much on human judgment, the system will use machine learning models to find patterns that people might easily miss.

### 1. Data Preparation and Feature Selection

Before building any predictive models, it’s really important to clean the data and make sure we are using the right features. The dataset would likely include things like income, credit score, age, employment stability, debt ratio, and repayment history. To handle these efficiently, we can use LASSO regression (L1 regularization) to automatically select the most important variables and remove the ones that don’t really help the model. This helps keep the model simple and prevents overfitting.

Also, checking for multicollinearity is necessary. Sometimes, different variables are too closely related to each other, which can cause instability in the model. To deal with that, the Variance Inflation Factor (VIF) can be used to detect and fix those issues. These two steps—LASSO and VIF—make the data more reliable and the model more interpretable, which is especially important for a bank because of the transparency and compliance requirements.

### 2. Predictive Modeling and AI Techniques

Once the data is clean and the features are selected, we can apply several machine learning algorithms. Logistic Regression can be the first step since it’s easy to interpret and gives probability-based scores. This makes it useful for explaining why a loan is approved or not, which is critical for financial reporting.

Then, we can use more advanced models like Random Forest and XGBoost to improve accuracy. These models can handle complex relationships between variables and capture non-linear patterns that simple models can’t. Random Forest is great because it’s stable and less likely to overfit, while XGBoost can make predictions very precisely by learning from mistakes in each round. Together, they can create a strong predictive system that improves both speed and accuracy in loan approvals.

### 3.Automation with NLP and OCR

To make the process even more efficient, Natural Language Processing (NLP) and Optical Character Recognition (OCR) can be added to automate how data is collected. For example, the system can read pay slips, ID cards, or tax reports and automatically extract the information needed for analysis. This reduces manual work and also lowers the chance of human error. It also means that customers can get their loan decisions faster because the verification part becomes automated.

### 4. Leadership and Ethical Considerations

From a leadership point of view, implementing AI is not just about technology—it’s also about people and trust. As the analytics lead, I will make sure the models are fair and transparent, especially since financial decisions directly affect people’s lives. Regular model audits, fairness checks, and bias detection are necessary to keep the process ethical.

## References
Bokrantz, J., Subramaniyan, M., & Skoogh, A. (2024). Realising the promises of artificial intelligence in manufacturing by enhancing CRISP-DM. Production Planning & Control, 35(16), 2234–2254. https://doi.org/10.1080/09537287.2023.2234882
Northouse, P. G. (2022). Leadership: Theory and Practice (9th ed.). Sage Publications.

I also believe in building a continuous learning culture where team members are encouraged to explore data, ask questions, and update models as new information comes in. AI should not replace people, but support them in making better decisions. With this approach, NY Bank can truly become a data-driven organization, where analytics doesn’t just make processes faster, but also helps the bank earn long-term trust from its customers.
