## Table of Contents
- [Installation](#install)
- [Project Overview and Motivation](#motivate)
- [File Descriptions](#describe)
- [Licensing, Authors, and Acknowledgements](#acknowledge)

<a id='install'></a>
### Installation
1. Python 3.6 and latest from [here](https://www.python.org/downloads/)
2. Anaconda distribution of Python from [here](https://www.anaconda.com/blog/anaconda-distribution-2022-10#).
3. Natural Language Tool Kit (NLTK) and its functionalities like _'punkt', 'wordnet', 'averaged_perceptron_tagger', 'stopwords'_. Just run the following in your command prompt: _pip install nltk_

<a id='motivate'></a>
### Project Overview and Motivation 
This project is a competition staged at kaggle. More info about the competition is [here](https://www.kaggle.com/competitions/nlp-getting-started/overview).<br>  

Twitter has become an important communication channel in times of emergency. The ubiquitousness of smartphones enables people to announce an emergency they’re observing in real-time. Because of this, more agencies are interested in programatically monitoring Twitter (i.e. disaster relief organizations and news agencies).

But, it’s not always clear whether a person’s words are actually announcing a disaster. Take this example:

The author explicitly uses the word “ABLAZE” but means it metaphorically. This is clear to a human right away, especially with the visual aid. But it’s less clear to a machine.

In this competition, you’re challenged to build a machine learning model that predicts which Tweets are about real disasters and which one’s aren’t. You’ll have access to a dataset of 10,000 tweets that were hand classified. If this is your first time working on an NLP problem, we've created a quick tutorial to get you up and running.<br>

The first part is the Extract, Transform, and Load(ETL) process. Here, the dataset is read into a dataframe, then cleaned with pandas, and stored in a SQLite database.

The second part is the machine learning portion. Here, the needed columns are extracted. Then, a machine learning pipeline is built that uses Natural Language Tool Kit (NLTK), as well as scikit-learn's Pipeline to output a final model that uses the text column to predict disaster text. The model is exported to a pickle file and used to form a new dataframe with two columns: _text_ and _y_pred_.<br>


<a id='describe'></a>
### File Descriptions

There is one file and one folder. The file __nlp_challenge__ contains the codes for the modeling.
Five files are available in the __data__ folder: train.csv, test.csv, y_pred.plk, result.csv, and sample_submission.csv.
Each sample in the train and test set has the following information:

- The text of a tweet
- A keyword from that tweet (although this may be blank!)
- The location the tweet was sent from (may also be blank)

You are predicting whether a given tweet is about a real disaster or not. If so, predict a 1. If not, predict a 0.

Files
- train.csv - the training set
- test.csv - the test set
- sample_submission.csv - a sample submission file in the correct format
- result.csv - model prediction result appended to the predicted text
- y_pred.plk - pickle file that stores the predicted results

Columns
- id - a unique identifier for each tweet
- text - the text of the tweet
- location - the location the tweet was sent from (may be blank)
- keyword - a particular keyword from the tweet (may be blank)
- target - in train.csv only, this denotes whether a tweet is about a real disaster (1) or not (0)


<a id='acknowledge'></a>
### Licensing, Authors, Acknowledgements
The data used is from [kaggle](https://www.kaggle.com/competitions/nlp-getting-started/data).
