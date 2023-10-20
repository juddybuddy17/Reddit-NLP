### The Data Science Process

**Problem Statement**
A Star Wars movie and Harry Potter movie are both being released this Christmas and my marketing team wants to use Reddit to identify the fans of each movie. We want to send targeted ads of the other movie to Reddit users in hopes to promote both movies to non-fanbase Reddit users. The issue is the hype is so real that the team is collecting posts at mass volume and cannot distinguish which subreddit it originated from.  

In order to predict which subreddit the post came from I have created three binary classification models which include combinations of Logistic Regression and Random Forest.  

**Data Collection**
Collected subreddits, r/HarryPotterBooks, r/StarWarsTheories using PRAW to pull posts from each subreddit. I then created the pulled data into a dataframe and saved as csv. I will concat the two cleaned dataframes to another csv so I can use it for the other models.

**Data Cleaning and EDA**
Deleted Unnamed: 0 column
Deleted any duplicate posts
Input a blank at any missings
Combined the “title” and “self_text” columns to make one text column
Binarized the subreddit column Harry : 0, Star Wars : 1

**Preprocessing and Modeling**
I wanted to see the difference of CVec and TVec so I am doing three models, two with different classifiers and two
with the same classifier but different preprocessor.

**Conclusion and Recommendations**
All the models seem to be overfit, but the predictions were not bad. There some mismatches that I thought should have been predicted better. More testing and modeling will need be to done to find a better predictor so that the marketing team can optimize their advertisement strategy.