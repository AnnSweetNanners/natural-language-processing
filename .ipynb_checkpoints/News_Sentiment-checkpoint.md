# Natural Language Processing
Unit 12 Homework- Natural Language Processing

This notebook analyzes news articles on cryptocurrenices Bitcoin and Etherium.

## I. Dependencies
This project utilizes the following libraries:
* os
* Pandas
* dotenv
* nltk.sentiment.vader(natural language toolkit)
    * Imports:
        * SentimentIntensityAnalyzer
* newsapi
    * Imports:
        * NewsApiClient
* nltk.tokenize 
    * Imports:
        * word_tokenize
        * sent_tokenize
* nltk.corpus
    * Imports:
        * stopwords
* nltk.stem
    * Imports:
        * WordNetLemmatizer
        * PorterStemmer
* string
    * Imports:
        * punctuation    
       
* Collections
    * Imports:
        * Counter
* nltk
    * Imports:
        * ngrams
* wordcloud
    * Imports:
        * WordCloud
* matplotlib.pyplot
    * .style.use('seaborn-whitegrid')
* matplotlib 
    * .rcParams['figure.figsize']=[20.0, 10.0]
* Spacy
    * Imports:
        * displacy
        
This project utilizes the following magic functions:
* %matplotlib inline

## II. Assumptions

The articles imported from newsapi are truncated. Analysis also illustrated that many of the articles are pulled from the same sources. Additionally it appears all articles are from 2020 and from September to present. I'm associating this with use of a free version of the API. This does affect the comprehenisveness of the analysis.

Still the exercise demonstrates the value in natural language processing.


## III. Summary of Findings
Analysis of news articles involving Bitcoin and Ethereum show a largely neutral sentiment towards both cryptocurrencies, with Ethereum having a slight edge over Bitcoin in the positive sentiment analysis.

When reviewing the top 10 words for articles about each cryptocurrency, 'satoshi' and 'nakoboto' came up 22 times. A quick Google search proved that Satoshi Nakaboto is a writer at [thenextweb](https://thenextweb.com/author/satoshi-nakaboto/) and writes about Bitcoin everyday. Quite a few words from his tagline show up frequently in the top 10 words. It appears NewsApi is getting most of the articles (in the free version) from this site.

When you remove the words in the tagline, it would appear most of the top words in the  bitcoin articles are fairly generic as they are in the ethereum articles.

Both the WordClouds and the NER have similar results. The most common words for etither cryptocurrency was bitcoin. Words like "intrinsic" and 'value'

Interestingly countries like Nigera and Lagos show up in the analysis, likely because crypto investment and use appears to be on the rise in those countries. Britian also shows up, and according to [bitcoin.com](https://news.bitcoin.com/significant-increase-uk-2-6-million-have-bought-cryptocurrencies/) investment is also on the rise there.


## IV. Questions Answered
>Q: Which coin had the highest mean positive score?

>A: Ethereum had the highest mean positive sentiment score at 0.086

>Q: Which coin had the highest compound score?

>A: Bitcoin has the highest compound score at .216

>Q. Which coin had the highest positive score?

>A: Ethereum had the highest max positive score at .278
