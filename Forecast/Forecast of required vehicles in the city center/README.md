# English Version
<a href="https://colab.research.google.com/github/AlexRossmann/machine-learning-services/blob/main/Forecast/Forecast%20of%20required%20vehicles%20in%20the%20city%20center/notebook.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Notebook In Google Colab"/></a>  



## Business Understanding
  
__Corporation__: Uber Inc.  
__Industry__: traffic  
__Area of application__: Prediction  
__Description__: Uber's business model consists of serving as an intermediary between driver and passenger. For concept success in terms of customer satisfaction,
efficient procedures must be in place for both parties.
Based on this, the following question will be answered:

"How can the amount of required vehicles in inner-city areas be predicted as precisely as possible using Uber as an example?"

## Data Understanding
  
__Data Frame__: active_vehicles  
__Source__: https://www.kaggle.com/fivethirtyeight/uber-pickups-in-new-york-city  
__Data Creator__: Uber Inc.  
__Date of Publication__: 2014  
__Data Type__: CSV  
__Description of Data Frame__: The data set consists of different accommodation characteristics, such as number of trips, date or number of active vehicles and many more.  
__Number of features__: 4  
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
  
__Algorithms__: Multiple Lineare Regression  
__Hyperparameter__:  
__Output__: supervised learning, classification  
__Data Split__: 80% train data, 20% test data   
__Model Description__: The targeted multiple linear regression model is a commonly used model for predictions. It will be created using scikit-learn and the Python module "Statsmodel". The model is supposed to be able to model a relationship between two or more features, based on a linear equation fitted to the observed data. However, the steps performed are similar in principle to those of simple linear regression. However, there are certain OLS assumptions that must be verified before the model can be developed. These are:
- Linearity
- no endogeneity
- normality, zero, mean, homoscedasticity
- no autocorrelation
- no multicollinearity

## Deployment
  
__Service__:  
__Target Group__: Uber users and providers  
__Benefits__: The quantity of vehicles required in the inner-city area can be forecast as precisely as possible   
__Integration__:

# German Version

## Geschäftsverständnis
  
__Konzern__: Uber Inc.  
__Industrie__: Verkehr  
__Anwendungsbereich__: Vorhersage von benötigten Fahrzeugen  
__Beschreibung__: Das Geschäftsmodell von Uber besteht daraus, als Vermittler zwischen Fahrer und Fahrgast zu dienen. Für einen Konzepterfolg in Bezug auf die Kundenzufriedenheit,
müssen effiziente Verfahren für beide Parteien vorhanden sein.
Auf Basis dieser Grundlage soll folgende Fragestellung beantwortet werden:

„Wie kann die Menge an benötigten Fahrzeugen im innerstädtischen Raum möglichst präzise prognostiziert werden am Beispiel von Uber?“  
__Lösung__: na 

## Datenverständnis
  
__Datenrahmen__: Aktive Fahrzeuge    
__Quelle__: https://www.kaggle.com/fivethirtyeight/uber-pickups-in-new-york-city  
__Datenersteller__: Uber   
__Veröffentlichungsdatum__: 2014  
__Datentyp__: CSV       
__Beschreibung des Datenrahmens:__ Der Datensatz besteht aus unterschiedlichen Unterkunftsmerkmalen, wie Anzahl der Fahrten, Datum oder Anzahl aktiver Fahrzeuge und viele weitere.   
__Anzahl der Attribute__: 4  
__Anzahl der Zielvariablen__: 1    
__Datentyp pro Attribut__:   
__Datentyp pro Zielvariable:__ integer
  
__Anzahl der Beobachtungen:__   
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
  
__Algorithmen__: Multiple Lineare Regression  
__Hyperparameter__:    
__Ausgabe__: supervised learning, classification  
__Datenaufteilung__: 80% Trainingsdaten, 20% Testdaten  
__Modellbeschreibung__: Multiple lineare Regression ist ein häufig verwendetes Model für Voraussagen. Sie wird mithilfe von scikit-learn sowie dem Python Modul „Statsmodel“ erstellt. Das Model soll in der Lage sein, eine Beziehung zwischen zwei oder mehreren Merkmalen zu modellieren, basierend auf einer linearen Gleichung, die an den beobachteten Daten angepasst wird. Die durchgeführten Schritte ähneln jedoch prinzipiell die der einfachen linearen Regression. Es gibt jedoch gewisse OLS- Annahmen, die überprüft werden müssen, bevor das Model entwickelt werden kann. Diese lauten:
- Linearität
- keine Endogenität
- Normalität, Zero, Mean, Homoskedastizität
- keine Autokorrelation
- keine Multikollinearität

## Bereitstellung
  
__Service__:  
__Zielgruppe__:  Uber Nutzer und Anbieter  
__Leistungen__: Die Menge an benötigten Fahrzeugen im innerstädtischen Raum kann möglichst präzise prognostiziert   
__Integration__: 
