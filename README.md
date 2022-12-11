# Disaster Tweets - Natural Language Processing

Twitter has become an important communication channel in times of emergency.
The ubiquitousness of smartphones enables people to announce an emergency they’re observing in real-time. Because of this, more agencies are interested in programatically monitoring Twitter (i.e. disaster relief organizations and news agencies). You may have noticed in case of some Natural calamities people tweet in search for help from people around the world also to make aware the Goverment of the same Country.

<a href="url"><img src="https://storage.googleapis.com/kaggle-media/competitions/tweet_screenshot.png" align="left" height="300" width="300" ></a>

But, it’s not always clear whether a person’s words are actually announcing a disaster. Take this example:

The author explicitly uses the word “ABLAZE” but means it metaphorically. This is clear to a human right away, especially with the visual aid. But it’s less clear to a machine.

The above problem is an perefct example for use case of Natural Lanaguage Processing. Using a dataset of 10,000 tweets. I've built an Machine Learning Model that predicts which Tweets are about real disasters and which one’s aren’t.

<br>
<br>
<br>
<br>


Let's take a look, how a non disaster and disaster tweet looks like.

<br>

<p align = "center">
<img src = "https://github.com/payush624/Disaster-Tweets---Natural-Language-Processing/blob/cae8a8bed6bdef968410378830b33e5e748ff53c/non%20disaster%20tweet%20example.png">
</p>
<p align = "center">
Fig.1 - Non Disaster Tweet Example
</p>


<p align = "center">
<img src = https://github.com/payush624/Disaster-Tweets---Natural-Language-Processing/blob/feb5feb19c875972193fb1b8530ee7f2a7e02718/disaster%20related%20tweet%20example.png>
</p>
<p align = "center">
Fig.2 - Disaster Tweet Example
</p>

<br>

Prior to building a model, I encountered several challenges with the data, such as the presence of special characters, numbers, and links. To overcome these issues, I applied regular expressions to remove unwanted elements, such as links and digits. I then tokenized the dataset and removed stop words. After performing text data processing, the comparison below illustrates the difference between uncleaned tweets (left) and cleaned tweets (right).

<p align = "center">
<img src = "https://github.com/payush624/Disaster-Tweets---Natural-Language-Processing/blob/21e69dc2750f2e21fa96e73c33c1ea613dd0febd/cleaned%20vs%20uncleaned.png">
</p>
<p align = "center">
Fig.3 - uncleaned tweets (left) vs cleaned tweets (right)
</p>

<br>

In general, we often work with a collection of text data that may or may not be labeled, and we want to build a machine learning model that can recognize patterns based on the words in the strings to predict new text data. Since computers only understand numerical data, we need to convert our text data into numerical form. To do this, I used both Count Vectorizer and Tf-Idf Vectorizer, so I could compare which vectorization method works best with my model. Next step was to split my dataset to training and testing set. I used the following Machine Learning algorithms Logistic Regression, Multinomial Naive Bayes, Support Vector Machine to build my model and compare which model works better. Below is the accuracy score for SVM which has higest score amongst the algorithms used.

<p align = "center">
<img src = "https://github.com/payush624/Disaster-Tweets---Natural-Language-Processing/blob/620aaf7b8c4af6184c308f02b05620a55a737e78/accuracy%20score%20svm.png">
</p>
<p align = "center">
Fig.4 - Accuracy score SVM
</p>

To evaluate the performance of my model, I tested it with a set of random tweets to see if it could accurately predict whether or not they were related to a disaster.

1 - disaster tweet

0 - Non disaster tweet


<p align = "center">
<img src = https://github.com/payush624/Disaster-Tweets---Natural-Language-Processing/blob/0dcecae1ad3552a8de2bbf6774986c6be52b1fa8/testing%20on%20user%20defined%20tweets.png>
</p>
<p align = "center">
Fig.5 - Testing model by giving random tweets for prediction
</p>

As you can see from above image model is able to predict tweets related to disaster 'flood flood save us' and 'volcanic eruption, save us'. "However, it is possible to confuse the model by providing it with input that contains a mix of different elements, as shown in the first example and i'm still working on improving my model accuracy and trying to understand different ML algorithms so I can implement it over here.

Check out my Notebook for code and model, feel free to contribute towards this project [Click here](https://github.com/payush624/Disaster-Tweets---Natural-Language-Processing/blob/f8e400204fe531c03918dea2305de9dfcddaa7de/Disaster_Tweets_Kaggle_Compitition.ipynb)

