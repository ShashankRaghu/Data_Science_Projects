# Telecom Churn Project
## The aim of this project is to build a model which can predict wheather a custmoer will churn(leave the netwrok). The dataset conatins information about a customers cellular transactions for the months June(6) to September(9). We need to predict of the customer will churn in September using the data from month 6 to 8.

* ### The dataset can be download from [this link](https://drive.google.com/file/d/1SWnADIda31mVFevFcfkGtcgBHTKKI94J/view).
* ### We have performed the following preprocessing steps:
  * ### Removing columns which have only one unique value.
  * ### For handling the missing values we found out that the missing values were MNAR(Missing not at random). We saw that the columns were missing when customers haven't used the service, hence we replaced these columns with zero.
  * ### Since there is a large number of customers, we want to focus on only the high value customer. So we sepearted the dataset with the top 30 percentile spenders in month 6 and 7.
* ### We calculated dependent variable "churn" by looking at total expenditure of customers in month 9, and those customers who spent 0 amount were tagged as churned.
* ### For EDA we have looked at the histograms, boxplots, barplots and heatmap. Below is the heatmap showing the correlation co-efficients.
![TelecomChurnGit](https://user-images.githubusercontent.com/77088516/125994623-84991dfb-f8c2-4ce2-bb85-f560e0deeb32.PNG)
* ### We performed some manual feature engineering and PCA to reduce the data to 60 columns.
* ### The skewness in the data is handles by PowerTransformation, and the data imbalance is handled by class weights. 
* ### For the model building we used StrifiedKFold for validation testing, and GridSearchCV for finding the best parameter. XGBoost, RandomForestClassifier and Logistic Regression models were tried.
* ### The Logistic Regression was the best model, with an accuracy of ~83.5%.
* ### We have also built Logistic Regression and Decision Tree models with non PCA data, in order to find the top predictors in the dataset.
