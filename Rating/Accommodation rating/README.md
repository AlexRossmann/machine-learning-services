# English Version

<a href="https://colab.research.google.com/github/AlexRossmann/ml-services/blob/main/Rating/Accommodation%20rating/notebook.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Notebook In Google Colab"/></a>  



## Business Understanding
  
__Corporation__: online marketplace  
__Industry__: real estate indutry  
__Area of application__: Evaluation  
__Business Objective__: With the help of AI, the given features of the accommodation can be analyzed and a price calculated  
__Description__: Hosts of the airbnb platform have to choose the prices of their accommodations independently at the current time, 
although they often do not know where the actual price might be. 

## Data Understanding
  
__Data Frame__: price  
__Source__: https://www.kaggle.com/brittabettendorf/berlin-airbnb-data  
__Data Creator__: Berlin airbnb  
__Date of Publication__: 2018  
__Data Type__: CSV  
__Description of Data Frame__: Data set with accommodation characteristics, such as location, longitude and latitude, number of calls, availability/year, etc.  
__Number of features__: 16  
__number of targets__: 1  
__Data type per feature__: integer

## Data Preparation
  
__Dimensionality Reduction__: Attributes that do not add value or are not significant are removed  
__Outlier__:  
__Missing Data__:  
__Unbalanced Data__:  
__Data Conversion__: Coding the categorical features  
__Distribution Function__: Similarity with an exponential distribution for the attribute "TotalCharges" recognizable

## Modelling and Evaluation
  
__Algorithms__: linear regression, random forest  
__Hyperparameter__:  
__Output__: supervised learning, classification  
__Data Split__: 80% train data, 20% test data   
__Model Description__: After data preparation, the appropriate machine learning algorithm was modeled. This use case is a binary classification problem. A classical solution method for this type of problem is the so-called logistic regression. This is used to estimate the probability of success of an event that depends on the independent events.  
__Evaluation Metrics linear regression__: R2=0.3746541844751121  
__Evaluation Metrics random forest__: R2=0.6171130215435493


## Deployment
  
__Service__: Calculation of real estates with the aid of AI  
__Target Group__: Real estate agencies and brokers  
__Benefits__: Through this service, more (possibly less) money can be obtained for the guest givers on airbn, as a fair price is determined through this service  
__Integration__:

# German Version

## Geschäftsverständnis
  
__Konzern__: Online-Marktplatz   
__Industrie__: Immobilienbranche  
__Anwendungsbereich__: Bewertung von Unterkünften  
__Unternehmensziel__: Mithilfe von KI können die gegebenen Features der Unterkunft analysiert und ein Preis berechnet werden   
__Beschreibung__: Gastgeber der airbnb Plattform müssen zum aktuellen Zeitpunkt die Preise ihrer Unterkünfte eigenständig wählen, obwohl sie oft nicht wissen, wo der eigentliche Preis liegen könnte.   
__Lösung__: na 

## Datenverständnis
  
__Datenrahmen__: price    
__Quelle__: https://www.kaggle.com/brittabettendorf/berlin-airbnb-data  
__Datenersteller__: Berlin airbnb   
__Veröffentlichungsdatum__: 2018    
__Datentyp__: CSV       
__Beschreibung des Datenrahmens:__ Die Zeilen des Datensatzes stellen jeweils eine Immobilie dar. Die Spalten beschreiben die Merkmale oder Eigenschaften der jeweiligen Immobilien. Mit Hilfe dieser Daten wird versucht zu analysieren, welche Preise für Immobilien anhand von hinterlegten Merkmalen berechnet wird. Zu diesem Zweck enthalten die historischen Daten die Zielvariable "price", die Auskunft darüber gibt, wie wertvoll die Immobilie ist.  
__Anzahl der Attribute__: 16    
__Anzahl der Zielvariablen__: 1    
__Datentyp pro Attribut__:   
__Datentyp pro Zielvariable:__ integer
  
__Anzahl der Beobachtungen:__ 7043  
__Standortparameter:__    
__Verteilungsparameter:__  

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
  
__Algorithmen__: Lineare Regression, Random Forest  
__Hyperparameter__:    
__Ausgabe__: supervised learning, classification  
__Datenaufteilung__: 80% Trainingsdaten, 205 Testdaten  
__Modellbeschreibung__: Nach der Datenaufbereitung wurde der entsprechende maschinelle Lernalgorithmus modelliert. Bei diesem Anwendungsfall handelt es sich um ein binäres Klassifikationsproblem. Eine klassische Lösungsmethode für diese Art von Problem ist die sogenannte logistische Regression. Diese wird verwendet, um die Erfolgswahrscheinlichkeit eines Ereignisses zu schätzen, die von den unabhängigen Ereignissen abhängt.  
__Bewertungsmetriken Lineare Regression__: R2=0.3746541844751121  
__Bewertungsmetriken Random Forest__: R2=0.6171130215435493

## Bereitstellung
  
__Service__: Berechnung von Immobilien mittels KI  
__Zielgruppe__: Immobilienbüros und Makler   
__Leistungen__: Durch diesen Service kann für die Gastergeber auf airbn mehr (ggf. auch weniger) Geld erhalten werden, da durch diesen Service ein fairer Preis ermittelt wird


