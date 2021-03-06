Finding Investment Opportunities - Predicting the Price of Bitcoin with Sentiment Analysis  
=================================================================

|Service|Status|
| -------------: | :---- |
| Travis Build   | [![Build Status](https://travis-ci.com/JeffreyJackovich/bitcoin-prediction-using-sentiment.svg?branch=master)](https://travis-ci.com/JeffreyJackovich/bitcoin-prediction-using-sentiment) |
| Coverage       | [![codecov](https://codecov.io/gh/JeffreyJackovich/bitcoin-prediction-using-sentiment/branch/master/graph/badge.svg)](https://codecov.io/gh/JeffreyJackovich/bitcoin-prediction-using-sentiment) |



### 10/2018 - 06/2020
# Contents
<div>
    <ul>1. <a href="https://github.com/JeffreyJackovich/bitcoin-prediction-with-sentiment#1-introduction">Introduction</a></ul>
    <ul><ul>1.1 Sentiment Analysis</ul></ul>
    <ul><ul>1.2 Twitter</ul></ul>
    <ul>2. <a href="https://github.com/JeffreyJackovich/bitcoin-prediction-with-sentiment#2-technologies">Technologies</a></ul>
    <ul>3. <a href="https://github.com/JeffreyJackovich/bitcoin-prediction-with-sentiment#3-methodology">Methodology</a></ul>
      <ul><ul>3.1 Bitcoin Price Data</ul></ul>
      <ul><ul>3.2 Technical Indicators</ul></ul>
      <ul><ul>3.3 Tweet source</ul></ul>
      <ul><ul>3.4 Tweet pre-processing</ul></ul>
    <ul>4. <a href="https://github.com/JeffreyJackovich/bitcoin-prediction-with-sentiment#4-results">Results</a></ul>
    <ul>5. <a href="https://github.com/JeffreyJackovich/bitcoin-prediction-with-sentiment#5-conclusions">Conclusions</a></ul>
    <ul>6. <a href="https://github.com/JeffreyJackovich/bitcoin-prediction-with-sentiment#6-future-work">Future Work</a></ul>
</div>

## 1. Introduction:  

In this project, my goal is to predict the price of Bitcoin from Tweets containing the string: 'BTC'.  

For more details, please refer to the full analysis below.

###  1.1  Sentiment Analysis

**Sentiment Analysis** 
    A type of natural language processing to identify and extract subjective information from text.  There are two type of user-generated content available on the web - facts and opinions.  Facts are statements about topics and are easily collectible from the Internet using search engines that index documents based on topic keywords.  Opinions are user specific statements exhibiting positive or negative sentiments about a certain topic.  Generally opinions are hard to categorize using keywords. [1] 

**Financial Markets**
    Public opinion regarding companies can be used to predict performance of their stocks in financial markets.  If people have a positive opinion about a product that company A has launched, then the share prices of A are likely to go higher.  Public opinion can be used as an additional feature in models to predict market performance.
     
###  1.2  Twitter
Twitter is an online social networking and micro-blogging service that enables
users to create and read short messages, called "Tweets". It is a global forum
with the presence of eminent personalities from the field of entertainment,
industry and politics. 

## 2. Technologies:
Programming Language: Python
<br>
Big data technologies: SparkML, Spark-SQL
<br>
Libraries: Pandas, Matplotlib, Scikit-learn, TensorFlow
 
## 3. Methodology: 
I used Twitter's querysearch option for the phrase: 'bitcoin'.

### 3.1 Tweet data source:
<ul>b. <a href="https://github.com/Jefferson-Henrique/GetOldTweets-python">GetOldTweets-python</a></ul>

### 3.2 Tweet Pre-processing: Pandas 
<ul><a href="https://github.com/JeffreyJackovich/bitcoin-prediction-with-sentiment/blob/master/tweet_pre-processing.ipynb">Tweet pre-processing: Pandas</a></ul>

### 3.3 Tweet Pre-processing: Spark 
<ul><a href="https://github.com/JeffreyJackovich/bitcoin-prediction-using-sentiment/blob/master/tweet_pre-processing_spark.ipynb">Tweet pre-processing: Spark</a></ul>

## 4. Results: 
LinearRegressor:
- Final RMSE (on training data): 1840.08
- Final RMSE (on test data): 3420.21

DNNRegressor:
- Final RMSE (on training data): 47.56
- Final RMSE (on test data): 61.90

<!--
<p><img width="1000"  
        src="https://github.com/JeffreyJackovich/bitcoin-prediction-using-sentiment/blob/master/plots/linearRegressor_test_results.png"> </p>
<br>
<br>
-->

## 5. Conclusions:
TBD  

## 5. Future Work:
Machine Learning Approaches: 
- Implement a Genetic Algorithm to optimize neural net's hyperparameter selection.

Optimization:
- Analyze the functions with <a href="https://docs.python.org/3.5/library/profile.html">cProfile</a> to determine the most inefficient functions to optimize.  Visualize optimization with <a href="http://pycallgraph.slowchop.com/en/master/">pycallgraph</a>.  

## References:

[1] Bo Pang and Lillian Lee. Opinion mining and sentiment analysis. _Foundations and trends in information retrieval_, 2(1-2):pages 1-135, 2008. 

[2] Empson, Rip. "Twitter Launches Clickable Stock Symbols, StockTwits' Howard Lindzon Says 'Hey, We Already Do That!'" TechCrunch, TechCrunch, 30 July 2012, techcrunch.com/2012/07/30/twitter-clickable-ticker-symbols/.

[3] Bollen, Johan, et al. "Twitter Mood Predicts the Stock Market." Twitter Mood Predicts the Stock Market., 14 Oct. 2010, pp. 1-8., arxiv.org/pdf/1010.3003.pdf.
