# Sales Forecast for retail store
>see __German Version__ [below](#German_version)

<a href="https://colab.research.google.com/github/AlexRossmann/ml-services/blob/main/Forecast/Sales%20Forecast%20for%20retail%20store/notebook.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Notebook In Google Colab"/></a>  



## Business Understanding

__Corporation:__ na     
__Industry:__ Retail  
__Area of Application:__ Sales 
__Business Objective:__ Sales forecasting under the influence of certain factors.      
__Description:__ Retail needs high sales and just-in-time delivery of products to be successful. Therefore, forecasts are needed on which stores in which departments make how much sales per week.     
__Solution:__ na    

## Data Understanding

__Data Frame:__ Stores, Train, Features       
__Source:__ Kaggle, https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting/data     
__Data Creator:__ Walmart        
__Date of Publication:__ 2014       
__Data Type:__ CSV    
__Description of Data Frame:__ The data used for the notebook is divided into three files. They contain different features and the common attribute stores.     
__Number of Features:__ in stores data = 3, in train data = 5, in features data = 12      
__Number of Targets:__     
__Data Type per Feature:__       

Stores.csv: Store(Integer), Type(Object), size(Integer)   

Train.csv: Store(Integer), dept(Integer), date(Integer), weekly_sales(Float), IsHoliday(Boolean)   

Features.csv: Store(Integer), data(Object), temperature(Float), fuel_price(float), MarkDown1(Float), MarkDown2(Float), Markdown3(Float), Markdown4(Float), Markdown5(Float), CPI(float), Unemployment(float), IsHoliday(boolean)    

__Data Type per Target:__ float     
__Number of Observations:__ in stores data = 45, in train data = 421570, in features data = 8190     
__Location parameter:__         
__Distribution parameter:__         
__Correlation Analysis:__ High correlation between Year and Fuel_price     

## Data Preparation

__Dimensionality Reduction:__ Attributes that do not add value or are not significant removed     
__Outlier:__     
__Missing Data:__ rows with missing data are removed      
__Unbalanced Data:__     
__Data Conversion:__ Coding of the categorical features and Dummy variables are created        
__Distribution Function:__      

__Feature Scaling:__ StandardScaler   
__Multicollinearity:__     

## Modelling and Evaluation  

__Algorithms:__ Linear multiple regression, random forest regressor       
__Hyperparameter:__      
__Output:__ supervised learning, regression    
__Data Split:__ 80% train data, 20% test data        
__Model Description:__ The three data sets train, store and features are linked via the common attribute "store". This creates a new file. From this file 80% are used for training and the rest for testing. After several pre-processing steps the classification is done first with linear multiple regression and then with random forest regressor. With the second model better results are achieved.       

__Evaluation Metrics Linear multiple regression:__ R^2 = 0,358    
__Evaluation Metrics random forest regressor:__ R^2 = 0,96987    

__Additional Information:__       

## Deployment

__Service:__    
__Target Group:__ Retail        
__Benefits:__ Just-in-time delivery possible, sales planning/forecasting         
__Integration:__    
- Forecast of Weekly_Sales data per store
- Forecast of Weekly_Sales data per department
- Aggregations can also be used to forecast total sales for a year        

<a id="German_version"></a> 

# Sales Forecast  (Deutschsprachige Version)  

## Geschäftsverständnis

__Unternehmen:__ na     
__Branche:__ Einzelhandel  
__Anwendungsbereich:__ Vertrieb  
__Unternehmensziel:__ Absatzprognose unter dem Einfluss bestimmter Faktoren.      
__Beschreibung:__ Um erfolgreich zu sein, benötigt der Einzelhandel hohe Umsätze und eine Just-in-time-Lieferung der Produkte. Daher werden Prognosen darüber benötigt, welche Filialen in welchen Abteilungen wie viel Umsatz pro Woche machen.     
__Lösung:__ na    

## Datenverständnis

__Datenrahmen:__ Filialen, Zug, Merkmale       
__Quelle:__ Kaggle, https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting/data     
__Datenersteller:__ Walmart        
__Datum der Veröffentlichung:__ 2014       
__Datentyp:__ CSV    
__Beschreibung des Datenrahmens:__ Die für das Notizbuch verwendeten Daten sind in drei Dateien unterteilt. Sie enthalten verschiedene Merkmale und die gemeinsamen Attributsspeicher.     
__Anzahl der Merkmale:__ in stores data = 3, in train data = 5, in features data = 12      
__Anzahl der Ziele:__     
__Datentyp pro Merkmal:__       

Stores.csv: Speicher(Ganzzahl), Typ(Objekt), Größe(Ganzzahl)   

Train.csv: Store(Integer), dept(Integer), date(Integer), weekly_sales(Float), IsHoliday(Boolean)   

Features.csv: Store(Integer), data(Object), temperature(Float), fuel_price(float), MarkDown1(Float), MarkDown2(Float), Markdown3(Float), Markdown4(Float), Markdown5(Float), CPI(Float), Unemployment(Float), IsHoliday(boolean)    

__Datentyp pro Ziel:__ float     
__Anzahl der Beobachtungen:__ in stores data = 45, in train data = 421570, in features data = 8190     
__Ort-Parameter:__         
__Verteilungsparameter:__         
__Korrelationsanalyse:__ Hohe Korrelation zwischen Jahr und Kraftstoffpreis     

## Datenaufbereitung

__Dimensionalitätsreduktion:__ Attribute, die keinen Wert hinzufügen oder nicht signifikant sind, entfernt     
__Ausreißer:__     
__Fehlende Daten:__ Zeilen mit fehlenden Daten werden entfernt      
__Unausgewogene Daten:__     
__Datenkonvertierung:__ Kodierung der kategorialen Merkmale und Dummy-Variablen werden erstellt        
__Verteilungsfunktion:__      

__Merkmalsskalierung:__ StandardSkalierer   
__Multikollinearität:__     

## Modellierung und Auswertung  

__Algorithmen:__ Lineare multiple Regression, Random Forest Regressor       
__Hyperparameter:__      
__Output:__ überwachtes Lernen, Regression    
__Datenaufteilung:__ 80% Trainingsdaten, 20% Testdaten        
__Modellbeschreibung:__ Die drei Datensätze train, store und features sind über das gemeinsame Attribut "store" verknüpft. Dadurch wird eine neue Datei erstellt. Von dieser Datei werden 80 % zum Trainieren und der Rest zum Testen verwendet. Nach mehreren Vorverarbeitungsschritten erfolgt die Klassifizierung zunächst mit linearer multipler Regression und dann mit Random Forest Regressor. Mit dem zweiten Modell werden bessere Ergebnisse erzielt.       

__Auswertung Metriken Lineare multiple Regression:__ R^2 = 0,358    
__Auswertungsmetrik Zufallsforstregressor:__ R^2 = 0,96987    

__Zusätzliche Informationen:__       

## Einsatz

__Dienstleistung:__    
__Zielgruppe:__ Einzelhandel        
__Nutzen:__ Just-in-time-Lieferung möglich, Absatzplanung/Vorhersage         
__Integration:__    
- Prognose der Weekly_Sales-Daten pro Filiale
- Prognose der Wöchentlichen_Absatzdaten pro Abteilung
- Aggregationen können auch zur Prognose des Gesamtumsatzes für ein Jahr verwendet werden   
