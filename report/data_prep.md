## Loan Approval Analysis Report — Data Cleaning & Exploratory Data Analysis
1. Background

NY Bank is currently undergoing a transformation to modernize its loan approval process, which has historically relied on manual verification, fragmented systems, and subjective decision-making. These inefficiencies have contributed to inconsistent outcomes, extended processing times, and reduced customer satisfaction.

As digital competitors continue to raise customer expectations for faster, data-driven credit decisions, NY Bank aims to shift toward an analytics-centered operating model.
This project supports that transformation by analyzing historical loan application data to uncover patterns, understand key approval drivers, and support the development of more transparent and consistent decision-making frameworks.

2. Purpose of Data Cleaning & EDA

Before building predictive models, it is essential to:

Ensure the data is clean, consistent, and usable

Understand the characteristics of customers applying for loans

Identify which variables may influence approval outcomes

Detect early signs of bias or imbalance

Provide insights to business stakeholders in a way that supports process redesign

The combination of data cleaning and exploratory data analysis (EDA) forms the foundation of all subsequent modeling and business recommendations.

3. Data Cleaning Summary

Data cleaning ensures that the dataset is reliable for analysis and modeling.
Below is a summary of the key cleaning steps applied, based on your implemented Python code:

3.1 Strip whitespace from column names

Many CSV exports include trailing spaces, which can cause errors.

df.columns = df.columns.str.strip()

3.2 Clean and encode the target variable (loan_status)

The raw values contained inconsistent spacing.
We normalized them and converted to numerical labels:

df['loan_status'] = df['loan_status'].astype(str).str.strip()
df['loan_status'] = df['loan_status'].map({'Approved': 1, 'Rejected': 0})
df = df.dropna(subset=['loan_status'])
df['loan_status'] = df['loan_status'].astype(int)

3.3 Remove irrelevant ID fields

Loan ID does not provide predictive value.

df = df.drop(columns=['loan_id'])

3.4 One-hot encode categorical variables

This prepares the dataset for machine learning:

df_encoded = pd.get_dummies(df, columns=['education', 'self_employed'], drop_first=True)

3.5 Validate target variable integrity

We ensured no missing labels:

y = df_encoded['loan_status']
print(y.isna().sum())


## Outcome:
The cleaned dataset is now structurally consistent, free of invalid loan status labels, and ready for reliable EDA and modeling.

4. Exploratory Data Analysis (EDA)

Five key visualizations were selected to focus on the most influential and interpretable dimensions:
loan status trends, education impact, and income characteristics.

4.1 Loan Status Distribution

The approval rate is greater than the rejection rate, indicating a mild class imbalance.
While not extreme, this imbalance is important for later modeling.

From a business perspective, this suggests NY Bank historically approves more applicants, but the pattern may depend heavily on financial characteristics.
<img width="1053" height="730" alt="image" src="https://github.com/user-attachments/assets/04ee2de6-31e1-4dc9-909a-255bb43f2d02" />


4.2 Education Level Distribution

Graduate and Non-Graduate applicants appear in nearly equal volume, suggesting educational background is well-represented across customer segments.

This balance also means education can be safely used as a feature without introducing demographic bias through sampling imbalance.
<img width="1045" height="738" alt="image" src="https://github.com/user-attachments/assets/08950df5-bb2b-4af0-be93-2a2fe619fbcb" />


4.3 Education vs Loan Status

The stacked bar chart shows that graduates have slightly higher approval rates, while non-graduates have marginally more rejections.

This suggests education may correlate with financial stability or credit behavior.
However, the effect is modest, indicating education should serve as a supporting feature, not a dominant predictor.
<img width="1057" height="694" alt="image" src="https://github.com/user-attachments/assets/d0284ca5-8991-4607-b3c4-3ef3139452c2" />


4.4 Income Annual Distribution

Income distribution is strongly right-skewed, with many low-to-middle income applicants and fewer high-income outliers.
This is typical for financial datasets and underscores the importance of:

considering normalization (e.g., log transform)

using robust measures (median vs mean)

applying tree-based models that handle skew effectively

The distribution also highlights NY Bank’s broad customer coverage across socioeconomic tiers.

4.5 Income vs Loan Status

This is one of the clearest patterns in the dataset:

Approved applicants tend to have higher median annual income

Rejected applicants cluster around lower income brackets

This confirms income is one of the strongest approval determinants.
It also validates traditional underwriting logic — income stability directly affects repayment capacity.
<img width="1009" height="692" alt="image" src="https://github.com/user-attachments/assets/63dd16af-87b2-45a4-8985-f11f53b565c4" />

5. Key Insights and Business Interpretation
Insight 1: Income is the strongest predictor of loan approval

This aligns with industry norms but also signals an opportunity to refine income thresholds or switch to flexible debt-to-income ratios.

Insight 2: Education has a secondary but measurable effect

Graduates have slightly higher approval success, potentially reflecting better employment stability.
NY Bank may consider whether current processes unintentionally disadvantage non-graduate applicants.

Insight 3: Class imbalance is present but manageable

Models may require:

class weighting

careful evaluation metrics beyond accuracy

This helps maintain fairness across applicant groups.

Insight 4: Skewed financial data may require transformation

Right-skewed distributions indicate potential benefit from:

log scaling

robust ML methods

outlier-aware preprocessing

Insight 5: Cleaned data is suitable for modeling and further analysis

The dataset now meets structural expectations for downstream tasks such as:

logistic regression

random forest

gradient boosting classifiers

SHAP-based interpretability

6. Conclusion

The data cleaning and EDA process provides essential clarity on the characteristics that influence loan approval outcomes.
Through structured preprocessing and targeted visual exploration, the analysis highlights income, education, and overall distribution patterns that shape NY Bank’s underwriting decisions.

These results form a strong foundation for building predictive models and for advising NY Bank on how to modernize its loan approval workflow—improving speed, transparency, and consistency across customer segments.
