# ofsted-inspection-prediction
# Predicting Ofsted Inspection Grades Using School Performance, Demographic, and Prior Inspection Data

## Summary

This project investigated whether publicly available data could be used to predict Ofsted inspection grades for secondary schools in England. The aim was to evaluate how factors like academic performance, pupil demographics, and previous inspection outcomes correlate with Ofsted ratings.

Three datasets were merged:
- Latest Ofsted inspection outcomes
- School-level performance data (e.g. Attainment 8, Progress 8)
- School characteristics (e.g. % SEN, FSM, EAL)

Several machine learning models were trained and evaluated using accuracy, precision, recall, and weighted F1-score. The best model (LightGBM) achieved:
- **74% accuracy**
- **73% weighted F1-score**

The model performed best when predicting schools rated 'Good'. It struggled with identifying schools rated 'Inadequate', limiting its practical use in early-warning systems or accountability.

## Key Predictive Features

- Prior inspection subgrades (leadership, overall effectiveness)
- GCSE Attainment 8 scores
- Average prior attainment
- % of pupils with special educational needs

## Limitations

- Weak prediction of ‘Inadequate’ schools
- Not suitable for real-world deployment without refinement

## Recommendations

- Explore **ordinal classification models** that respect the order of grades
- Use **contextual and qualitative data** such as governance, staff turnover, and Ofsted report sentiment
- Apply other techniques to handle class imbalance more robustly

## Project Files

- 2 Jupyter notebooks (logistic regression, tree-based models)
  
## 📁 Data Sources

The following publicly available datasets were used for this project:

1. **Ofsted Inspection Outcomes (as of March 2025)**  
   - Contains school-level inspection results and subdomain scores.  
   https://www.gov.uk/csv-preview/680117c990dd6a0497e28815/Management_information_-_state-funded_schools_-_latest_inspections_-_as_at_31_Mar_2025.csv

2. **School Performance Tables (Key Stage 4)**  
   - Includes academic performance indicators such as Attainment 8, Progress 8, and EBacc statistics.  
https://explore-education-statistics.service.gov.uk/data-catalogue?publicationId=c8756008-ed50-4632-9b96-01b5ca002a43&releaseVersionId=b76a938a-7875-4542-af20-0b23ecb99a49&themeId=74648781-85a9-4233-8be3-fe6f137165f4

3. **School Characteristics Dataset**  
   - Provides pupil demographic data: % SEN, % FSM, EAL, IDACI index, etc.  
https://explore-education-statistics.service.gov.uk/data-catalogue?publicationId=c8756008-ed50-4632-9b96-01b5ca002a43&releaseVersionId=b76a938a-7875-4542-af20-0b23ecb99a49&themeId=74648781-85a9-4233-8be3-fe6f137165f4

📝 **Note**: These are the **original raw datasets**. All data cleaning, merging, and feature engineering are done within the Jupyter notebooks in this repository.


---

**Note:** This project is intended for research and learning purposes. 
