# Model Card

Last updated: April 2024


## Model Details

This model was developed to classify patients into categories reflecting their healthcare needs (e.g., 0-1 doctors, 2-3 doctors, 4 or more doctors) so that we can predidct the number of doctors visits.

### Model date

April 2024

### Model type

RandomForest Classifier

### Model version

1.0

### Developer: 

Mijin Cho

### Model Implementation Code

[Jupyter NoteBook](https://github.com/mijinatdiscovery/NPHA-doctor-visits/blob/main/notebooks/Model%2BAnalysis.ipynb)

### Paper or other resource for more information

[National Poll on Healthy Aging (NPHA)](https://www.icpsr.umich.edu/web/NACDA/studies/37305/versions/V1)

## Intended Uses:

### Primary intended uses

The primary intended users of this model is AI practitioners for learning purposes.


### Secondary uses

Here are some secondary use cases we imagine are likely:
Health and Medicine: Healthcare providers, medical staff planners, and healthcare policy makers.


## Evaluation Data and Metrics

### Datasets

This model was trained on a subset of [the National Poll on Healthy Aging (NPHA) dataset](https://archive.ics.uci.edu/dataset/936/national+poll+on+healthy+aging+(npha)), consisting of 714 records of seniors who responded to the NPHA survey. The features include 14 attributes related to health and sleep. There is information about race/ethnicity, gender, and age.

We removed all survey respondents with missing responses for any of the chosen features.


### Motivation

The National Poll on Healthy Aging dataset was created to gather insights on the health, healthcare, and health policy issues affecting Americans aged 50 and older. By focusing on the perspectives of older adults and their caregivers, the University of Michigan aimed to inform the public, healthcare providers, policymakers, and advocates about the various aspects of aging. This includes topics like health insurance, household composition, sleep issues, dental care, prescription medications, and caregiving, thereby providing a comprehensive understanding of the health-related needs and concerns of the older population.

### Evaluation Data

The model was evaluated on a separate test set extracted from the same distribution as the training data.

###  Evaluation results

                         precision  recall   f1-score   

                  1         0.22      0.18      0.20       
                  2         0.53      0.51      0.52        
                  3         0.33      0.39      0.36        
     train accuracy                             0.64
      test accuracy                             0.41

### Ethical Considerations

Fairness and Bias: Initial tests indicate potential bias in accurately classifying classes with fewer samples. Further bias auditing and fairness assessments are recommended.

Privacy: This model was trained on anonymized patient data. Care should be taken to ensure that all data used with this model complies with local privacy laws and regulations.

### Caveats and Recommendations

The model currently shows signs of overfitting with significant discrepancies between training and test performance. It should not be used for critical healthcare decisions. It's essential to improve the model's precision and recall across all classes to make it a reliable tool. 

Collecting more data and enhancing feature engineering are crucial steps in improving model performance. More data provides the model with a diverse set of examples, reducing overfitting and improving generalization. Enhanced feature engineering helps in creating better features and incorporating relevant data, leading to improved accuracy and capturing hidden patterns in the data.