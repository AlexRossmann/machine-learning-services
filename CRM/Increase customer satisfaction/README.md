# Steigerung von Kundenzufriedenheit bei Netflix

<a href="https://colab.research.google.com/github/AlexRossmann/machine-learning-services/blob/main/CRM/Increase%20customer%20satisfaction/notebook.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Notebook In Google Colab"/></a>  



Duruch die breitgefächerte Auswahlmöglichkeit an Serien und Filmen, ist es für den Nutzer zeitaufwändiger, interessante Filme für zu finden. 
Das langandauernde Durchsuchen der Mediathek sorgt für eine schlechte Benutzererfahrung, welche wiederum zu höheren Stornierungsraten führt.

Um die Stornierungsraten zu senken, gilt es zu überprüfen, ob durch das Anwenden von Machine Learning in Bezug auf Filmempfehlungen, 
die Kundenzufriedenheit gesteigert werden kann.

# Datenbeschreibung

Als Basis wird ein Datensatz aus Kaggle verwendet, welche im Jahre 2020 veröffentlicht wurde.
Der Datensatz besteht aus unterschiedlichen Unterkunftsmerkmalen, wie Genre, Title, Sprachen und viele weitere.
Sie sind in Trainings- und Testdaten unterteilt.

https://www.kaggle.com/ibtesama/getting-started-with-a-movie-recommendation- system

# Modell

In diesem Service wird die lineare Regression als Modell verwendet.


# English Version

## Business Understanding
  
__Corporation__: Netflix  
__Industry__: movies  
__Area of application__: algorhithms  
__Description__: In order to reduce future cancellation rates and at the same time increase the customer satisfaction of Netlix users, this service will be used to calculate movie recommendations that are individually adapted to the users.

## Data Understanding
  
__Data Frame__: status  
__Source__: https://www.kaggle.com/tmdb/tmdb-movie-metadata  
__Data Creator__: TMDb API   
__Date of Publication__: 2016  
__Data Type__: CSV  
__Description of Data Frame__: The dataset consists of different features which are useful in describing series and movies. These include features such as original_title, overview, popularity, production_companies, production_countries, release_date.  
__Number of features__: 20  
__number of targets__: 1  
__Data type per feature__: integer

## Data Preparation
  
__Dimensionality Reduction__: Attributes that do not add value or are not significant are removed  
__Outlier__:  
__Missing Data__:  
__Unbalanced Data__:  
__Data Conversion__: Coding the categorical features  
__Distribution Function__: StandardScaler

## Modelling and Evaluation
  
__Algorithms__: Linear Reression  
__Hyperparameter__:  
__Output__: supervised learning, classification  
__Data Split__: 80% train data, 20% test data   
__Evaluation Metrics__: train performance: 1.0; test performance: 0.508633196384475

## Deployment
  
__Service__: Increasement of customer satisfaction  
__Target Group__: Netflix users  
__Benefits__: This service enables the company to retain as many customers as possible and to increase customer satisfaction.  
__Integration__:

# German Version

## Geschäftsverständnis
  
__Konzern__: Netlix  
__Industrie__: Filme  
__Anwendungsbereich__: Filmempfehlungen   
__Beschreibung__: Um die Abbruchquoten in Zukunft zu senken und gleichzeitig die Kundenzufriedenheit der Netlix-Nutzer zu erhöhen, werden mit diesem Service individuell auf die Nutzer abgestimmte Filmempfehlungen berechnet.  
__Lösung__: na 

## Datenverständnis
  
__Datenrahmen__: Status    
__Quelle__: https://www.kaggle.com/tmdb/tmdb-movie-metadata  
__Datenersteller__: TMDb API   
__Veröffentlichungsdatum__: 2016  
__Datentyp__: CSV       
__Beschreibung des Datenrahmens:__ Der Datensatz besteht aus verschiedenen Merkmalen, die für die Beschreibung von Serien und Filmen nützlich sind. Dazu gehören Merkmale wie original_title, overview, popularity, production_companies, production_countries, release_date.  
__Anzahl der Attribute__: 20  
__Anzahl der Zielvariablen__: 1    
__Datentyp pro Attribut__:   
__Datentyp pro Zielvariable:__ integer
  
__Standortparameter:__    
__Verteilungsparameter:__    
__Korrelationsanalyse:__  

## Datenaufbereitung
  
__Dimensionsreduktion__: Attribute, die keinen Mehrwert bieten oder nicht signifikant sind, werden entfernt.    
__Ausreißer__:  
__Fehlende Daten__:  
__Unausgeglichene Daten__:    
__Datenkonvertierung__: Kodierung der kategorialen Merkmale.   
__Verteilungsfunktion__: StandardScaler  
__Funktionsskalierung__:  
__Multikollinearität__:  

## Modellierung und Auswertung
  
__Algorithmen__: Lineare Regression  
__Hyperparameter__:    
__Ausgabe__: supervised learning, classification  
__Datenaufteilung__: 80% Trainingsdaten, 20% Testdaten  
__Bewertungsmetriken__: Trainingsperformance: 1.0; Testperformance: 0.508633196384475  
__Weitere Informationen__:  

## Bereitstellung
  
__Service__: Steigerung der Kundenzufriedenheit  
__Zielgruppe__: Netflix Nutzer  
__Leistungen__: Dieser Service ermöglicht es dem Unternehmen, möglichst viele Kunden zu halten und die Kundenzufriedenheit zu erhöhen.  
__Integration__: 
