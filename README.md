# Email-SMS-spam_classifier
## Overview 
The Email Spam Classifier is a machine learning project designed to classify emails as spam or not spam.
This project leverages various machine learning algorithms to analyze and predict the spam status of emails based on their content.

## 1.Data Cleaning
I have done some basic level datacleaning like,firstly i drop the irrelevant columns.Then i label our output through encoding  like spam(1),Not spam(0).

## 2.Exploratory Data Analysis(EDA)
I do EDA on the dataset to understand the distribution of the datalike the data is highly imbalanced, with a higher proportion of ham messages compared to spam. Visualization using a pie chart illustrates this imbalance clearly.

- I did some feature engineering in order to having a better understand towards the dataset.i create 3 more columns num_characters,num_words,num_sentences and trying to find descriptive statistics on themin both spam as well as ham  target values.
- Spam messages tend to be longer and contain more words and sentences on average compared to ham messages.
- Pairplots and heatmaps help visualize the relationships and correlations between these features, giving us insights into the data patterns.

## 3. Data Preprocessing

To prepare the text data for model building, we perform several preprocessing steps by using nltk library:
- **Lowercasing**: Converting all text to lowercase to maintain consistency.
- **Tokenization**: Splitting the text into individual words.
- **Removing Special Characters**: Keeping only alphanumeric characters.
- **Removing Stop Words and Punctuation**: Filtering out common but non-informative words.
- **Stemming**: Reducing words to their root forms.

Using the transformed text, we create new columns in the dataset that reflect these changes.

## 4.Data Visualization
- Visualize common words in spam and ham messages using word clouds and bar plots. These visuals help identify key terms for feature selection.

## 5.Model Evaluation

- We implemented and evaluated three Naive Bayes models using TF-IDF features to classify emails:

- **Gaussian Naive Bayes**: This model achieved an accuracy of 86.94%. However, it struggled with precision in detecting spam, making it less reliable for this task.

- **Multinomial Naive Bayes**: Outperformed the others with an impressive accuracy of 97.10% and perfect precision in spam detection, making it the most effective model in our evaluation.

- **Bernoulli Naive Bayes**: Also performed well, with an accuracy of 96.95%, but slightly behind the Multinomial variant.


- **Conclusion**: The Multinomial Naive Bayes model stands out as the most accurate and precise, making it our top choice for deployment.


## 6. Model Improvement and Hyperparameter Tuning

To further enhance our model's performance, we can:
- **Optimize Hyperparameters**: Using techniques like GridSearchCV to find the best parameters for our model.
- **Feature Selection**: Experimenting with different features and n-grams to improve model accuracy.
- **Balancing the Dataset**: Employing techniques like SMOTE to address the data imbalance.

