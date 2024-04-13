# NPHA Model Card for RandomForest Classifier

Last updated: April 2024


## Model Details



### Model date

April 2024

### Model type

RandomForest Classifier

### Model version

1.0

### Developer: 

Mijin Cho

### Model Implementation Code: 

[github](https://github.com/mijinatdiscovery/NPHA-doctor-visits/blob/main/notebooks/NPHA-doctor-visits.ipynb)

### Paper or other resource for more information

[paper](https://www.icpsr.umich.edu/web/NACDA/studies/37305/versions/V1)


### Primary intended uses

This model is intended to classify patients into three categories based on the number of doctors they have visited: 0-1 doctors, 2-3 doctors, and 4 or more doctors.

### Intended Users

Healthcare providers, medical staff planners, and healthcare policy makers.


### Out-of-scope use cases



## Evaluation Data and Metrics
### Datasets

### Datasets

This model was trained on a subset of [the National Poll on Healthy Aging (NPHA) dataset](https://archive.ics.uci.edu/dataset/936/national+poll+on+healthy+aging+(npha)), consisting of 714 records of seniors who responded to the NPHA survey. The features include 14 attributes related to health and sleep. There is information about race/ethnicity, gender, and age.

We removed all survey respondents with missing responses for any of the chosen features.


### Motivation

The National Poll on Healthy Aging dataset was created to gather insights on the health, healthcare, and health policy issues affecting Americans aged 50 and older. By focusing on the perspectives of older adults and their caregivers, the University of Michigan aimed to inform the public, healthcare providers, policymakers, and advocates about the various aspects of aging. This includes topics like health insurance, household composition, sleep issues, dental care, prescription medications, and caregiving, thereby providing a comprehensive understanding of the health-related needs and concerns of the older population.

### Ethical Considerations

Fairness and Bias: Initial tests indicate potential bias in accurately classifying classes with fewer samples. Further bias auditing and fairness assessments are recommended.

Privacy: This model was trained on anonymized patient data. Care should be taken to ensure that all data used with this model complies with local privacy laws and regulations.

### Caveats and Recommendations

## Model Performance

The model currently shows signs of overfitting with significant discrepancies between training and test performance. It should not be used for critical healthcare decisions.

## Improvement Recommendations
