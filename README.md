# Spotify Review Sentiment Analysis

**Dataset:**

This project uses web-scraped Google Play Store reviews regarding the Spotify app. The reviews are from Jan 1st to Jul 7th of 2022. The dataset and its attribute information can be found at: https://www.kaggle.com/datasets/mfaaris/spotify-app-reviews-2022


**Project Objectives:**

(1) Apply text pre-processing techniques and perform exploratory data analysis (EDA) to gain a better understanding of the data

(2) Perform entity-based sentiment analysis (SA) to categorize users opinions towards the app


**Results:**

(1) EDA: There was a day in March and a week in April in which Spotify encountered technical problems and updated its app in which users reported access issues and bugs respectively. These contributed to the large spikes in negative reviews around their respective times

(2) SA: For multi-classification, where the reviews are categorized as positive, neutral, or negative, Kaggle users reported accuracies in the 70s. I was in this ballpark, using Naive Bayes and LightGBM reached an accuracy of 79 and 80% respectively. Other performance metrics, such as recall, precision, and f1 score were in the mentioned range as well. However, both algorithms did not predict neutral reviews well because it was the class with the fewest observations. This led to me to take a binary classification approach, categorizing reviews as either positive or negative

(3) SA: For binary classification, I introduced Logistic Regression in addition to Naive Bayes and LightGBM. Logistic Regression reached an accuracy of 87%. Compared to Logistic Regression and focusing soley on accuracy, Naive Bayes and LightGBM underperformed, but experienced a 6% increase. Naive Bayes reached an accuracy of 85% while LightGMB reached 86%. All three algorithms predicted the two classes well. In short, it is evident that approaching this project as a binary classification problem resulted in better model performance


**Opportunities:**

(1) Perform aspect-based sentiment analysis to understand what users specifically like and dislike about the app. This can be done by identify aspects, such as music selection, ads, etc. and or leveraging techniques such as topic modeling