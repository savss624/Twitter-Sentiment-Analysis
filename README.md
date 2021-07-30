# Twitter Sentiment Analysis
Natural Language Processing (NLP) is a unique subset of Machine Learning which cares about the real life unstructured data. Although computers cannot identify and process the string inputs, the libraries like NLTK, TextBlob and many others found a way to process string mathematically. Twitter is a platform where most of the people express their feelings towards the current context. As humans, we can guess the sentiment of a sentence whether it is positive or negative. Similarly, here we'll see how to train and develop a simple Twitter Sentiment Analysis supervised learning model using python and NLP libraries.

# Data Exploration
Since it is a supervised learning task we are provided with a training data set which consists of Tweets labeled with “1” or “0” and a test data set without labels.
* label “0” :  ***Positive Sentiment***
* label “1” :  ***Negative Sentiment***

Now we will read the data with pandas.

# Data preprocessing and Feature Engineering
The given data sets are comprised of very much unstructured tweets which should be preprocessed to make an NLP model. In this project, we tried out the following techniques of preprocessing the raw data. For which we'll use a python Library ***"NLTK"***.
* Removal of punctuations.
* Removal of commonly used words (stopwords).
* Normalization of words.

### Removal of Punctuations and stopwords
Punctuations will be always a disturbance in NLP specially hashtags and “@” play a major role in tweets. 
Stopwords (most common words e.g: is, are, have) do not make sense in learning because they don’t have connections with sentiments. 

So removing them saves the computational power as well as increases the accuracy of the model.

### Normalization of words ***( Lemmatization )***
