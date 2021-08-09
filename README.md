# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP

### Executive Summary

Some of the most popular subreddits of all time relate to video game discussions particularly discussions around popular new releases as well as promotion of the works of independent game developers. This project explores using natural language processing to identify whether a gaming discussion involves general video game discussion or discussions about indie releases.

The 'Games' subreddit is a forum where users discuss their interests in popular, typically AAA games, discuss and review new titles, and can view game trailers.

The 'IndieGaming' subreddit is a forum where users discuss progress on games they are working on, gather support and suggestions for concept art, or are seeking advice for certain tools and software used in game development.

This project compares results of different classification models: Random Forest Classifier, Support Vector Mechines, Logistic Regression, and K Nearest Neighbors.

Comparing the accuracy scores from the four models indicate that all models produce high variance, low bias results as all models show higher training scores than test scores. Comparing to the baseline score of 50%, each of the models performed well above this score. 

RandomForest and SVM were shown to provide better scores to sort through the Games and IndieGaming subreddit types using a CountVectorizer to tokenize text. RandomForestClassifier did provide the best accuracy on the training data with a score of 91.7% on the larger dataset and 99.7% on the smaller dataset. SVM also provided scores over 90% for both dataset sizes but provided worse overfitting than RandomForestClassifier.

Even though logistic reggression did not provide the highest training score, it did provide the smallest variance of around 5% between a training score of 83.8% and test score of 78.8% on the larger dataset.

KNN performed worse overall on accuracy and overfitting.

#### Contents

Data Collection and Cleaning: 
IndieGaming Subreddit - part1a_reddit_datacollect_indiegaming.ipynb
Games Subreddit - part1b_reddit_datacollect_games.ipynb

Models and Conclusions:
part2_reddit_model.ipynb

#### About the API

Data was collected using Pushshift's API following this tutorial: https://youtu.be/AcrjEWsMi_E

**NOTE:** Pushshift now limits you to 100 posts per request (no longer the 500 in the screencast).