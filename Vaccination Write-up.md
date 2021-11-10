**Machine Learning Classification Project Write-Up**

Learning and Classifying Vaccine Hesitancy

**Abstract:**

 the World Health Organization reported vaccine hesitancy as one of the ten leading threats to global health. One-fifth of Americans report that they are hesitant against getting vaccinated or/and doubt vaccine safety. Thus, I looked at which individuals would be likely to hesitate against getting vaccines in this project. The project used the data, "the National 2009 H1N1 Flu Survey Data", which were collected in 2009 and 2010 to monitor influenza immunization coverage for random American households. I built different classification models and compared them to select a model that performed the best to predict the true positive cases (i.e., individuals who were vaccinated for H1N1). Random Forest outperformed the other models (i.e., Logistic Regression, Naive Bayes, and XGBoost) in the project. With the validation dataset, the score on recall was 0.745. With the holdout (test) dataset, the recall score was 0.701. Future studies can perform more advanced feature engineering, such as testing on a different set of features, and test other possible emsembling models. 



**Design**

Vaccination is the most effective way to prevent infectious diseases. Infectious diseases can be prevented by providing vaccines and creating sufficient community immunization. While a large portion of people believe that vaccines could protect them from contagious diseases, however, there have been controversies on vaccine safety for a long time. One-fifth of Americans report that they are hesitant against getting vaccinated or/and doubt about vaccine safety. the World Health Organization reported vaccine hesitancy as one of the ten leading threats to global health. Thus, I looked at which individuals would be likely to hesitate against getting vaccines in this project.

This prediction can be useful when advertising vaccines to those who are hesitant against getting a vaccine or planning out alternatives for those with vaccine hesitancy to reduce the spread of infectious diseases. I predicted how likely people received H1N1 vaccines during the pandemic in 2009 using different binary classification models.

**Data:**

This project originated from the DrivenData competition, "Flu Shot Learning: Predict H1N1 and Seasonal Flu Vaccine". The project used the data, "the National 2009 H1N1 Flu Survey Data", which were collected in 2009 and 2010 to monitor influenza immunization coverage for random American households, when a pandemic caused by the H1N1 influenza virus (i.e., swine flue) in 2009. The dataset has 26707 rows and includes the target variable (whether individuals got h1n1_vaccine) and a total of 34 features (e.g., face mask behavior, frequent hand wash, education level, age, etc). 

**Algorithms:**

I built different classification models and compared them to select a model that performed the best to predict the true positive cases (i.e., individuals who were vaccinated for H1N1).

A. Feature Engineering 

1. Treating categorical variables (dummy variables and ordinal variables)
2. Combining duplicating values in features
3. Feature selection using feature importance
4. Class imbalance using SMOTE (the negative cases (78%) were about four times larger than the positive cases)
5. Tuning hyperparameter with GridCV for logistic regression, random forest, and XGBoost 

B. Models

The dataset was split into 60/20/20 (train, validation, test). The following models were compared for scores to see which model performed the best: Logistic regression, Naive Bayes, Random Forest with GridCV, and XGBoost with GridCV. The evaluation metrics I used in the project was recall to predict true positive the best by penalizing false negatives. Random Forest outperformed the other models (i.e., Logistic Regression, Naive Bayes, and XGBoost) in the project. With the validation dataset, the score on recall was 0.745. With the holdout (test) dataset, the recall score was 0.701.



**Tools**: 

The main tools I used in the project were the necessary python packages for classification models (i.e., sklearn). Specifically, the following sklearn packages were used: cross-validation, train test split, linear regression, random forest, XGBoost, and Naive Bayes. The other supplementary python packages used were imblearn for the data imbalance and Numpy and Pandas for data manipulation. For visualization, I used seaborn and matplotlib.



**Communication:**

This project was delivered in a PowerPoint presentation. More details were embedded on my personal Github page. 