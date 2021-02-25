# Tweet Analysis
This is a short demo application to show how analysis on Tweets can be done.
The main library used for retrieving Tweets from Twitter is a python library Tweepy.

# Requirements
* You would need to replace the API keys in the notebook tweet_explore.ipynb with your own keys. You can sign up for your own API keys here https://developer.twitter.com/en
* Other packages and dependencies are listed in requirements.txt.

## Section 1 - Retrieving tweets
This section how you can search and retrieve tweets related to a certain topic.
Tweets are then parsed into a pandas dataframe which can then be used for further analysis.

## Section 2 - Frequency of hashtags for live stream Tweets
In this section, we use the streaming provided by the Tweepy library to retrieve Tweets that are streamed lived. These tweets are written to a text file, which can then be read and presented into a chart.

We use the method async = True when streaming the tweets in the notebook so that it is non-blocking. The next block of code then reads the text file every 3 seconds to retrieve the latest set of hashtags, and plots them using matplotlib.

#### Future enhancements
Pyspark offers a streaming library which can be used to ingest data from a stream. This would be a more efficient approach. (Reason it wasn't used here is because the Spark installation does not seem to agree with the new M1 Macs hardware, and I faced some difficulties during installation. )


## Section 3 - Sentiment analysis of Tweets
In this section, we explore how we make use of Textblob, a popular Python NLP library to perform a simple sentiment analysis on Tweets related to Bitcoin. 
