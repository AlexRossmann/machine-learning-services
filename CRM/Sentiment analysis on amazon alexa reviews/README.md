# Sentiment analysis on amazon alexa reviews
>see __German Version__ [below](#German_version)

<a href="https://colab.research.google.com/github/AlexRossmann/ml-services/blob/main/CRM/Sentiment%20analysis%20on%20amazon%20alexa%20reviews/notebook.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Notebook In Google Colab"/></a>  



## Business Understanding

__Corporation:__   Amazon  
__Industry:__   e-Commerce  
__Area of Application:__   Analyze User Generated Comments and User Generated Content  
__Business Objective:__   Analyze if a users comment is positive or negative. This is also called sentiment analysis.  
__Description:__  Customers can give feedback to Products they bought through amazon by talking with the alexa speach assistant  
__Solution:__  The combination of words in a comment are analysed.  

## Data Understanding
### example comments:
0                                           Love my Echo!  
1                                               Loved it!  
2       "Sometimes while playing a game, you can answe...  
3       "I have had a lot of fun with this thing. My 4...  
4                                                   Music  
                              ...                          
3145    "Perfect for kids, adults and everyone in betw...  
3146    "Listening to music, searching locations, chec...  
3147    "I do love these things, i have them running m...  
3148    "Only complaint I have is that the sound quali...  

__Name of Dataset:__    Amazon Alexa Reviews  
__Source:__  https://www.kaggle.com/sid321axn/amazon-alexa-reviews  
__Data Creator/Publisher:__  amazon  
__Date of Publication:__  2018-07-31  
__Data Type:__   tsv 
__Description of Data Frame:__  This dataset consists of a nearly 3000 Amazon customer reviews (input text), star ratings, date of review, variant and feedback of various amazon Alexa products like Alexa Echo, Echo dots, Alexa Firesticks etc. for learning how to train Machine for sentiment analysis.  
__Number of Features:__  5  
__Number of Targets:__  1  
__Number of Observations:__  3000   
__Distribution parameter:__ 257 negative reviews: 2893 positive reviews   

| Feature  | Data Type|
|-----|------|
|rating          |   int64  |
|date            |   str [ example: "30-Jul-18" ]  |
|variation       |   str [ example: "Black" ]  |
|verified_reviews|   str [ example: ""Given as a gift to my wife, to compliment my echo.  She loves it."" ]  |
|feedback        |   int64  |
|length          |   int64  |

## Data Preparation

__Dimensionality Reduction:__  all features other then the comments are removed   
__Unbalanced Data:__  the data is unbalanced, as there are way more positive reviews then negative reviews  
__Remove Stopwords:__  Stopwords are words, that are used manly as a filler in sentences, or words, that aren't meaningful themselves. These words are listed in the module stopwords in nltk.corpus  
__Data Conversion:__  The comments are converted to all lowercase letters and the stopwords are removed. Then the scentences get split into an array of individual words.     
__CountVectorizer:__ The CountVectorizer from sklearn.feature_extraction.text is used to extract the 2500 most important Words in the whole dataset.  
Based on these 2500 words every comment can be described with a 1 by 2500 vector. The number in each field represents the number of times the word associated with this field can be found in the comment.  

## Modelling and Evaluation

__Algorithms:__  DecisionTreeClassifier; DecisionTreeClassifier  
  
__Output:__  
__Data Split:__  train test split  80 % 20 %  
__Model Description:__  The model decides if a comment is positive   or negative  
__Evaluation Metrics:__  The model is correct 89 % of the time  
 | |precision   |  recall   | f1-score   | support |
 |- |- |- |- |-
  |          0     |   0.39    |   0.54    |   0.45     |    54
   |         1     |   0.96     |  0.92    |   0.94     |   576
 |    accuracy       |           |          |  0.89     |   630
  |  macro avg     |   0.67    |   0.73    |   0.70     |   630
 |weighted avg    |    0.91    |   0.89     |  0.90    |    630 

## Deployment

__Service:__  
__Target Group:__  
__Benefits:__  
__Integration:__  

<a id="German_version"></a> 

# Titel (Deutschsprachige Version)  

## Geschäftsverständnis

__Konzern:__  
__Industrie:__  
__Anwendungsbereich:__  
__Unternehmensziel:__  
__Beschreibung:__  
__Lösung:__  

## Datenverständnis

__Name des Datensatz:__  
__Quelle:__  
__Datenersteller:__  
__Veröffentlichungsdatum:__  
__Datenformat:__   csv?  
__Beschreibung des Datenrahmens:__  
__Anzahl der Merkmale:__  
__Anzahl der Beobachtungen:__  
__Standortparameter:__  
__Verteilungsparameter:__  
__Korrelationsanalyse:__  


## Datenaufbereitung

__Dimensionsreduktion:__  
__Ausreißer:__  
__Fehlende Daten:__  
__Unausgeglichene Daten:__  
__Datenkonvertierung:__  
__Verteilungsfunktion:__  
__Merkmal skalierung :__  
__Test auf Multikollinearität:__  

## Modellierung und Auswertung

__Algorithmen:__  
__Hyperparameter:__  optimierung der Trainingsrate / Batch size, ...  
__Ausgabe:__  
__Datenaufteilung:__  train test split  
__Modellbeschreibung:__  
__Bewertungsmetriken:__  
__Weitere Informationen:__  

## Bereitstellung

__Service:__  
__Zielgruppe:__  
__Leistungen:__  
__Integration:__  
