## Contents
This repo contains data, results, and information regarding Sentiment analysis of the 9 Mainline Star Wars movies. 

### including: 

Readme - explanation of the repository

Licensing - explans the terms under which this repository can be cited

Scripts - contains all source code for the project, scripts used with explanation of commands

Data - Contains all data for the project and a Data Appendix outlining analysis and variables for each respective dataset

Output - contains all output generated from data analysis including tables and figures 

## Section 1: Software and Platform

### Software:

Python: 3.10 via Google Colab

### Addons: 

vaderSentiment

NRClex

Pandas

Numpy

matplotlib

tdqm notebook 

nltk
- punkt
- wordnet
- averaged_perceptron_tagger
- stopwords
- brown
- vader_lexicon
- opinion_lexicon
- punkt_tab

### Platform:

Windows 10

## Section 2: Map of Documentation

README

LICENSE

SCRIPTS


DATA

- SW_01
- SW_02
- SW_03
- SW_04
- SW_05
- SW_06
- SW_07
  
OUTPUT

- anger
- anticip
- disgust
- download
- ep1
- ep2
- ep3
- ep4
- ep5
- ep6
- ep7
- fear
- joy
- neg
- pos
- sad
- surp
- trust

References 

## Section 3: Reproducing Results

Step 1: importing add ons
Start by downloading vaderSentiment and NRClex from the internet and using pip install to use them in Python. 
Import nltk and essential NLP datasets (punkt, wordnet, averaged_perceptron_tagger, stopwords, brown, vader_lexicon, opinion_lexicon, punkt_tab)
Import re, pandas, numpy, and matplotlib

Step 2: import data
Download all txt files under the Data folder
Assign each text file a respective episode variable (episode1 = SW_01.txt, episode2 = SW_02.txt, etc..)
Group the data into trilogies (Prequels = (episode1, episode2, episode3), original = (episode4, episode5, episode6), sequels = (episode7)

Step 3: Cleaning data
For each script use re to clean them, converting all text to lowercase, replace all new lines with a space, replace multiple spaces with a single space, remove numbers, remove punctuation (except spaces), and finally remove all screenplay markers (int, ext, cut, to, cont, continued, fade)

Step 3: Emotional Analysis
Use the “analyzer.polarity_scores()” command to calculate the VADER compound, positive, negative, and neutral scores for each film. Print the scores for each film.
Create a new variable for each script that uses NRCLex ex: (episode1_NRC = NRCLex(episode_clean)). Use the command episode_NRC.raw_emotion_scores to get the count of emotion in each movie. Also use the command episode_NRC.affect_frequencies to get the frequency of the emotion throughout each movie. 
Create a dictionary of the NRC frequencies for each episode and remove the positive and negative emotion. Then set the variable, “max_emotion_episode” to the max emotion frequency from each episode. Print the value.
 
Step 4: Plotting Results
In separate plots, plot the negative, positive, and neutral sentiment scores for the first and second trilogy on a bar graph.
Create a bar plot with the x-axis being each episode and y-axis being the frequency of an emotion. Make a bar plot for each emotion separately.
Create a bar plot with the x-axis being each emotion and y-axis being the frequency of an emotion. Make a bar plot for each episode separately. 


