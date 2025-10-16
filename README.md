Fake News Detection


This project aims to build a machine learning model to detect fake news. The dataset used contains news articles with labels indicating whether they are real or fake.

Dataset


The dataset contains the following columns:


id: unique id for a news article

title: the title of a news article

author: author of the news article

text: the text of the article; could be incomplete

label: a label that marks whether the news article is real or fake (1: Fake news, 0: Real News)

Data Preprocessing


Loading the dataset: The dataset was loaded into a pandas DataFrame.

Handling Missing Values: Missing values in the 'title', 'author', and 'text' columns were replaced with empty strings.

Merging Author and Title: The 'author' and 'title' columns were merged into a new column called 'content'.

Stemming: The 'content' column was processed using stemming to reduce words to their root form and remove stopwords.

Vectorization: The textual data in the 'content' column was converted into numerical data using TfidfVectorizer.

Splitting the dataset: The dataset was split into training and testing sets.

Model Training and Evaluation


Several classification models were trained and evaluated on the dataset:

Logistic Regression: Achieved a test accuracy of 0.979. Hyperparameter tuning using GridSearchCV improved the test accuracy to 0.979.

Random Forest Classifier: Achieved a test accuracy of 0.993. Hyperparameter tuning using GridSearchCV resulted in the following best parameters and a test accuracy of 0.995.

KNeighbors Classifier: Achieved a test accuracy of 0.523. Hyperparameter tuning using GridSearchCV resulted in the following best parameters and a test accuracy of 0.541.

Gaussian Naive Bayes: Achieved a test accuracy of 0.803.

Support Vector Classifier (SVC): Achieved a test accuracy of 0.991. Hyperparameter tuning using GridSearchCV resulted in the following best parameters and a test accuracy of 0.994.

The best performing model based on test accuracy was the RandomForestClassifier.
