
<p align="center"><img width="100%" src="Employee Attrition And Performance Analysis 5555.png" /></p>

--------------------------------------------------------------------------------

## Problem Statement:

Human Resources are critical resources of any organization. Organizations spend huge amount of time and money to hire and nurture their employees. It is a huge loss for companies if employees leave, especially the key resources. Reasons for attrition can be plenty and range from dissatisfaction due to low salaries, less or no career growth opportunities, inferior employee supervision, eagerness to get into companies with global presence, lack of recognition, lack of freedom of expression in the organization and underutilization of talents and skills of the individuals. Thus in a situation when more and more employees are quitting the organization, the attrition rate is on a rise. So if HR can predict weather employees are at risk for leaving the company, it will allow them to identify the attrition risks and help understand and provide necessary support to retain those employees or do preventive hiring to minimize the impact to the organization.

## Objective:
The Objective Of This Project Is To Develop Analytics And Report Using Data Science Tool To Provide Detailed Insights On HR Analytics Focusing On Employee Attrition And Performances.

**Hypothesis:** 
1. To Understand And Analyze Factors That Lead To Employee Attrition.
2. To Analyze Factors Affecting Employee Performance And Means To Optimize The Same. 

## Random Forest Classifier using Scikit-learn
Random forest is a supervised learning algorithm. It has two variations – one is used for classification problems and other is used for regression problems. It is one of the most flexible and easy to use algorithm. It creates decision trees on the given data samples, gets prediction from each tree and selects the best solution by means of voting. It is also a pretty good indicator of feature importance.
Random forest algorithm combines multiple decision-trees, resulting in a forest of trees, hence the name Random Forest. In the random forest classifier, the higher the number of trees in the forest results in higher accuracy.
By using grid search best parameters was found to be –
RandomForestClassifier(criterion='entropy', n_estimators=10, random_state=0)
The major hurdle was we had 1223 unlabeled (No in Attrition) and 237 labelled (Yes in Attrition), which is a highly imbalanced data. So I used stratified sampling based on proportion of attrition in overall data.
* Decision Tree Modeling: I have used Decision tree to create model. The major hurdle was we had 1223 unlabelled (No in Attrition) and 237 labelled (Yes in Attrition), which is a highly imbalanced data. So I used stratified sampling based on proportion of attrition in overall data.

* Model Evaluation: I have used the k fold cross validation technique for assessing how the results of a model will generalize to an independent test data set.  I used k =5 i.e.. 5 fold cross validation. Model was fit on the stratified sample data and tested on unmarked dataset.

* ROC Curve: The ROC curve is a simple plot that shows the trade-off between the true positive rate and the false positive rate of a classifier for various choices of the probability threshold. ROC area = 0.6128 and F1 = 0.81

## Suggested Action
It’s not sensible to focus on every employee who wants to leave because it costs time and energy for human resources management department. HR department need to focus on:
* Improving the work conditions
Provide an option for the employee’s to work from home, on a flexible schedule, or in an office with an ergonomic workspace, they will be more satisfied with their work and more likely to achieve a healthy work-life balance.
* Offer modest salaries and perks
To maintain the critical employee’s company need’s to offer equitable and modest salaries. You can also give added perks like flexible schedules, travel discounts etc.
* Employee Engagement
When you have talented employee’s we need to find ways that you can help expand the employee’s skill set, so that their involvement in the job increases. If their involvement is low, they will get bored and think that they are not growing within the organization



## Repository Contains
 - Data Folder -- Contains Raw Data Files (Data can be downloaded from [kaggle](https://www.kaggle.com/pavansubhasht/ibm-hr-analytics-attrition-dataset))
