# Flight delays prediction
>see __German Version__ [below](#German_version)

<a href="https://colab.research.google.com/github/AlexRossmann/machine-learning-services/blob/main/Tourism/flight%20delay%20prediction/notebook.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Notebook In Google Colab"/></a>  



## Business Understanding

Flight delays have become a major problem for air traffic systems around the world. The aviation industry is constantly suffering from the economic losses associated with flight delays. According to the United States Bureau of Transportation Statistics (BTS), in 2018, more than 20% of U.S. flights were delayed. These delays have a serious economic impact in the United States, amounting to $40.7 billion per year. Passengers suffer lost time, missed business opportunities or leisure activities, and airlines that attempt to compensate for delays cause additional fuel consumption and a greater negative impact on the environment. impact on the environment. To reduce the negative economic and environmental impacts of unexpected flight delays, and to meet the increasing demand for air travel with increasing flight delays. accurate forecasting of flight delays at airports is needed.

  
__Corporation:__   None    
__Industry:__   Airlines    
__Area of Application:__  Airlines Prediction    
__Business Objective:__   This use case includes the prediction of a possible flight delay of different airlines at American airpots. This is how an estimation of a flight delay can be done 

## Data Understanding

The first problem is already the data set. The problem here is that
Excel can display a maximum of 1,048,576 rows and 16,384 columns. The data set
data set has seven times more rows than Excel can display.
Therefore, only a text editor, database application like MS Access
or via Python for a complete data exploration.


  
__Name of Dataset:__  Flight delay 
  
__Source:__  Kaggle, https://www.kaggle.com/usdot/flight-delays
  
__Data Creator/Publisher:__  Department of Transportation
  
__Date of Publication:__  2015
  
__Data Type:__   csv  
  
__Number of Features:__  31  
  
__Number of Observations:__  5819079  

Just some of the 31 features listed below  

| Feature  | Data Type|
|-----|------|
|YEAR                                |   int64 |
|MONTH                               |   int64 |
|DAY                                 |   int64 |
|DAY_OF_WEEK                         |   int64 |
|AIRLINE                             |   object|
|FLIGHT_NUMBER                       |   int64 |
|TAIL_NUMBER                         |   object|
|ORIGIN_AIRPORT                      |   object|
|DESTINATION_AIRPORT                 |   object|
|SCHEDULED_DEPARTURE                 |   int64 |
|DEPARTURE_TIME                      |   float64|
|DEPARTURE_DELAY                     |   float64|
|TAXI_OUT                            |   float64|
|WHEELS_OFF                          |   float64|
|SCHEDULED_TIME                      |   float64|
|ELAPSED_TIME                        |   float64|
|AIR_TIME                            |   float64|
|DISTANCE                            |   int64  |
|WHEELS_ON                           |   float64|
|TAXI_IN                             |   float64|
|SCHEDULED_ARRIVAL                   |   float64|
|ARRIVAL_TIME                        |   float64|
|ARRIVAL_DELAY                       |   float64|
|DIVERTED                            |   int64  |
|CANCELLED                           |   int64  |
|CANCELLATION_REASON                 |   object |
|AIR_SYSTEM_DELAY                    |   float64|
|SECURITY_DELAY                      |   float64|
|AIRLINE_DELAY                       |   float64|
|LATE_AIRCRAFT_DELAY                 |   float64|
|WEATHER_DELAY                       |   float64|


--> 
## Data Preparation

At the beginning, all packages needed for the project were loaded via Jupyter Notebook
was loaded. Then, the flights data.csv file was read in and some details were
such as types of variables in the dataframe and the set of null values for each variable.
variable were output. Each entry in the flights data.csv file represents one flight in 2019.
can be inferred that more than 7,400,000 flights were recorded in 2019.
These flights are described using 31 variables.

## Modelling and Evaluation
  
__Algorithms:__  Logistische Regression; Polynomial regression   
__Output:__  Flight delay  


## Deployment
  
__Target Group:__  Airlines   
__Benefits:__  Apart from the financial losses incurred by the industry, flight delays also represent a negative
also damage the reputation of airlines and reduce their reliability.reliability. It causes various sustainability problems, such as the Increase in fuel consumption and gas emissions. The analysis carried out here
analysis not only predicts delays based on the data available to date, but alsoavailable data, but also gives a statistical description of the Airlines, their ranking based on their on-time performance and
delays in terms of time, with the top performers in terms of delays can be made immediately visible


  


<a id="German_version"></a> 

# Titel (Deutschsprachige Version)  

## Geschäftsverständnis
Flugverspätungen sind zu einem großen Problem für die Luftverkehrssysteme in aller Welt geworden. Die Luftfahrtindustrie leidet ständig unter den wirtschaftlichen Verlusten, die mit Flugverspätungen verbunden sind. Nach Angaben des United States Bureau of Transportation Statistics (BTS) waren im Jahr 2018 mehr als 20 % der Flüge in den USA verspätet. Diese Verspätungen haben schwerwiegende wirtschaftliche Auswirkungen in den Vereinigten Staaten, die sich auf 40,7 Milliarden US-Dollar pro Jahr belaufen. Die Passagiere leiden unter Zeitverlust, verpassten Geschäftsmöglichkeiten oder Freizeitaktivitäten, und Fluggesellschaften, die versuchen, Verspätungen zu kompensieren, verursachen zusätzlichen Treibstoffverbrauch und größere negative Auswirkungen auf die Umwelt. Um die negativen wirtschaftlichen und ökologischen Auswirkungen unerwarteter Flugverspätungen zu verringern und die steigende Nachfrage nach Flugreisen mit zunehmenden Flugverspätungen zu befriedigen, ist eine genaue Vorhersage von Flugverspätungen auf Flughäfen erforderlich.


  
__Konzern:__  BTS  
__Industrie:__  Airlines  
__Anwendungsbereich:__  Fluggesellschaften   
__Lösung:__  Vorhersage von Flugverspätungen

## Datenverständnis

Die erste Problematik stellt bereits der Datensatz dar. Die Problematik hierbei ist, dass
Excel maximal 1.048.576 Zeilen und 16.384 Spalten darstellen kann. Der hier vorliegende Datensatz besitzt sieben-mal mehr Zeilen als Excel somit darstellen kann. Dadurch kann nur durch einen Texteditor, Datenbankanwendung wie z.B. MS Access oder über Python eine vollständige Datenexploration erfolgen.

  
__Name des Datensatz:__  Flight delay   
__Quelle:__  https://www.kaggle.com/usdot/flight-delays   
__Datenersteller:__   Department of Transportation  
__Veröffentlichungsdatum:__  2015  
__Datenformat:__   csv    
__Anzahl der Merkmale:__  31  
__Anzahl der Beobachtungen:__  5819079

## Datenaufbereitung
  Zu Beginn wurden alle für das Projekt benötigten Pakete über Jupyter Notebook geladen. Dann wurde die Datei flights data.csv eingelesen und einige Details wie die Typen der Variablen im Datenrahmen und die Menge der Nullwerte für jede Variable ausgegeben. Jeder Eintrag in der Datei flights data.csv steht für einen Flug im Jahr 2019. Daraus lässt sich ableiten, dass im Jahr 2019 mehr als 7.400.000 Flüge erfasst wurden. Diese Flüge werden durch 31 Variablen beschrieben.



## Modellierung und Auswertung
  
__Algorithmen:__  Logistische Regression; Polynomial regression 
  
__Datenaufteilung:__  train test split  


## Bereitstellung
  
__Service:__  Vorhersage von Flugverspätungen 
  
__Zielgruppe:__  Airlines

