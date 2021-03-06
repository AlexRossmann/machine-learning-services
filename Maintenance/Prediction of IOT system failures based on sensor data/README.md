# Prediction of fire protection system failures based on sensor data
>see __German Version__ [below](#German_version)

<a href="https://colab.research.google.com/github/AlexRossmann/machine-learning-services/blob/main/Maintenance/Prediction%20of%20IOT%20system%20failures%20based%20on%20sensor%20data/notebook.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Notebook In Google Colab"/></a>  



## Business Understanding
Minimax GmbH & Co. KG is a leading global provider of solutions in the 
fire protection sector with annual sales of 1.7 billion euros and approximately 
approximately 9000 employees worldwide. Both in the industrial sector, such as in 
power plants and data centers, as well as in office and administrative buildings.
Minimax supplies tailor-made fire protection systems with, for example 
for example classic sprinkler systems or water mist extinguishing systems. In doing so 
Minimax uses an end - to - end approach when installing its solutions.

Translated with www.DeepL.com/Translator (free version)

  
__Corporation:__   Minimax GmbH & Co. KG    
__Industry:__   Fire protection system    
__Area of Application:__  predictive maintenance      
__Business Objective:__   The question of the case study is to what extent this sensor data can be used for an AI-based 
prediction of failures in a plant and thus to introduce a reactive 
preventive maintenance intervals, a reactive-preventive maintenance interval can be introduced. 
can be introduced, which is based on predictions of an ML model. In concrete terms: How 
time intervals are possible for a component before it enters a defective state. 
into a defective state.

## Data Understanding
  
__Name of Dataset:__    Turbofan Engine Degradation Simulation Data Set    
__Source:__  https://ti.arc.nasa.gov/tech/dash/groups/pcoe/prognostic-data-repository/#turbofan      
__Data Creator/Publisher:__   NASA Ames Prognostics Data Repository    
__Date of Publication:__  2008    
__Data Type:__   txt    
__Description of Data Frame:__  Engine degradation simulation was carried out using C-MAPSS. Four different were sets simulated under different combinations of operational conditions and fault modes. Records several sensor channels to characterize fault evolution. The data set was provided by the Prognostics CoE at NASA Ames.    
__Number of Features:__  26  
__Number of Observations:__  20.631  


| Feature |  Meaning |  Datatype|
|----------|---------------|------------| 
| id       |  Id of the unit in question | int| 
| zyklus   | time in days             | int|
|setting1, ???, setting3 |3 operational settings         | float |
|s1, ???, s21 |21 different sensor data                      | float |

## Data Preparation
  
__Dimensionality Reduction:__  remove the id  
remove 'setting3', 's1', 's5', 's10', 's16', 's18', 's19', as their values are constant    
__Data Conversion:__  calculate the remaining days until failure  
__Feature Scaling:__  scaling of all sensor data by using 

## Modelling and Evaluation
  
__Algorithms:__  Long Short-Term Memory Layer Recurrent Neural Network  (LSTM NN)  
__Hyperparameter:__   the size of the window for the LSTM model is set by manual experimentation  
__Output:__    
__Data Split:__  train test split   80 / 20  
__Model Description:__  the model can predict wether the device is close to failure. It is a binary classification answering the question: Will the device have a failure within 1 day  
__Evaluation Metrics:__  accuracy = 94 %

## Deployment
  
__Service:__  predict wether the device is close to failure  
__Target Group:__  IOT Devices with lots of sensors  
__Benefits:__  predictive maintenance allows you to replace devices before they break down. This can eliminate reduce downtime and save cost.  
__Integration:__  Sensor data is collected on the cloud, as all the IOT devices have internet connectivity. 
The neural Network runs once a day on all the collected data. If the model detects a device, that is close to failure, the service informs a technician.

<a id="German_version"></a> 

# Vorhersage von Ausf??llen einer Brandschutzsystemen auf Basis von Sensordaten (Deutschsprachige Version)  

## Gesch??ftsverst??ndnis
Die Minimax GmbH & Co. KG ist ein weltweit f??hrender Anbieter von L??sungen im 
Brandschutzbereich mit einem j??hrlichen Jahresumsatz von 1,7 Milliarden Euro und 
circa 9000 Mitarbeitern weltweit. Sowohl im industriellen Bereich wie zum Beispiel in 
Automobilwerken, Kraftwerken oder Data Centern, als auch in B??ro- und
Verwaltungsgeb??uden liefert Minimax ma??geschneiderte Brandschutzsysteme mit 
zum Beispiel klassischen Sprinkleranlagen oder Wassernebel-L??schanlagen. Dabei 
nutzt Minimax einen End ??? to ??? End Ansatz bei der Installation ihrer L??sungen.
  
__Konzern:__    
__Industrie:__    
__Anwendungsbereich:__    
__Unternehmensziel:__  Die Fragestellung der Fallstudie ist, inwieweit diese Sensordaten f??r eine AI-basierte 
Vorhersage von Ausf??llen einer Anlage genutzt werden k??nnen und damit statt 
pr??ventiven Wartungsintervallen ein reaktiv-pr??ventiver Wartungsintervall eingef??hrt 
werden kann, welcher auf Vorhersagen eines ML-Modells basiert. Konkret also: Wie 
viele nachfolgende Zeitintervalle sind f??r eine Komponente m??glich, bevor sie sich in 
einen Defektzustand versetzt.   


## Datenverst??ndnis
Der Datensatz, der in dieser Fallstudie verwendet wurde, enth??lt 20.631 Daten, die 
von Datensatz der NASA zu Turbo-Fan-Engines stammen. Dies h??ngt damit 
zusammen, dass eine geringe Verf??gbarkeit von Echtdaten im Bereich Industrial 
Internet of Things vorherrscht, da die meisten Unternehmen ihre Maschinendaten 
geheim halten m??chten. Der genutzte Datensatz enth??lt Sensordaten von 
Triebwerken, sowie St??rungen und, f??r den Testdatensatz, einen Indikator, nach wie 
vielen Intervallen (im Falle Minimax Zeitintervalle) ein Austausch des Triebwerks 
(hier Komponenten) n??tig ist. Dieses Set-Up kann auf den Anwendungsfall, also mit 
der vorhandenen Datenstruktur bei Minimax verglichen werden.    
__Name des Datensatz:__    
__Quelle:__    
__Datenersteller:__    
__Ver??ffentlichungsdatum:__    
__Datenformat:__   csv?    
__Beschreibung des Datenrahmens:__    
__Anzahl der Merkmale:__    
__Anzahl der Beobachtungen:__    
__Standortparameter:__    
__Verteilungsparameter:__    
__Korrelationsanalyse:__  


## Datenaufbereitung
  
__Dimensionsreduktion:__    
__Ausrei??er:__    
__Fehlende Daten:__    
__Unausgeglichene Daten:__    
__Datenkonvertierung:__    
__Verteilungsfunktion:__    
__Merkmal skalierung :__    
__Test auf Multikollinearit??t:__  

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


# Vorhersage von Ausf??llen einer Brandschutzsystemen auf Basis von Sensordaten

## Problemstellung
Mit Hilfe des Inveron Gefahrenmanagementsystem k??nnen die bereits mit Sensoren 
ausgestatteten Anlagen manuell ??berwacht und gesteuert werden, zum Beispiel von 
einem Leitstand aus. Inveron ist dabei eine Software, die alle Sensordaten aus den 
Brandschutzsystemen b??ndelt und visualisiert. Au??erdem k??nnen mit Hilfe von 
Inveron Probealarme ausgel??st werden, oder Alarme zur??ckgesetzt werden. 
Das Inveron Gefahrenmanagementsystem verarbeitet bereits eine Menge 
Sensordaten, die in der lokalen Systemumgebung, zum Beispiel der
Sicherheitszentrale eines Industrieunternehmens genutzt werden. Spezifische
Wartungsintervalle geben Servicetechnikern von Minimax vor, wann eine Anlage zu 
warten ist. 
Inveron kann, neben der ??berwachung von eigenen Sensordaten, auch Fremddaten 
??berwachen. Zum Beispiel k??nnen aufgeschaltete Videokameras zur 
Branddetektierung genutzt werden. Auch Einbruchmeldeanlagen, Anlagen zur 
Zaun??berwachgung oder Torsteuerungsanlagen. Offene Schnittstellen (OPC, 
Modbus, Profibus, BAC-net) erm??glichen eine langfristige Einsetzbarkeit bei 
Austausch von Einzelkomponenten.

## Fragestellung
Die Fragestellung der Fallstudie ist, inwieweit diese Sensordaten f??r eine AI-basierte 
Vorhersage von Ausf??llen einer Anlage genutzt werden k??nnen und damit statt 
pr??ventiven Wartungsintervallen ein reaktiv-pr??ventiver Wartungsintervall eingef??hrt 
werden kann, welcher auf Vorhersagen eines ML-Modells basiert. Konkret also: Wie 
viele nachfolgende Zeitintervalle sind f??r eine Komponente m??glich, bevor sie sich in 
einen Defektzustand versetzt.
Predictive Maintainance soll dabei helfen, den Zustand von in Betrieb befindlichen 
Anlagen zu bestimmen, um abzusch??tzen, wann eine Wartung durchgef??hrt werden 
sollte. Dieser Ansatz verspricht Kosteneinsparungen gegen??ber der routinem????igen 
oder zeitbasierten vorbeugenden Instandhaltung, da Ma??nahmen nur dann
durchgef??hrt werden, wenn sie gerechtfertigt sind. Es handelt sich also um eine 
zustandsorientierte Wartung, die auf der Grundlage von Sch??tzungen des 
Degradationszustands einer Komponente durchgef??hrt wird.

## Data Understanding
Im Data Understanding wird der Rohdatensatz das erste Mal untersucht. Hierbei soll 
der Data Scientist ein ???Gef??hl??? f??r die Daten bekommen und sehen, inwieweit die 
Daten f??r die weitere Analyse verwendbar sind. Besonderheiten der Daten k??nnen 
aufgezeigt werden und eventuelle Probleme mit der Datenqualit??t erkannt werden, 
um sie im n??chsten Schritt, der Data Preparation, zu beheben. 
Die Daten bestehen aus drei Datens??tzen, PM_train, PM_test und PM_truth. Diese 
haben jeweils verschiedene Attribute, wie in Tabelle 1 dargestellt. Die Attributnamen 
wurden im Nachhinein vom Autor dieser Arbeit den Tabellen hinzugef??gt, da diese 
urspr??nglich nicht vorhanden waren.


| Attribute |  Bedeutung |  Datentyp|
|----------|---------------|------------| 
| id       |  Nummer des Bauteils, welches im Geb??ude verbaut ist | int| 
| zyklus   | Zeit, in Zyklen (1 Zyklus = 1 Tag)                   | int|
|setting1, ???, setting3 | 3 operationale Einstellungen              | float |
|s1, ???, s21 | 21 Sensor Daten                                      | float |


Wie in der Tabelle  sichtbar geben die Daten Zust??nde von Bauteilen zu einem 
bestimmten Zykluszeitpunkt wieder. ??bertragen auf Minimax bedeutet dies, dass die 
id ein Gesamtbauteil darstellt, also ein Anlagenteil welches als Ganzes gewechselt 
werden kann, beispielsweise ein Feuermelder. Verschiedene Sensordaten, in diesem 
Falle 21 verschiedene, k??nnen Einflussindikatoren sein, wann ein Anlagenteil aufh??rt 
zu funktionieren. Genau das soll in dieser Fallstudie herausgefunden werden. In der 
Tabelle PM_truth befindet sich, nach id geordnet, die Zahl der Zyklen nach denen ein 
Bauteil nicht mehr funktioniert.
