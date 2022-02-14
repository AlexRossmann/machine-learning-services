# Vorhersage von erfolgreichen oder gescheiterten StartUps

<a href="https://colab.research.google.com/github/AlexRossmann/machine-learning-services/blob/main/Success%20Predicition/Prediction%20of%20Successful%20or%20Failed%20Startups/notebook.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Notebook In Google Colab"/></a>  



# Datenbeschreibung

Als Basis wird ein Datensatz aus Crunchbase verwendet, welcher in Form von 11 zusammenhängenden CSV Dateien bereitgestellt ist.
Der Datensatz besteht aus unterschiedlichen Merkmalen, wie Beziehung, Meilensteine und Ort.
DIe Daten sind in Test- und Trainingsdaten unterteilt.

# Modell

In diesem Service werden vier unterschiedliche Modelle verwendet, welche aus SVC, RandomForest, ExtraTrees und der GradientBoosting-Klassifikatoren bestehen.

# English Version

## Business Understanding
  
__Corporation__: Crunshbase Inc.  
__Industry__: Finances  
__Area of application__: Prediction  
__Business Objective__: The intended goal of this service is to predict the success or failure of StartUps.  
__Description__: The success of a StartUps is defined as the event that brings the founders of the company a large turnover through the process of Merger and Acquisitio or 
an initial public offering. If a company has to be shut down, it is considered a failure.

## Data Understanding
  
__Data Frame__: status  
__Source__: local csv  
__Data Creator__: Crunchbase  
__Date of Publication__: -  
__Data Type__: CSV  
__Description of Data Frame__: Data set with details of the startups, such as name, city, longitude and latitude, founding period, etc.
  
__Number of features__: 48  
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
  
__Algorithms__: SVC, Random Forest, Extra Trees, Gradient Boosting  
__Hyperparameter__:  
__Output__: supervised learning, classification  
__Data Split__: 80% train data, 20% test data   
__Model Description__:   
__Evaluation Metrics__: voting score: 0,7728102492615089; stacking score: 0,7837837837837837838

## Deployment
  
__Service__:  
__Target Group__: Finances  
__Benefits__: Through this service, investors and startups can predict whether the companies will succeed or fail
  
__Integration__:

# German Version

## Geschäftsverständnis
  
__Konzern__: Crunchbase  
__Industrie__: Finanzen  
__Anwendungsbereich__: Vorhersage von Erfolgreichen StartUps  
__Unternehmensziel__: Das angestrebte Ziel dieses Services ist das Vorhersagen eines Erfolges bzw. eines Misserfolges von StartUps  
__Beschreibung__: Der Erfolg eines StartUps wird definiert als das Ereignis, dass den Gründern des Unternehmens ein großen Umsatz durch den Prozess von Merger and Acquisitio oder einen Initial Public Offering einbringt. Muss ein Unternehmen stillgelegt werden, so gilt es als gescheitert.  
__Lösung__: na 

## Datenverständnis
  
__Datenrahmen__: Status    
__Quelle__: lokale csv  
__Datenersteller__: Cunshbase   
__Veröffentlichungsdatum__: -  
__Datentyp__: CSV       
__Beschreibung des Datenrahmens:__ Datensatz mit Angaben zu den Neugründungen, wie Name, Stadt, Längen- und Breitengrad, Gründungszeitraum usw.  
__Anzahl der Attribute__: 48  
__Anzahl der Zielvariablen__: 1    
__Datentyp pro Attribut__:   
__Datentyp pro Zielvariable:__ integer
  
__Anzahl der Beobachtungen:__ 924  
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
  
__Algorithmen__: SVC, Random Forest, Extra Trees, Gradient Boosting  
__Hyperparameter__:    
__Ausgabe__: supervised learning, classification  
__Datenaufteilung__: 80% Trainingsdaten, 205 Testdaten  
__Modellbeschreibung__:   
__Bewertungsmetriken__: voting score: 0,7728102492615089; stacking score: 0,7837837837837837838

## Bereitstellung
  
__Service__:  
__Zielgruppe__: Finanzen  
__Leistungen__: Durch diesen Service kann für Investoren und StartUps vorhergesagt werden, ob die Unternehmen erfolgreich sind oder scheitern  
__Integration__: 
