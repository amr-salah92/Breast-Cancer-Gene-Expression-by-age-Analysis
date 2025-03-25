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
**Company**: Breast Cancer Genomics Research Institute  
**Analysis**: Statistical Comparison of Population vs. Sample Mean Age at Diagnosis Using Z-Score  

---

## 2. Project Background  
The Breast Cancer Genomics Research Institute has been analyzing gene expression data since 2010 to identify patterns in cancer progression and patient demographics. The dataset includes clinical records of **693 breast cancer patients**, focusing on variables such as age at diagnosis, treatment history, and genetic markers.  

**Key Metrics**:  
- **Dataset Size**: 1,904 patient records.  
- **Timeframe**: Data collected from 2015–2023.  
- **Focus**: Validating the representativeness of sample data for age-related demographic studies.  

---

## 3. Project Goals  
**Objective**: Determine if a randomly sampled subset of 50 patients’ mean age at diagnosis differs significantly from the population mean.  
**Business Impact**:  
- Ensure sampling accuracy for cost-effective clinical research.  
- Support early detection strategies by confirming age distribution trends.  

---

## 4. Data Structure & Initial Checks  
**Dataset**: `Breast Cancer Gene Expression.csv`  
- **Columns Analyzed**:  
  - `patient_id` (integer): Unique patient identifier.  
  - `age_at_diagnosis` (float): Age in years at diagnosis.  
- **Data Quality**:  
  - No missing values in the analyzed columns.  
  - Population mean age: **61.09 years** (σ = 12.98).  
  - Sample mean age: **58.72 years** (σ = 13.91).  

---

## 5. Executive Summary  
**Key Findings**:  
1. **No Statistical Difference**: The sample mean age (58.72) aligns with the population mean (61.09) based on z-score analysis.  
2. **Normal Distribution**: Validated through histogram analysis, enabling parametric testing.  
3. **Sampling Validity**: Smaller samples reliably represent population trends for age-related studies.  

---

## 6. Insights Deep Dive  
### **Category 1: Hypothesis Testing**  
- **Z-Score**: **0.05218** (within ±1.96 critical range), indicating no significant difference.  
- **p-value**: **0.47918** (>0.05), failing to reject the null hypothesis.  

### **Category 2: Distribution Analysis**  
- **Population Skew**: 22.15 % of patients in the sample diagnosed before age 51.  
- **Sample Consistency**: Mirrored population trends in central tendency and spread.  

![age_at_diagnosis_histogram](https://github.com/user-attachments/assets/d0ff9902-40af-4073-93b7-143375af7c45)

---

## 7. Recommendations  
1. **Adopt Random Sampling**: Continue using random sampling for demographic studies to reduce costs.  
2. **Subgroup Analysis**: Investigate patients under 50 (22.15 % of the sample) for early intervention programs.  
3. **Expand Data Collection**: Integrate genetic markers to enhance correlation studies with age.  

---

## 8. Technical Details  
**Tools**:  
- **Python**: `pandas` (data manipulation), `scipy.stats` (norm), `matplotlib` (visualization).  
- **Jupyter Notebook**: Interactive analysis and reproducibility.  

---

## 9. Assumptions and Caveats  
1. **Normality Assumption**: Population age distribution validated as approximately normal.  
2. **Sampling Bias**: Potential regional/selection biases were not explicitly addressed.  
3. **Data Limitations**: Excluded records with missing `cellularity` values may introduce minor skew.  
 
