# Spotify Review Sentiment Analysis

**Dataset:**

This project uses web-scraped Google Play Store reviews regarding the Spotify app. The reviews are from Jan 1st to Jul 7th of 2022. The dataset and its attribute information can be found at: https://www.kaggle.com/datasets/mfaaris/spotify-app-reviews-2022

<br>

**Project Objectives:**

(1) Apply text pre-processing techniques and perform exploratory data analysis (EDA) to understand the data in depth

(2) Perform entity-based sentiment analysis (SA) to classify users' app review ratings (1-5 stars) as positive, neutral, or negative. Binary and multi-class classification are explored, where the ratings are categorized as follows:

* Binary classification: positive (4 stars or above), negative (3 stars or below)
* Multi-class classification: positive (4 stars or above), neutral (3 stars), negative (2 stars or below)

<br>

**Results:**

(1) EDA: Unsurprisingly, over 90% of the reviews are subjective, where users have expressed some degree of personal feeling. In addition, subjectivity score and review length have a weak correlation with rating. The higher the subjectivity score, the higher the rating and the longer the review, the lower the rating

(2) EDA: April appears to be a pivotal month. While it has the highest percentage of negative reviews, the following months, May and June, have more positive reviews than neutral and negative reviews combined. There was a day in March and a week in April in which Spotify encountered technical problems and updated its app in which users reported access issues and bugs respectively. These complications contributed to the large spikes in negative reviews around their respective times

(3) SA: For multi-class classification, where the reviews are categorized as positive, neutral, or negative, Kaggle users reported accuracies in the 70s. I was in this ballpark, using Naive Bayes and LightGBM reached an accuracy of 79% and 80% respectively. Other performance metrics, such as recall, precision, and f1 score were in the mentioned range as well. However, both algorithms did not predict neutral reviews well because it was the class with the fewest observations. This led to me to take a binary classification approach, labeling reviews as either positive or negative

(4) SA: For binary classification, I introduced Logistic Regression in addition to Naive Bayes and LightGBM. Logistic Regression reached an accuracy of 87%. Both Naive Bayes and LightGBM underperformed, but experienced a 6% accuracy increase. The former reached an accuracy of 85% while the latter reached 86%. All three algorithms predicted positive and negative reviews well. It is evident that approaching this project as a binary classification problem resulted in better model performance

<br>

**Opportunities:**

(1) Perform aspect-based sentiment analysis to understand what users specifically like and dislike about the app. This can be done by identifying aspects, such as music selection and ads, and or leveraging other techniques such as topic modeling
