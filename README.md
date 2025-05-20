# Mental Health
## Business Goal
Mental health plays a fundamental role in both individual well-being and societal stability. Poor mental health can negatively affect quality of life, job performance, and relationships with family, friends, and the broader community. Mental health disorders are highly prevalent, impacting hundreds of millions of people every year and many more at some point in their lives.
The goal of this analysis is to develop predictive models capable of identifying mental health conditions based on various medical and demographic features. Understanding the factors associated with mental illness is essential for researchers and healthcare professionals, as it enables better diagnosis, prevention, and treatment.
The dataset used in this analysis includes valuable information about individuals, such as age, gender, occupation, country of residence, mental health condition and severity, consultation history, stress levels, sleep hours, work hours, and physical activity.

## Data
The mental health dataset, sourced from Kaggle, includes eleven baseline variables, both numerical and categorical. The target column indicates whether or not the individual has a mental health condition. The data is balanced.


## Modeling and Performance
In this project, we evaluated various classification models to predict mental health conditions using the Kaggle dataset. The models tested were:

* Logistic Regression
* Random Forest
* XGBoost

Each model was trained and tested using a train/test data split, followed by cross-validation. Polynomial Features was used for Logistic Regression. Performance was optimized using GridSearchCV and parameter tuning in Random Forest.
Among all models, Logistic Regression delivered the best performance with the least overfitting. The results were as follows:

* Accuracy: 53%
* Recall: 70%

This means the model correctly identifies mental health conditions in 70% of relevant cases and has an overall accuracy of 53%. Although the accuracy is not high, the model is useful for identifying individuals who do in fact present a mental health condition, which is especially relevant in public health contexts.

## Conclusions
The model revealed a significant relationship between certain features and the target variable (mental health condition). Specifically:
Countries such as Australia and Germany showed lower coefficients, suggesting fewer cases of mental health issues.

In contrast, the United States and Canada showed higher coefficients, indicating a higher incidence of mental health conditions in those populations.

After country, the features most strongly associated with increased mental health risk were:

Medium stress levels

Working more than 45 hours per week

These findings offer valuable and actionable insights for improving mental health outcomes.
Additionally, by generating SHAP plots to interpret the model, we observed that female patients show a higher incidence of mental health conditions compared to male patients.

## Next Step and Recommendations
The model does not yet offer a strong representation of the data. If this were a model to be used in a healthcare center, it might not justify the allocation of resources given that it only correctly identifies 53% of those in need. Therefore, it is recommended to continue exploring additional datasets that either complement the current variables or introduce new ones associated with the development of mental health conditions. This could provide more comprehensive information for building effective action plans. Nonetheless, the current model reveals important relationships that can guide future research and intervention strategies.

## Actionable Insights
* Personalized Care:
 Develop individualized treatment plans that take the patient's gender into account to optimize care and effectively manage mental health conditions.

* Stress Management Education and Tools:
 Provide patients with educational resources and tools to manage stress, such as breathing techniques, support groups, and access to counseling services.

* Awareness of Work-Life Balance:
 Raise awareness about the negative impact of long working hours on mental health. Promote a healthy balance between work, leisure, and rest.
