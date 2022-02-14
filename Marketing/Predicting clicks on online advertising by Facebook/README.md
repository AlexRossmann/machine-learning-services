# Advertising Prediction Notebook
>see __German Version__ [below](#German_version)

<a href="https://colab.research.google.com/github/AlexRossmann/machine-learning-services/blob/main/Marketing/Predicting%20clicks%20on%20online%20advertising%20by%20Facebook/notebook.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Notebook In Google Colab"/></a>  



## Business Understanding

From an economic perspective, it is necessary for Facebook to keep customers on their streaming platform for as long as possible. However, the question now arises as to how this can be achieved. The problem here is that Netflix has a good data basis, but this must first be processed and then developed into a digital service. Furthermore, it must be specified which data is available at all, which services can be implemented based on this data, and what added value the customer and Netflix itself derive from this. As a service, this paper deals with a recommendation model that suggests a selection of similar offers to the user for each film or series offered.

  
__Corporation:__   None    
__Industry:__   Facebook    
__Area of Application:__  Social Media     
__Business Objective:__   Identify the clicks on the online advertising

## Data Understanding

In this notebook, the advertising dataset of Kaggle is analyzed. It consists of 10 columns with a total of 1000 rows. The use case consists of predicting whether a website visitor will click on an advertisement or not based on his demographics and internet usage data.
The Clicked on Ad target value is perfectly balanced between the two categories (0.1), as the mean value is exactly 0.5. This means that there are the same number of values for both categories (500 each). In addition, we can see that the Ad Topic Line and City features have very many unique values (1000 and 969 "unique" values, respectively), which means that. It can be seen that there are significant differences between the user profiles. Users who click on an ad (Clicked on Ad=1) spend less time on the website on average, are older (approx. 40), have a lower income and use the Internet significantly less. From this information, a rough user profile can already be derived, which could also be relevant for a company's marketing and sales to optimize their measures based on the user profiles.



  
__Name of Dataset:__  Advertising    
__Source:__  https://www.kaggle.com/fayomi/advertising  
__Data Creator/Publisher:__  fayomi  
__Date of Publication:__  2018  
__Data Type:__   csv    
__Number of Features:__  10    
__Number of Observations:__  1000    
__Correlation Analysis:__  -

Just some of the 10 features listed below  

| Feature  | Data Type|
|-----|------|
|Daily Time Spent on Site            |   float64  |
|Age                                 |   int64    |
|Area Income                         |   float64  |
|Daily Internet Usage                |   float64  |
|Ad Topic Line                       |   object   |
|City                                |   object   |
|Male                                |   int64    |
|Country                             |   object   |
|Timestamp                           |   object   |
|Clicked on Ad                       |   int64    |


--> 
## Data Preparation  
__Dimensionality Reduction:__ 1 column with the subject id 'subject'-->only for filtering, must be removed     
__Missing Data:__  no missing data    
__Unbalanced Data:__  Oversampling wwith imblearn.over_sampling.RandomOverSampler    
__Multicollinearity:__  All Features with a VIF over 10 are discarded (522 Features are discarded)  
at the end 39 Features are left  

## Modelling and Evaluation
  
__Algorithms:__  Logistische Regression; Decision Tree;   
__Output:__  the subject clicks on the advertisement    
__Data Split:__    
__Evaluation Metrics:__  
| model_type | accuracy_train	|accuracy_test|
|-----|------|---|		
|LogReg |	0.9696|	0.9032	|
|DecisionTree|	0.9261 |	0.9295	|


## Deployment
  
__Target Group:__  Social Media Facebook   
__Benefits:__  In particular, the features "Daily Time Spent on Site" and "Daily Internet Usage" have a high negative impact on the decision of the model, i.e. the user will not click on the ad. This is also in line with the findings which show that customers are more likely to click on an ad if they spend less time on a website. 
  
__Integration:__    


<a id="German_version"></a> 

# Titel (Deutschsprachige Version)  

## Geschäftsverständnis
Aus wirtschaftlicher Sicht ist es für Facebook notwendig, die Kunden so lange wie möglich auf seiner Streaming-Plattform zu halten. Nun stellt sich aber die Frage, wie dies erreicht werden kann. Das Problem dabei ist, dass Netflix zwar über eine gute Datenbasis verfügt, diese aber erst einmal aufbereitet und zu einem digitalen Angebot entwickelt werden muss. Außerdem muss festgelegt werden, welche Daten überhaupt vorhanden sind, welche Dienste auf Basis dieser Daten realisiert werden können und welchen Mehrwert der Kunde und Netflix selbst daraus ziehen. Als Service geht es in diesem Beitrag um ein Empfehlungsmodell, das dem Nutzer zu jedem angebotenen Film oder jeder Serie eine Auswahl an ähnlichen Angeboten vorschlägt.


  
__Konzern:__  None  
__Industrie:__  Facebook  
__Anwendungsbereich:__  Social media   
__Lösung:__  Identifizieren der Klicks auf die Online-Werbung

## Datenverständnis

In diesem Notebook wird der Datensatz von Kaggle analysiert. Er besteht aus 10 Spalten mit insgesamt 1000 Zeilen. Der Anwendungsfall besteht in der Vorhersage, ob ein Website-Besucher auf der Grundlage seiner demografischen Daten und seiner Internetnutzungsdaten auf eine Anzeige klicken wird oder nicht.
Der Zielwert für angeklickte Werbung ist perfekt zwischen den beiden Kategorien ausgeglichen (0,1), da der Mittelwert genau 0,5 beträgt. Dies bedeutet, dass es für beide Kategorien die gleiche Anzahl von Werten gibt (jeweils 500). Darüber hinaus können wir feststellen, dass die Merkmale "Ad Topic Line" und "City" sehr viele eindeutige Werte aufweisen (1000 bzw. 969 "eindeutige" Werte), was bedeutet, dass. Es ist zu erkennen, dass es erhebliche Unterschiede zwischen den Nutzerprofilen gibt. Nutzer, die auf eine Anzeige klicken (Clicked on Ad=1), verbringen im Durchschnitt weniger Zeit auf der Website, sind älter (ca. 40), haben ein geringeres Einkommen und nutzen das Internet deutlich weniger. Aus diesen Informationen lässt sich bereits ein grobes Nutzerprofil ableiten, das auch für Marketing und Vertrieb eines Unternehmens relevant sein könnte, um ihre Maßnahmen auf Basis der Nutzerprofile zu optimieren.

  
__Name des Datensatz:__  Advertising     
__Quelle:__  https://www.kaggle.com/fayomi/advertising  
__Datenersteller:__  fayomi  
__Veröffentlichungsdatum:__  2018  
__Datenformat:__   csv    
__Anzahl der Merkmale:__  10  
__Anzahl der Beobachtungen:__  1000


