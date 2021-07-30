# Twitter Sentiment Analysis
![intro](https://github.com/savss624/Readme-Images/blob/main/Twitter%20Sentiment%20Analysis/intro.jpg)
Natural Language Processing (NLP) is a unique subset of Machine Learning which cares about the real life unstructured data. Although computers cannot identify and process the string inputs, the libraries like NLTK, TextBlob and many others found a way to process string mathematically. Twitter is a platform where most of the people express their feelings towards the current context. As humans, we can guess the sentiment of a sentence whether it is positive or negative. Similarly, here we'll see how to train and develop a simple Twitter Sentiment Analysis supervised learning model using python and NLP libraries.

# Data Exploration
Since it is a supervised learning task we are provided with a training data set which consists of Tweets labeled with ***"Positive Sentiment"***, ***Neutral Sentiment"*** or ***"Negative Sentiment"*** and a test data set without labels.

Now we will read the data with pandas.

![data reading](https://github.com/savss624/Readme-Images/blob/main/Twitter%20Sentiment%20Analysis/data%20exploration.png)

# Data preprocessing and Feature Engineering
The given data sets are comprised of very much unstructured tweets which should be preprocessed to make an NLP model. In this project, we tried out the following techniques of preprocessing the raw data. For which we'll use a popular python Library ***"NLTK"***.
* Removal of punctuations.
* Removal of commonly used words (stopwords).
* Normalization of words.

### Removal of Punctuations and stopwords
Punctuations will be always a disturbance in NLP specially hashtags and “@” play a major role in tweets. 
Stopwords (most common words e.g: is, are, have) do not make sense in learning because they don’t have connections with sentiments. 

So removing them saves the computational power as well as increases the accuracy of the model.

### Normalization of words ***( Lemmatization )***
Lemmatization is a normalization technique where list of tokenized words are converted into shorten root words to remove redundancy. Lemmatization is the process of reducing inflected (or sometimes derived) words to their root form.

Lemmatization consider morphological analysis of the words and returns meaningful word in proper form. The output we will get after lemmatization is called ‘lemma’, which is a root word.

![data cleaning](https://github.com/savss624/Readme-Images/blob/main/Twitter%20Sentiment%20Analysis/data%20cleaning.png)

# Vectorization and modeling
CountVectorizer is used to transform a given text into a vector on the basis of the frequency (count) of each word that occurs in the entire text.
It is used to convert a collection of text documents to a vector of term/token counts. It also enables the pre-processing of text data prior to generating the vector representation.

CountVectorizer creates a matrix in which each unique word is represented by a column of the matrix, and each text sample from the document is a row in the matrix. The value of each cell is nothing but the count of the word in that particular text sample.

![vectorizer](https://github.com/savss624/Readme-Images/blob/main/Twitter%20Sentiment%20Analysis/Vectorizer.png)
So, we have now vectorized our sting data to numerical values in order to feed it to a machine learning algorithm. We choose Support Vector Machine classifier for this classification since it is very powerful and one of the most common algorithm used in NLP.

![modeling1](https://github.com/savss624/Readme-Images/blob/main/Twitter%20Sentiment%20Analysis/modeling1.png)
And also tuned the parameters of the svm model using GridSearchCV to improve its accuracy.

![modeling2](https://github.com/savss624/Readme-Images/blob/main/Twitter%20Sentiment%20Analysis/modeling2.png)

# Model Validation
Since we decided to select the technique of the Natural Language Processing, we have to validate it with the existing training data set before applying to the test data set.

![report](https://github.com/savss624/Readme-Images/blob/main/Twitter%20Sentiment%20Analysis/report.png)
An accuracy of 0.93837 is obtained for our training data which is a pretty good score.
