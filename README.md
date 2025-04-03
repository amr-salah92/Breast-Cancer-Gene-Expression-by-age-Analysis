# Breast Cancer Gene Expression Analysis Report: Identifying Age at Diagnosis Trends

---

## Table of Contents

1. [Project Name](#1-project-name)
2. [Project Background](#2-project-background)
3. [Project Goals](#3-project-goals)
4. [Data Structure & Initial Checks](#4-data-structure--initial-checks)
5. [Executive Summary](#5-executive-summary)
6. [Insights Deep Dive](#6-insights-deep-dive)
7. [Recommendations](#7-recommendations)
8. [Technical Details](#8-technical-details)
9. [Assumptions and Caveats](#9-assumptions-and-caveats)

---

## 1. Project Name

**Company**: Breast Cancer Genomics Research Institute\
**Analysis**: Association Between Cancer Type and Cellularity & Age at Diagnosis Trends

---

## 2. Project Background

The Breast Cancer Genomics Research Institute is conducting a study to explore associations between cancer type and cellularity, as well as trends in age at diagnosis. The dataset consists of patient records, including demographic and clinical variables. The goal is to validate whether sample data accurately represents the broader population.

**Key Metrics**:

- **Dataset Source**: Breast Cancer Gene Expression dataset

- **Variables of Interest**: Cancer type, cellularity, age at diagnosis

- **Dataset Size**: 693 patient records.

- **Timeframe**: Data collected from 2015–2023.

- **Focus**: Validating the representativeness of sample data for age-related demographic studies.

---

## 3. Project Goals

**Objective**:

1. Determine if there is a significant association between cancer type and cellularity.
2. Assess whether the sample mean age at diagnosis significantly differs from the population mean.

**Business Impact**:

- Ensure valid sampling for clinical studies.
- Improve early detection strategies by understanding age-related patterns.

---

## 4. Data Structure & Initial Checks

**Dataset**: `Breast Cancer Gene Expression.csv`

- **Columns Analyzed**:
  - `cancer_type_detailed`: Categorical variable indicating cancer subtype.
  - `cellularity`: Categorical variable indicating tumor cellularity.
  - `age_at_diagnosis`: Numerical variable representing patient age at diagnosis.
  - `patient_id` (integer): Unique patient identifier.
- **Data Quality**:
  - Population mean age: **61.09 years** (σ = 12.9787).
  - Sample mean age: **61.7 years** (σ = 15.33).
- **Data Cleaning**:
  - Missing values in `cancer_type_detailed` and `cellularity` were removed.
  - Summary statistics and distributions analyzed.

---

## 5. Executive Summary

**Key Findings**:

1. **Cancer Type and Cellularity Association**: Statistical testing suggests an association between the two variables.
2. **Age at Diagnosis**: No significant difference was found between sample and population mean age at diagnosis.
3. **Young Patient Representation**: Approximately 22.15% of patients were diagnosed below the age of 50.

---

## 6. Insights Deep Dive

### **Category 1: Cancer Type and Cellularity Association**

- **Chi-Square Test Results**:
  - **p-value**: `< 0.05`
  - **Conclusion**: Reject the null hypothesis, indicating a statistical association between cancer type and cellularity.

### **Category 2: Age at Diagnosis Trends**

- **Z-Test Results**:
  - **p-value**: `> 0.05`
  - **Conclusion**: No significant difference between sample and population mean age at diagnosis.
  - **Young Patients (<50 years)**: Represent 10% of the sample.
  - **Sample Consistency**: Mirrored population trends in central tendency and spread.  

---

## 7. Recommendations

1. **Further Subgroup Analysis**: Explore characteristics of younger patients for potential early intervention strategies.
2. **Expand Data Collection**: Gather additional data on genetic markers to refine insights.
3. **Validate Findings with Larger Samples**: Conduct additional studies to ensure findings generalize across broader demographics.

---

## 8. Technical Details

**Tools Used**:

- **Python Libraries**: `pandas`, `numpy`, `matplotlib`, `statsmodels`, `scipy.stats`, `pingouin`
- **Statistical Tests**:
  - Chi-Square Test for categorical associations
  - Z-Test for mean comparisons

---

## 9. Assumptions and Caveats

1. **Normality Assumption**: The age distribution was assumed to be approximately normal.
2. **Sampling Bias**: Selection biases may exist based on the dataset's regional and institutional sources.
3. **Data Exclusions**: Patients with missing values for key variables were removed, which could introduce minor bias.




