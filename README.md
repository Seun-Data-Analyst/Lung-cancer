<h1 align="center">🩺 Lung Cancer Data Analysis</h1>
<p align="center">
Analysis of lung cancer data using Python (pandas, matplotlib), focusing on demographics, lifestyle, comorbidities, and treatment outcomes to guide prevention and care strategies.
  <!-- Badges -->
<p align="center">
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square" alt="Status Badge">
  <img src="https://img.shields.io/badge/Data%20Cleaning-✓-blue?style=flat-square" alt="Data Cleaning Badge">
  <img src="https://img.shields.io/badge/Insights-14-orange?style=flat-square" alt="Insights Badge">
  <img src="https://img.shields.io/badge/Recommendations-14-yellow?style=flat-square" alt="Recommendations Badge">
</p>

---

## 📑 Table of Contents
- [Introduction](#-introduction)
- [Objectives](#-objectives)
- [Scope](#-scope)
- [Key Columns](#-key-columns)
- [Data Cleaning Process](#-data-cleaning-process)
- [Key Insights](#-key-insights)
- [Recommendations](#-recommendations)
- [Conclusion](#-conclusion)

---

- ## 🧾1. Introduction
This report aims to analyze data related to lung cancer. Lung cancer is a major contributor to cancer-related deaths, making the study of its epidemiology and treatment outcomes paramount.  
This dataset provides an in-depth look at various factors linked to lung cancer diagnosis and management. It contains essential information on patient demographics, clinical histories, and treatment outcomes, enabling researchers and healthcare providers to better understand the disease's prevalence and development.

---

## 🎯1.1 Objectives
1. Examine the influence of age, gender, and country of residence on lung cancer diagnosis and treatment outcomes.
2. Explore the effects of comorbid conditions (such as hypertension, asthma, and cirrhosis) on treatment efficacy and patient survival.
3. Determine the role of family history in lung cancer risk and its implications for early diagnosis and intervention.
4. Assess the effectiveness of different treatment types (surgery, chemotherapy, radiation therapy) on patient survival rates.
5. Investigate how BMI and cholesterol levels relate to lung cancer progression and treatment success.

---

## 🗂️1.2 Scope
This report specifically examines key variables, grouped as follows:

#### I. Demographic Variables
- **Age**: Age of the patient at diagnosis.  
- **Gender**: Gender of the patient.  
- **Country**: Country of residence of the patient.  

#### II. Clinical Variables
- **Diagnosis Date**: Date when lung cancer was diagnosed.  
- **Cancer Stage**: Stage of cancer at the time of diagnosis.  
- **Family History**: Presence of lung cancer in the family.  

#### III. Lifestyle Factors
- **Smoking Status**: Current or past smoking habits.  
- **BMI**: Body Mass Index of the patient.  
- **Cholesterol Level**: Cholesterol levels measured.  

#### IV. Comorbid Conditions
- **Hypertension**: Presence of high blood pressure.  
- **Asthma**: History of asthma.  
- **Cirrhosis**: Presence of liver cirrhosis.  

#### V. Treatment Variables
- **Treatment Type**: Type of treatment received (e.g., surgery, chemotherapy).  
- **End Treatment Date**: Date when treatment concluded.  

#### VI. Outcome Variable
- **Survived**: Indicator of whether the patient survived beyond a specified follow-up period.  

---

## 🧩 Key Columns
| Column | Description |
|-------|-------------|
| `ID` | Unique patient identifier |
| `Age` | Age at diagnosis |
| `Gender` | Patient gender |
| `Country` | Country of residence |
| `Diagnosis Date` | Date of diagnosis |
| `Cancer Stage` | Stage I – IV |
| `Family History` | Presence of cancer history |
| `Smoking Status` | Never, Passive, Former, Current |
| `BMI` | Body Mass Index |
| `Cholesterol Level` | Low, Medium, High |
| `Treatment Type` | Surgery, Chemotherapy, Radiation, Combined |
| `Survived` | Binary survival outcome |
| `Number of Days Treatment` | Treatment duration |
| `Weight` | Patient weight |

---

## 🧹2. Data Cleaning Process

1. **Removing Duplicates**  
   - Used `drop_duplicates()` to identify and remove duplicate rows.  

2. **Checking Data Types**  
   - Used `data.dtypes` to confirm correct data types for each column and avoid errors during analysis.  

3. **Checking Null Values**  
   - Used `data.isna().sum()` to identify missing values, which could affect accuracy.  

4. **Checking Unique Values**  
   - Used `data.unique()` to check the number of unique values per column and detect anomalies.  

---

## 📊3. Key Insights

### 3.1 Most Common Age Group Affected by Cancer
- **Analysis:** Age groups were categorized into children, teenagers, adults, and the elderly.  
- **Insights:**  
  - **Adults**: 597,823 cases (highest incidence).  
  - **Elderly**: 290,742 cases.  
  - **Teenagers**: 1,401 cases (rare).  
  - **Children**: 35 cases (very rare).  

### 3.2 Survival Rate Across Age Groups
- **Analysis:** Compared survival rates across all age groups.  
- **Insights:**  
  - **Adults:** 78% dead, 22% survived.  
  - **Teenagers:** Highest survival rate (23.1%).  
  - **Children:** 22.86% survived.  
  - **Insight:** Age slightly influences survival, with teenagers showing better outcomes.

### 3.3 Cancer Rates by Gender
- **Analysis:** Compared male vs. female incidence.  
- **Insights:**  
  - **Males:** 445,134 cases.  
  - **Females:** 444,866 cases.  
  - **Insight:** Males are marginally more affected.  

### 3.4 Survival Rates by Gender
- **Analysis:** Compared survival outcomes by gender.  
- **Insights:**  
  - **Male Survival:** 22.08%  
  - **Female Survival:** 22.02%  
  - **Insight:** Slightly more males survived compared to females.  

### 3.5 Countries Most Affected
- **Insights:**  
  - **Highest:** Malta (33,367 cases)  
  - **Next:** Ireland (33,243), Portugal (33,208)  
  - **Lowest:** Bulgaria (32,559 cases)

### 3.6 Most Common Treatment Type
- **Insights:**  
  - **Most Common:** Chemotherapy (223,262 cases)  
  - **Least Common:** Radiation (220,868 cases)

### 3.7 Treatment Type and Survival Rate
- **Insights:**  
  - **Surgery:** Highest survival rate (22.15%)  
  - **Chemotherapy:** Highest death rate (78.13%)

### 3.8 Smoking Status
- **Insights:**  
  - **Passive Smokers:** 223,170  
  - **Never Smoked:** 222,751  
  - **Former Smokers:** 222,181  
  - **Current Smokers:** 221,898  

### 3.9 Smoking Status and Survival
- **Insights:**  
  - **Never Smoked:** Highest survival rate (22.13%)  
  - **Former Smokers:** Highest death rate (77.99%)

### 3.10 Family History of Cancer
- **Insights:**  
  - **With Family History:** 49.98%  
  - **Without Family History:** 50.02%  
  - **Insight:** Nearly equal distribution, but genetic factors still significant.

### 3.11 Cholesterol Levels
- **Insights:**  
  - **Low:** 26.67%  
  - **Medium:** 22.21%  
  - **High:** 51.12% (majority of patients)

### 3.12 Cancer Stages
- **Insights:**  
  - **Stage IV:** Highest survival rate (22.16%)  
  - **Stage I:** Highest death rate (78.14%)

### 3.13 Weight Analysis
- **Insights:**  
  - **Obese:** 68.84% (majority)  
  - **Normal:** 22.41%  
  - **Underweight:** 8.46%  
  - **Overweight:** 0.28%

### 3.14 Comorbid Conditions
- **Insights:**  
  - **Asthma:** 418,069 cases (21.9% survival)  
  - **Cirrhosis:** 201,101 cases (22.17% survival)  
  - **Other Cancers:** 78,460 cases (21.76% survival)

---

## 🧠4. Recommendations

### 4.1 Adults (Most Affected Age Group)
- Implement targeted cancer screening programs for adults.  
- Promote lifestyle modification campaigns.  
- Raise awareness on early detection signs.  

### 4.2 Survival Across Age Groups
- Investigate protective factors for teenagers with higher survival rates.  
- Improve access to advanced treatment for adults and elderly.  
- Integrate palliative care for high-risk groups.  

### 4.3 Gender-Based Cancer Rates
- Design gender-sensitive cancer prevention strategies.  
- Encourage regular screening for men.  
- Fund research on gender-related risk factors.  

### 4.4 Survival by Gender
- Investigate reasons behind higher female mortality.  
- Encourage gender-specific support programs.  
- Standardize treatment guidelines for equity.  

### 4.5 High-Incidence Countries
- Study environmental/lifestyle factors in Malta, Ireland, Portugal.  
- Strengthen early detection infrastructure.  
- Share best practices from lower-incidence countries.  

### 4.6 Chemotherapy (Most Common Treatment)
- Improve chemotherapy effectiveness and reduce side effects.  
- Educate patients on treatment options.  
- Invest in targeted therapy research.  

### 4.7 Treatment & Survival
- Expand access to surgery where feasible.  
- Use genetic profiling for personalized treatment plans.  
- Integrate multi-disciplinary care approaches.  

### 4.8 Smoking Status
- Launch anti-smoking campaigns and enforce smoke-free policies.  
- Provide free cessation programs for smokers.  

### 4.9 Smoking and Survival
- Monitor former and passive smokers closely.  
- Include smoking history in treatment planning.  

### 4.10 Family History
- Encourage genetic counseling and early screening.  
- Promote healthy lifestyle changes for high-risk families.  

### 4.11 Cholesterol Levels
- Investigate links between high cholesterol and cancer.  
- Integrate cholesterol checks into screening programs.  
- Promote dietary changes for cholesterol management.  

### 4.12 Cancer Stages
- Strengthen early cancer detection efforts.  
- Improve treatment access for Stage I patients.  
- Enhance follow-up programs for Stage IV survivors.  

### 4.13 Weight Management
- Prioritize obesity prevention programs.  
- Monitor underweight patients for underlying conditions.  
- Promote workplace wellness initiatives.  

### 4.14 Comorbid Conditions
- Develop multi-disease management programs.  
- Coordinate care between oncology and other specialties.  

---

## 🏁5. Conclusion
This analysis provides a comprehensive overview of factors influencing lung cancer incidence and survival.  
Key findings include:
- Adults bear the highest disease burden.  
- Teenagers have the best survival outcomes.  
- Males are slightly more affected, but females show slightly higher mortality.  
- Chemotherapy is the most common treatment, but surgery yields the best survival rates.  
- Obesity, smoking, and high cholesterol are significant risk factors.  

**Overall:** A multi-pronged approach combining prevention, early detection, personalized treatment, and comorbidity management is essential to improve survival rates and quality of life for patients.

---
