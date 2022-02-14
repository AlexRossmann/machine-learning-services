# Improvement of components for autonomous motor vehicles
>see __German Version__ [below](#German_version)

<a href="https://colab.research.google.com/github/AlexRossmann/machine-learning-services/blob/main/Automotive/Improvement%20of%20components%20for%20autonomous%20motor%20vehicles/notebook.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Notebook In Google Colab"/></a>  



## Business Understanding

This case study is intended to assist technology companies in developing and improving components for autonomous vehicles. In doing so, this case study poses the question: In which areas are the weaknesses of the tested systems and how can these be classified? The question will be answered by classifying the reasons for the human test driver's intervention in the system. In doing so, the reasons are to be classified into different categories:
  - Software problems
  - hardware problems
  - Software and hardware problems (problems that occur in combination)
  - Problems caused by objects of traffic control (e.g. malfunctions of traffic light systems)
  - problems caused by other road users
  - external influences (including e.g. blockages, hidden elements, weather and road conditions)
other problems


__Corporation:__   None  
__Industry:__   Automotive industry  
__Area of Application:__  technology  
__Business Objective:__   TThe dataset will be used to examine where the technology shows weaknesses and how the problems can be categorized. The aim is to support technology companies in the development of components in the field of autonomous driving  

## Data Understanding

The underlying dataset was obtained from Kaggle and shows necessary interventions by a driver in autonomous driving vehicle technology. It was recorded from December 1, 2018 to November 30, 2019 and is licensed under U.S. Government Works. The data processing is done with the help of a Jupyter notebook, which is included in the most popular data science platform "Anaconda". The data set is in 8885 x 9 format.


__Name of Dataset:__  Automated driving

__Source:__  https://www.kaggle.com/art12400/2019-autonomous-vehicle-disengagement-reports 

__Data Creator/Publisher:__  Art124

__Date of Publication:__  2019

__Data Type:__   csv  

__Number of Features:__  9  

__Number of Observations:__  8885  

Just some of the 9 features listed below  

| Feature  | Data Type|
|-----|------|
|Manufacturer                               |object|
|Permit Number                              |object|
|DATE                                       |object|
|VAN NUMBER                                 |object|
|OPERATING WITHOUT DRIVER                   |object|
|DRIVER PRESENT                             |object|
|DISENAGEMENT INITIATED BY                  |object|
|DISENAGEMENT LOCATION                      |object|
|FACTS CAUSING DISENAGEMENT                 |object|
  



## Data Preparation

The main part of the data mining is the preparation of the data, which is done below.
The first analysis shows that the data set consists mainly of categorical values. In addition, the column names are very long and they contain too much information.

## Modelling and Evaluation

__Algorithms:__   Decision Tree, K-Nearest-Neighbor-Algorithmus
__Output:__  Software, Hardware  


## Deployment

__Target Group:__  Automotive industry   
__Benefits:__  The data analysis has clearly shown that most problems exist in the area of the combination of software and hardware. To ensure road safety, the primary goal is to provide mature software, robust hardware and their interoperability.
By identifying and classifying the existing problems of autonomous motor vehicles on public roads, technology companies can ensure more efficient development of components and the greatest possible safety on the roads.


  


<a id="German_version"></a> 

# Titel (Deutschsprachige Version)  

## Geschäftsverständnis
Diese Fallstudie soll Technologieunternehmen bei der Entwicklung und Verbesserung von Komponenten für autonome Fahrzeuge unterstützen. Dabei wirft diese Fallstudie die Frage auf: In welchen Bereichen liegen die Schwächen der getesteten Systeme und wie lassen sich diese einordnen? Die Frage wird beantwortet, indem die Gründe für den Eingriff des menschlichen Testfahrers in das System klassifiziert werden. Dabei sollen die Gründe in verschiedene Kategorien eingeteilt werden:
  - Software-Probleme
  - Hardware-Probleme
  - Software- und Hardwareprobleme (Probleme, die in Kombination auftreten)
  - Probleme, die durch Objekte der Verkehrssteuerung verursacht werden (z. B. Fehlfunktionen von Lichtsignalanlagen)
  - Probleme, die durch andere Verkehrsteilnehmer verursacht werden
  - äußere Einflüsse (einschließlich z. B. Blockaden, verborgene Elemente, Wetter- und Straßenbedingungen)
sonstige Probleme




__Konzern:__  Automobil   
__Industrie:__  Automobil Industrie  
__Lösung:__  Vorhersage von Software und Hardware Probleme  

## Datenverständnis

Der zugrundeliegende Datensatz stammt von Kaggle und zeigt notwendige Eingriffe eines Fahrers in autonom fahrende Fahrzeugtechnologie. Er wurde vom 1. Dezember 2018 bis zum 30. November 2019 aufgezeichnet und ist unter U.S. Government Works lizenziert. Die Datenverarbeitung erfolgt mit Hilfe eines Jupyter-Notebooks, das in der populärsten Data-Science-Plattform "Anaconda" enthalten ist. Der Datensatz liegt im Format 8885 x 9 vor.

__Name des Datensatz:__  Automated driving   
__Quelle:__  https://www.kaggle.com/art12400/2019-autonomous-vehicle-disengagement-reports   
__Datenersteller:__   Art124  
__Veröffentlichungsdatum:__  2019  
__Datenformat:__   csv    
__Anzahl der Merkmale:__  9  
__Anzahl der Beobachtungen:__  8885  

## Datenaufbereitung
  Der wichtigste Teil des Data Mining ist die Aufbereitung der Daten, die im Folgenden vorgenommen wird.
Die erste Analyse zeigt, dass der Datensatz hauptsächlich aus kategorischen Werten besteht. Darüber hinaus sind die Spaltennamen sehr lang und enthalten zu viele Informationen.



## Modellierung und Auswertung

__Algorithmen:__  Decision Tree, K-Nearest-Neighbor-Algorithmus




## Bereitstellung

__Service:__  Vorhersage von Software und Hardware Probleme

__Zielgruppe:__  Automobil Industrie 

