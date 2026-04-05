# 📊 Credit Card Approval Analysis using Python

## 🎯 Project Overview
This project analyzes credit card application data to identify key factors influencing approval and rejection decisions. Using Python-based data analysis and visualization, the project extracts meaningful insights to support data-driven business decision-making.

## 💼 Business Problem
Financial institutions must evaluate credit card applications efficiently while minimizing risk. This project addresses:
* **What factors influence credit approval?**
* **Which customers are likely to be rejected?**
* **How can risk be identified early?**

---

## 🛠️ Tools & Technologies
* **Python**: Core programming language.
* **Pandas**: Data manipulation and analysis.
* **Matplotlib & Seaborn**: Data visualization.
* **Jupyter Notebook**: Development environment.

## 🧠 Skills Demonstrated
* Data Cleaning & Preprocessing
* Exploratory Data Analysis (EDA)
* Statistical Analysis
* Business Insight Generation
* Analytical Thinking & Storytelling

---

## 📂 Dataset Information
* **Total Records**: 690
* **Features**: 16 columns (A1–A14, anonymized)
* **Target Variable (Class)**: 
    * `1` → Approved
    * `0` → Rejected

---

## 🧹 Data Cleaning & Preprocessing
To ensure the reliability of insights, the following steps were performed:
1.  **Structure Audit**: Used `.info()` and `.head()` to understand data types.
2.  **Missing Value Check**: Verified via `.isnull().sum()`.
3.  **Duplicate Check**: Confirmed no redundant records existed.
4.  **Consistency**: Ensured all features were numeric and ready for modeling.

> **Business Impact**: A clean dataset reduces the risk of biased decision-making and ensures model accuracy.

---

## 🔍 Exploratory Data Analysis (EDA)
### Key Observations
* **Skewness**: Many features show skewed distributions, requiring careful handling during modeling.
* **Outliers**: Significant outliers were identified in feature **A14**.
* **Behavioral Gaps**: Clear statistical differences exist between approved and rejected applicant profiles.

### 📊 Visual Insights
| Visualization | Key Insight |
| :--- | :--- |
| **Approval vs Rejection** | The dataset shows a higher rejection rate, indicating conservative credit approval policies. |
| **Top Factors** | A8 is the strongest predictor of approval. |
| **Correlation Matrix** | Strong relationships between **A8, A9, and A10**, suggesting linked financial behaviors. |
| **Feature A13** | Acted as a strong indicator for **Risk/Rejection**. |

---

📊 Key Visualizations & Insights

### 🔹 Approval vs Rejection

![Approval vs Rejection](<outputs/approval_vs_rejection.png>)

**Insight:**
Slightly more rejected applications than approved
Indicates relatively strict approval criteria

### 🔹 Top Factors Influencing Approval

![Top Factors Influencing Approval](<outputs/top_factors_influencing_approval.png>)

**Insight:**
A14 dominates approval decisions
Other features (A10, A2, A5, A7) have smaller but meaningful impact

### 🔹 Normalized Feature Impact

![Normalized Feature Impact](<outputs/normalized_feature_impact.png>)

**Insight:**
A14 shows high magnitude impact, but correlation analysis indicates A8 is the strongest predictor.

### 🔹 Distribution of A14

![Distribution of A14](<outputs/a14_distribution.png>)

**Insight:**
Highly right-skewed distribution
Presence of extreme high-value applicants

### 🔹 Approved vs Rejected (A14)

![Approved vs Rejected](<outputs/approved_vs_rejected_distribution.png>)

**Insight:**
Approved customers tend to have higher A14 values

### 🔹 A14 vs Class (Boxplot)

![Boxplot](<outputs/a14_vs_class_boxplot.png>)

**Insight:**
Approved group has higher median and wider spread
Significant outliers present

### 🔹 Correlation Matrix

![Correlation Matrix](<outputs/a14_vs_class_boxplot.png>)

**Insight:**
Strong correlations among A8, A9, A10
These features likely represent related financial behavior

### 🔹 A10 vs Approval

![A10 vs Approval](<outputs/a10_vs_approval.png>)

**Insight:**
Higher A10 values increase approval probability

### 🔹 Pairplot Analysis

![Pairplot](<outputs/pairplot.png>)

**Insight:**
Partial separation between approved and rejected groups
Indicates potential for predictive modeling

### 🔹 A14 vs A10 Scatter Plot

![A14 vs A10 Scatter Plot](<outputs/a14_vs_a10_scatter.png>)

**Insight:**
Approved customers cluster in higher-value regions
Combination of features improves decision clarity


---

## 📈 Statistical & Risk Analysis
### 🟢 Approval Drivers
* **A8 (0.72 correlation)**: The strongest predictor of approval.
* **A9 & A10**: High positive impact on approval probability.
* **A14**: High-magnitude feature that significantly influences the final decision.

### 🧪 Analytical Approach
- Compared group means using `.groupby()`
- Used correlation matrix to identify linear relationships
- Applied feature difference analysis between approved vs rejected
- Used distribution plots to detect skewness and outliers

### 🔴 Risk Indicators
* **A13** shows negative association with approval and may contribute to risk evaluation.

---

## 💡 Business Recommendations
1.  **Prioritize High-Potential Leads**: Focus on applicants scoring high in features **A8, A9, and A10**.
2.  **Strict Risk Mitigation**: Implement automated flags for high **A13** values to trigger manual reviews.
3.  **Scoring Model**: Develop a weighted credit scoring system based on the top 5 identified drivers.
4.  **Outlier Management**: Apply robust scaling to **A14** to prevent extreme values from distorting the approval logic.

---

## 🚀 Conclusion & Future Scope
This project demonstrates how data-driven analysis can optimize the credit approval pipeline. By focusing on high-impact variables, financial institutions can reduce risk while improving the speed of approvals.
