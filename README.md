#### Overview

This project involves the comprehensive task of analyzing Twitter sentiments about Apple and Google products. The dataset is from CloudFlower and contains tweets, the app the tweet came from, and the emotion that connects to it. To analyze these sentiments it was necessary to export the data from excel to python. The ultimate goal was to filter for tweets classified as positive or negative. This was represented as either 0 or 1 in python. The other primary task was to create a binary classifier. 

#### Business Objective

For the purposes of this project, Apple and Google have hired me as a consultant to anlayze the sentiments from this dataset as a starting point to studying patterns of feedback that are informative to their products. Apple and Google are concerned with the increasing levels of negative comments and misinformation online. From connecting comments to their products it's possible to identify key words that are driving positive or negative feedback. 

#### Data Understanding and Analysis

The first step of the data analysis was to identify the columns needed from the three included. The three columns are the body of the tweets, the app the tweet originated from, and the emotion. The app the tweet originiated from was dropped as it wasn't deemed a primary focus compared to the emotions for each tweet. The four emotions were negative emotion, positive emotion, no emotion toward brand or product, or I can't tell. The negative and positive emotions were the two emotions kept. The other emotions were dropped. This was filtered by changing the column type from object to integer and then using the loc function to keep only the negative and positive emotions. 

The second step was to vectorize the data for our tweet text column. 

Then a train test set is completed with y as the emotion for either positive or negative and X as the text body. 

This train test set can now be used on three different models to see what model results in the highest accuracy score. The three models used are Logistic Regression, Random Forest, and Multinomial. Classification Reports were then created for these three models with an accuracy score as the primary measure of strength. The accuracy scores for the three models were 0.77 for Logistic Regression, 0.74 for Random Forest, and 0.78 for Multinomial. 

A cross validation was also created for these three models with a cv=5. The mean accuracy for these 3 models were 0.73 for Logisitic Regression, 0.71 for Random Forest, and 0.72 for Multinomial.

NLP Preprocessing: 

A process doc was created to generate a list of each word from each line of the body from the dataset. The idea here is to tokenize the words from the text body so that each word can be it's own string in a dataframe of words that are found. This conversion would be helpful to Apple & Google because it makes it easy to identify words that. The top 25 words that were most frequent are sxsw, mention, ipad, link, rt, apple, i, google, iphone, quot, store, app, new, get, austin, go, launch, android, circle, social, amp, need, use, come, time. Other words that appeared more than 100 times and stand out as being associated with positive reviews are need, good, great, win. Words that are more likely associated with negative reviews could be wait, design, or line.

#### Predictive Findings and Recommendations 

Based on the findings from the data I have a few recommendations:

The first would be to go through the most frequent words and create an analysis of the strength of the association with the word and what is considered to be a negative or positive comment. The NLP Preprocessing accomplishes the task of taking a string with a negative or positive comment and converting it to a datatable of words with the frequency of how many times the word appears in the reviews. 

A second recommendation would be to further this study by filtering for the words that are associated with positive or negative reviews in a specific fashion. Then products can be designed to fit descriptive words that are positive. This can be done with advertisements and other types of marketing that fits into the algorithms we've been discussing.




