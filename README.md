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

Before working on building a model, I came accross various challeges with data ie there were many specials characters, numbers, links etc. To overcome this I used regex to remove unwanted links, digits etc then tokenized my dataset and removed the stop words. After performing Text Data Processing, below is the comparison of uncleaned tweets (left) vs cleaned tweets (right)

<p align = "center">
<img src = "https://github.com/payush624/Disaster-Tweets---Natural-Language-Processing/blob/21e69dc2750f2e21fa96e73c33c1ea613dd0febd/cleaned%20vs%20uncleaned.png">
</p>
<p align = "center">
Fig.2 - uncleaned tweets (left) vs cleaned tweets (right)
</p>

