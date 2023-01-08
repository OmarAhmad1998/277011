# Team Members


Omar Almohammad Ali 277011
Nadeer Salem 274491

# Credit Score Classification

# Introduction
The greatest financial company in the world has collected bank details and credit-related information from all over the globe. My task was to design a data-driven solution to reduce the manual burden and divide the users into three credit score brackets: Poor, Standard, and Good. My solution aimed to help the company develop targeted products for each group.

# Methods
The main goal of this project was to design a data-driven solution to divide users into three credit score brackets: Poor, Standard and Good. To achieve this goal, we used various machine learning algorithms and feature selection techniques.

First, we performed an explanatory data analysis (EDA) to get a better understanding of the dataset. We extracted information about the dataset, looked at the unique values of each categorical variable, and checked for missing values. We then cleaned up the dataset by imputing missing values and preprocessing the categorical variables using label encoding.

Next, we generated train, test, and validation sets using a train-test split method, with the train set comprising 75% of the data and the test and validation sets each comprising 12.5% of the data. We also scaled the data using the StandardScaler method.

For feature selection, we used the Recursive Feature Elimination (RFE) method to select the most important features. We then used the SelectFromModel method to further eliminate features based on their importance.

As for the machine learning algorithms, we used three different classifiers: Random Forest Classifier, MPL Classifier, and AdaBoost. We trained and tested the models on the preprocessed data and compared their performance using the accuracy metric.

Finally, we tried removing variables to see if it would improve the performance of the models. We found that removing variables slightly improved the performance of the Random Forest Classifier and slightly decreased the performance of the MPL Classifier and AdaBoost.

In terms of the environment, we used the following libraries: pandas, numpy, matplotlib, seaborn, and scikit-learn. We recommend using the conda package manager to install these libraries. The specific versions of the libraries can be found in the conda list file provided in the project repository.

Overall, we believe that the combination of feature selection and different machine learning algorithms helped us achieve our goal of accurately dividing users into credit score brackets. However, it is worth noting that further improvements could be made by experimenting with different feature selection techniques and using more advanced machine learning algorithms.

# Experimental Design
To achieve this goal, We first conducted exploratory data analysis (EDA) on the dataset to understand the structure of the data and identify any missing values or inconsistencies. We then cleaned and preprocessed the data, including imputing missing values and encoding categorical variables.

Next, We split the data into train, test, and validation sets and trained three different classifiers: a Random Forest Classifier, a Multi-Layer Perceptron (MPL) Classifier, and an AdaBoost Classifier. Weused the train and validation sets to fit the models and the test set to evaluate their performance.

We also applied feature selection techniques to see if removing certain variables would improve the performance of the models. We tried two methods: Principal Component Analysis (PCA) and removing variables with high correlation.

# Results
The results of the classification models are summarized in the table below:

|                 Model                | Accuracy |
|:------------------------------------:|----------|
| Random Forest Classifier (before)    | 0.89     |
| MPL Classifier (before)              | 0.84     |
| AdaBoost (before)                    | 0.85     |
| Random Forest Classifier (after PCA) | 0.90     |
| MPL Classifier (after PCA)           | 0.82     |
| AdaBoost (after PCA)                 | 0.85     |

We can see that applying feature selection methods improved the performance of the Random Forest and MPL classifiers, but had little effect on the AdaBoost classifier. In particular, using the correlation method increased the accuracy of the Random Forest classifier by 0.02 and the MPL classifier by 0.01.

# Conclusion
In conclusion, using data-driven approaches and feature selection techniques can be effective in improving the performance of classification models for credit score prediction. However, the specific technique that works best may depend on the specific model and dataset being used. Further experimentation and evaluation may be necessary to determine the optimal approach in a given situation.

There are several questions that may not be fully answered by our work. One potential question is the extent to which the features we selected truly represent the most important factors in predicting credit score. It is possible that there are other factors that are more influential in determining credit score, but we did not include them in our analysis. Additionally, our model may not be able to accurately predict credit score for certain individuals or groups, such as those with very high or very low annual incomes.

There are several natural next steps for this direction of future work. One potential next step would be to expand the dataset to include a wider range of individuals and potentially incorporate additional features that could provide more insight into the credit scoring process. Additionally, it may be useful to investigate different machine learning algorithms and compare their performance on the dataset in order to identify the most effective approach. Finally, it may be worthwhile to explore methods for improving the interpretability of the model, such as using feature importance measures or implementing techniques like local interpretable model-agnostic explanations (LIME).
