# CMPE255_Bonuswork2

# Bonus Work 2
## Tech stack
- - - 1.Python
- - - 2.HTML 
- - - 3.Flask Framework
- - - 5.Models(Gaussian NB-wow , Gaussian NB - TFIDF , TensorFlow - LSTM)

## Summary
- - - 1.Create the classification model for predicting tweet sentiment ([ colab link - ])
- - - 2.Flask framework is used for UI integration with the developed model.
- - - 3.Once the search button is hit in UI, it actually gets matched tweets in real time from the twitter using tweepy API and then classifies the sentiment.

# Description

## Abstract
This project is all about how to collect data from Twitter using the Twitter API in real time, and then use a 
model to predict the sentiment of a tweet. It also describes pre-processing that is involved in this process,
and how to create a user interface to interact with the model.

## Fetching tweets from twitter in real time
### Twitter API
I used Tweepy to access the data from Twitter. Twitter provides us with developer accounts that allow access to its data
through its API services, provided you have the proper access levels.

### Cleaning the data
Data has been checked and modified to make the tweets free from the unwanted characters which are not alphabets or 
any special characyers like @$...

### Lemmatization
Lemmatization links words with similar meanings to one word. It groups together different synonymous or inflected 
words so they can be considered as a single word.

### Bag of words and TF-IDF
The bag-of-words model is a way of representing text data that is easy to use and can be successful when trying to model text with 
machine learning algorithms. Also used TF-IDF as it is proven to provide better results compared to BOW.

## Modeling the data
### GaussianNB
Naive Bayes is a probabilistic model that is based on Bayes theorem. This theorem provides a conditional probability of 
an event A, happening given another event, B, has previously happened. In this case, the predictor values are assumed to
follow a Gaussian distribution.

The model was trained with both the bag of words and tf-idf approaches, as the stop words might not have been completely 
removed in the bag of words approach and in tf-idf, which removes the unwanted words which makes the model train with 
more relevant data.

### XGBoost
XGBoost is an open-source implementation of the gradient boosted trees algorithm, which is a supervised learning algorithm that uses the estimates of a set of simpler models to predict a target variable.

## Downloading the model
The model which has been trained in the previous step has been stored and downloaded from colab so that it
can be used with flask and integrated to a UI (web application)

## Flask Framework
Flask is a Python micro web framework that is used to create dynamic user interfaces. The model from the colab has been 
imported to the flask project structure and has been integrated using the following code. The home.py file has the code to
call the model with the tweet data which has been gathered from the get-related-tweets method which returns the relevant 
tweets from the twitter in real time as twitter would return if we search in the twitter search box. This data is then 
pre processed before being sent to the model for prediction. A virtual environment has been created with name twitter and
installed all the necessary packages required for the running of the application. The templates folder contains the code
for HTML which basically displays the user screens. The folder structure is as shown below.

## Comparision of models using bar chart


## UI Screens:
![alt](https://github.com/iswarya1223/CMPE255_Bonuswork2/blob/main/after%20keyword%20search.png)


