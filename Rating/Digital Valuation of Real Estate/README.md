# English Version

<a href="https://colab.research.google.com/github/AlexRossmann/machine-learning-services/blob/main/Rating/Digital%20Valuation%20of%20Real%20Estate/notebook.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Notebook In Google Colab"/></a>  



## Business Understanding
  
__Corporation__: online marketplace  
__Industry__: real estate indutry  
__Area of application__: Evaluation  
__Business Objective__: With the help of AI, the given properties of the accommodation can be evaluated without the customers having to make a local visit  
__Description__: The real estate company wants to expand and digitize the individual process steps.
For example, real estate properties are to be valued without an appraiser having to visit the property on site.

## Data Understanding
  
__Data Frame__: price  
__Source__: https://www.kaggle.com/corrieaar/apartment-rental-offers-in-germany  
__Data Creator__: Immoscount24  
__Date of Publication__: 2019  
__Data Type__: CSV  
__Description of Data Frame__: The data set consists of different property characteristics, such as state, interior (balcony), year of construction or else uploaded photos.  
__Number of features__: 49  
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
  
__Algorithms__: linear regression  
__Hyperparameter__:  
__Output__: supervised learning, classification  
__Data Split__: 80% train data, 20% test data   
__Model Description__: The quality of a linear regression model can be determined by the coefficient of determination R2. This indicates whether the predictors are suitable for predicting the target variable. Applied to the training data, the model achieves an R2 value of 0.67. Thus, the model is neither in the overfitting nor in the underfitting range.
The R2 value of the test data is 0.68 and thus shows a marginally higher quality of the model than for the training data. It can be concluded that the multiple linear regression model is quite suitable for an initial estimation of the rental price. However, further refinements of the predictors can further improve the predictive accuracy. The business results will now be further explained in the following chapter, the deployment.
   
__Evaluation Metrics__: R2=0.6769948772700947

## Deployment
  
__Service__:  
__Target Group__: Real estate agencies and brokers  
__Benefits__: Through this service, more (possibly less) money can be obtained for the guest givers on airbn, as a fair price is determined through this service  
__Integration__:

# German Version

## Geschäftsverständnis
  
__Konzern__: Online-Marktplatz   
__Industrie__: Immobilienbranche  
__Anwendungsbereich__: Bewertung con Unterkünften  
__Unternehmensziel__: Mithilfe von KI können die gegebenen Features der Unterkunft analysiert und ein Preis berechnet werden   
__Beschreibung__: Das Immobilienunternehmen möchte expandieren und die einzelnen Prozessschritte digitalisieren. So sollen Immobilienobjekte bewertet werden, ohne dass ein Gutachter vor Ort die Immobilie besichtigen muss.  
__Lösung__: na 

## Datenverständnis
  
__Datenrahmen__: Mietpreis    
__Quelle__: https://www.kaggle.com/corrieaar/apartment-rental-offers-in-germany  
__Datenersteller__: Immoscount24   
__Veröffentlichungsdatum__: 2019  
__Datentyp__: CSV       
__Beschreibung des Datenrahmens:__ Der Datensatz besteht aus verschiedenen Immobilienmerkmalen wie Zustand, Innenausstattung (Balkon), Baujahr oder auch hochgeladenen Fotos.  
__Anzahl der Attribute__: 49  
__Anzahl der Zielvariablen__: 1    
__Datentyp pro Attribut__:   
__Datentyp pro Zielvariable:__ integer
  
__Anzahl der Beobachtungen:__ 268.850  
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
__Datenaufteilung__: 80% Trainingsdaten, 205 Testdaten  
__Modellbeschreibung__: Die Güte eines linearen Regressionsmodells lässt sich anhand des Bestimmtheitsmaßes R2 ermitteln. Dieses gibt an, ob die Prädiktoren zur Vorhersage der Zielvariablen geeignet sind. Auf die Trainingsdaten angewandt, erreicht das Modell einen R2-Wert von 0,67. Damit befindet sich das Modell weder im Overfitting- noch im Underfitting-Bereich.
Der R2-Wert der Testdaten beträgt 0,68 und zeigt damit eine geringfügig höhere Qualität des Modells als für die Trainingsdaten. Daraus lässt sich schließen, dass das multiple lineare Regressionsmodell für eine erste Schätzung des Mietpreises durchaus geeignet ist. Durch weitere Verfeinerungen der Prädiktoren kann die Vorhersagegenauigkeit jedoch weiter verbessert werden. Die Geschäftsergebnisse werden nun im folgenden Kapitel, der Anwendung, näher erläutert.  
__Bewertungsmetriken__: R2=0.6769948772700947

## Bereitstellung
  
__Service__:   
__Zielgruppe__:  Immobilienbüros und Makler  
__Leistungen__: Durch diesen Service kann für die Gastergeber auf airbn mehr (ggf. auch weniger) Geld erhalten werden, da durch diesen Service ein fairer Preis ermittelt wird  
__Integration__: 
