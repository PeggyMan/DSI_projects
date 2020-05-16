# **Project 3: Web APIs & Classification**

**Table of Content:**

* [Problem Statement](#Problem-Statement)
* [Executive Summary](#Executive-Summary)
* [Datasets](#Datasets)
* [Pre Processing](Pre_processing)
* [EDA](EDA)
* [Modelling](Modelling)



## **Problem Statement**

**Will a legal advice be misclassified as relationship advice?**

## **Executive Summary**

When people have relationship problems, apart from telling their friends and family, it is not surprised that they tend to share or post the issues on forum like reddit to ask for others'opinion. Some relationship issue can be in harm. For example, sex crime, stalking, rape, harresment, divorce or even life thretening scenario etc. These issues are indeed involved legal actions or legal consultancy.

Reddit is a globally well known social news platform,home to thousands of communities. It can be crucial as if the post owner is able to get appropriate advice or catch the attention in time via reddit, the user engaement will increase. When user engagement is enhance, it also facilitates to positive brand image.

Given 2 subreddit :r/legaladvice and r/relationshipadvice. We are helping Reddit to categorize the text messages(inclduing posts titles and selftext) into the above two predefined categories, by using two classification models to predict whether a posts be misclassified as relationship issue but actually it will be more appropriate to be labelled as a legal issue.

#### Here is the answers:

The two models has high accuracy score, 97%-98% of the posts are classified correctly, both Naive Bayes and Logistic Regression models are able to classify the subreddits.

- The top related words for relationship advice are : feel,love,girl,gf,think,date
- The top related words for legal advice are : sign,illegal,car,report,police,charge

However,there are 12 cases asking for legal advice but are labelled as relationship advice. These misclassified posts are mostly related to human relationship. For example, posts have mentioned the following words:, ex, husband,family, father, month, stepfather, parents, Sexting etc, they are all misclassified as relationship advice even though there are wordings in the posts,decribing the sceniro like crimial, raped, kill, beaten, abuse.

#### Improvement:

We are assuming the model will be able to spot posts that invloved wordings like 'divorce', 'sexual abuse' posts as they are in the boundary between legal and relationship. Unfortunatedly, no such posts are found.

As we are only examine around 1000 posts and only the title and selftext in this project, we should collect at least 10000 posts and to include other features like the comments,created time,length of post to have a more thorough  analysis, We can also run on others classifcaiton models such as random forrest and K- Nearest Neighbour.

I will also try different Stopwords with different parameters of the models.

#### Recommedation:

Knowing that there is limitation of the classification models,we can educate Reddit admins and the reddit moderators to be more aware and pay attention to cases invloving family and parenting problems.



## Datasets

The data set are collection of posts by using Reddit's API, which returns `.json` dictionaries for data requests. 

Posts are collected from two subreddits : legal advice and relationship_advice

Data Source: 

- [legal advice subreddit](https://www.reddit.com/r/legaladvice.json')
- [relationship_advice subreddit](https://www.reddit.com/r/relationship_advice.json)

This data set of legal_advice contains 1060 posts. The data set of relationship_advice contain 1296 posts. 

The post title and selftext will be combined for text classification and modelling 



## Pre Processing 

We do the data cleaning  by using Stemming, regular expression and cleaning  (i.e. removing HTML).

Then we use vectorizing with Count Vectorizer and TF-IDF (Term Frequency-Inverse Document Frequency) as these are the easiest way for us to convert text data into a structured, numeric X dataframe



## EDA

EDA includes find the top 30 words of each subreddit and visualise in bar plot, among these top words, finding the top common words that appeared on both subreddits. We will add these common words in create a new stop words list. 



## Modelling

Using the following models with different parameters :

Naive Bayes

Logistic Regression

We look for the top 50 features from these 2 models and compare the score and features of the models.

Then we use pipeline and gridsearchCV to opimize the classiification performance.



## Model Evaluation

Overall speaking, the two models obtain high accuracy score. Navie bayes with tdidf has 0.97 as in both train and test result, no overfitting and underfitting. But the top 50 features are not satisfying. 

Logistic Regression with count vectorizator are overfited. Training score is 0.99 while test score is 0.97. However, the top 50 features are making more sense and we can easily distingh the different words used in legal advice and relationship advice.


Lastly, I use pipeline and gridsearchCV for tdidf and logistic regression and the best test score slightly out perform the best train score : 
- best score_train is 0.9687095312095313
- best score_test is 0.9744027303754266

To sum up , 97% of the posts are classified correctly, both Naive Bayes and Logistic Regression models are able to classify the subreddits.

However,there are 12 cases asking for legal advice but are labelled as relationship advice. These misclassified posts are mostly related to human relationship. For example, posts have mentioned the following words:, ex, husband,family, father, month, stepfather, parents, Sexting etc, they are all misclassified as relationship advice even though there are wordings in the posts,decribing the sceniro like crimial, raped, kill, beaten, abuse.

It might because the posts in legal advice do not contain many crimial cases, as reflected on the top features of the legal advise, cases are mainly related to car, employment, landlord or properties issue.

 



### 
