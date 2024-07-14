---
layout: page
title: Sentiment Analysis
description: Classifying sentiment or opinion expressed in tweets during 2012 US elections
img: "assets/img/projects/sentiment_analysis/thumbnail.png"
importance: 14
category: Other
---

<h4><u>Access this project</u></h4>
<b>GitHub repo:</b> <a href='https://github.com/komar41/twitter-sentiment-analysis'>https://github.com/komar41/twitter-sentiment-analysis</a> <br>
<b>Tools used:</b> Python, NumPy, Pandas, nltk, scikit-learn, matplotlib, seaborn, TensorFlow, Keras.
<p align='justify'>
The primary goal of this project is to classify sentiments expressed in tweets regarding the 2012 US election into <b>positive</b> and <b>negative</b> classes. <b>Sentiment analysis</b>, also known as opinion mining, is the process of determining and categorizing the emotions or opinions conveyed in a piece of text.
</p>
<h4><u>Data Wrangling</u></h4>
<p align='justify'>
First, we clean the tweets! Lowercasing, removing URLs and usernames, punctuation and numbers.
</p>
<pre><code>def dataClean(tweets_raw):
    cleanTweets = []
    for tweet in tweets_raw:
        tweet = tweet.lower() 
        tweet = re.sub(r'\w+:\/{2}[\d\w-]+(\.[\d\w-]+)*(?:(?:\/[^\s/]*))*', '', tweet) #remove URL
        tweet = re.sub(r'(\s)@\w+', r'', tweet) 
        tweet = re.sub(r'@\w+', r'', tweet) 
        tweet = re.sub('<[^<]+?>', '', tweet) 
        tweet = re.sub('[^A-Za-z0-9 ]+', '', tweet)
        tweet = re.sub(" \d+", " ", tweet) 
        lower_case = tweet.lower()

    words = lower_case.split()
    tweet = ' '.join([w for w in words if not w in nltk.corpus.stopwords.words("english")]) #remove stopwords
    ps = nltk.stem.PorterStemmer()
    stemmedTweet = [ps.stem(word) for word in tweet.split(" ")]
    stemmedTweet = " ".join(stemmedTweet)
    tweet = str(stemmedTweet)
    tweet = tweet.replace("'", "")
    tweet = tweet.replace("\"","")
    cleanTweets.append(tweet)

return cleanTweets
</code></pre>

<h4><u>Exploratory Data Analysis</u></h4>
<p align='justify'>
After cleaning the data, we move on to analysis. We checked the data distribution, words per tweet, and unique words in both Obama and Romney tweets. The following images are a few of these highlights.
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/twitter-sentiment-analysis/raw/main/assets/obama_tweets.png" alt="Obama Tweets" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/twitter-sentiment-analysis/raw/main/assets/romney_tweets.png" alt="Romney Tweets" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/twitter-sentiment-analysis/raw/main/assets/words_per_tweet.png" alt="Words per Tweet" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h4><u>Data Modeling and Results</u></h4>
<p align='justify'>
After data preprocessing and analysis, we trained the clean data on eight machine learning algorithms for sentiment classification. We performed tests using both 80-20 train-test split and 10-fold cross-validation. Furthermore, we analyzed precision, recall, F1-score, and accuracy measures. The results highlight that overall <b>support vector machine</b> performed better than the other models. Model <b>accuracy</b> for sentiment analysis on both Obama and Romney tweets is highlighted in the image below.
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/twitter-sentiment-analysis/raw/main/assets/accuracy_.png" alt="Model Accuracy" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<p align='justify'>
For more information, see the notebooks inside the <a href="https://github.com/komar41/twitter-sentiment-analysis/tree/main/Sentiment%20Analysis">Sentiment Analysis</a> folder.
</p>
<h4><u>Team</u></h4>
<p align='justify'>
<ul>
    <li>Kazi Shahrukh Omar</li>
    <li>Soham Pradhan</li>
</ul>
</p>
