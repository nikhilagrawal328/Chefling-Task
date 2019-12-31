# Chefling-Task
Predict the tags associated with a recipe
## Approach to solve the problem

* The required dataset that is provided is highly uncleaned and unbalanced.
* So the first step is to clean and preprocess the data. As in the dataset some columns have missing values so I drop them as they are few in number but some have lot of missing values or list like prep_time,cuisine and cooking time so for them I introduce new value and fill all those null values with the introduced value.
* After getting the cleaned text I perfrom some data analysis on the tags try to identify which are the most favored tags, how many tags are there, build a wordcloud etc.
* As there are total 776 tags and predicting all of them is a computation heavy task because it is a multi label classification problem so to deal with these problem I have taken the top 200 tags which covers about 99.4% of the recipes that we have.
* In this problem I have used Average W2V technique for text(recipe) vectorization. We can also used tf-idf W2V, tf-idf and many other but for simplicity I have used only one.
* After getting all the data in required format I perform 80:20 train test split and perform modelling with OneVsRest classifier with Logistic Regression and SVM as it is a multi label classification problem.
