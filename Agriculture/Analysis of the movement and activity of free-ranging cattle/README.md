# Analysis of the movement and activity of free-ranging cattle
>see __German Version__ [below](#German_version)

<a href="https://colab.research.google.com/github/AlexRossmann/machine-learning-services/blob/main/Agriculture/Analysis%20of%20the%20movement%20and%20activity%20of%20free-ranging%20cattle/notebook.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Notebook In Google Colab"/></a>  



## Business Understanding
Farmers are coming under increasing economic pressure. For example, the 
expensive logistical problems due to the corona pandemic. At the same time
more and more consumers are placing higher demands on animal welfare. 
animal husbandry. These market conditions appear problematic for farmers, 
as the latter aspect is naturally associated with certain costs and necessitates a general rethink. 
general rethinking is necessary.
New technologies, such as artificial intelligence and the use of sensors, can make 
and the use of sensors, processes can be made more efficient and at the same time the 
Animal welfare requirements can be better met.
One problem farmers face is that they cannot target or individually 
care for their animals. The knowledge of which activities, for example, have a particular 
have a particular influence on milk production or meat quality, for example, cannot be 
be comprehensively recorded. Therefore, no targeted measures for the 
promotion of certain activities is possible. Conceivable measures would be
motivating individual animals to move more or optimizing breeding. 
breeding. So far, however, it is difficult to create continuous activity profiles of the animals. 
create.
Another problem for farmers is that it is often not possible to detect changes in the
changes in the health status of individual animals is often not possible.
Although regular monitoring of the condition of a herd is a legal requirement, especially on larger farms it is 
legal requirement, however, especially in larger farms, due to the large 
due to the large number of animals, health changes can only be detected late.
be detected. Often, in case of illness, the only treatment available is antibiotics or other 
other expensive drugs. Conscientious behavioral changes can, however 
provide initial indications at an early stage. Healthy cattle, for example, normally move 
normally move quite a lot and reduce their activity when they develop the first 
signs of disease develop. Early detection of this 
reduction in movement would be of great importance to a farmer.
Healthy Cattle plans, to address the above issues, to use an 
activity classification for activity profiling and early detection of disease.
Detection of disease. The hypothesis is that with the help of 
typical sensors of a smartphone and the use of a machine 
Learning algorithm, the activities can be classified.
For the planned solution, Healthy Cattle would first like to test whether, with the help of 
sensors of a smartphone can classify activities with sufficient accuracy. 
of activities is possible. To be able to test this as cost-effectively as possible, 
the first prototype will not be based on the company's own data, but on data from a similar 
data available on the Internet from a similar setup.

__Corporation:__   None  
__Industry:__   Agriculture  
__Area of Application:__  Cattle Farming   
__Business Objective:__   Identify Activities of Cows on the field  

## Data Understanding
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.
In one experiment, 30 subjects performed a fixed movement sequence with a 
Smartphone to perform a fixed sequence of movements. In the process 
the linear acceleration and angular velocity signals on three axes in each case. 
angular velocity signals were recorded on three axes in each case. The individual 
data points were classified or labeled according to activity. Through 
filtering methods, these were then freed from noise and further
and further time- and frequency-related features were extracted. From these 
features such as mean, standard deviation, minimum, maximum, median, etc. were calculated. 
maximum value, median, etc.  
<!-- The underlying machine learning problem is to be classified in the area of supervised learning. 
Learning, since learning is done on labeled data. Each data point 
in the dataset has a set of features - calculated from the sensor values - and a target - the activity class.
The available dataset consists of 10299 observations 
(Observations). There are no missing values and there are no 
duplicates.
The number of features is very large, which makes a comprehensive analysis of the individual features very difficult. 
of the individual features is very difficult. A graphical check for 
multicollinearity using the correlation matrix is therefore not useful. A 
Variance Inflation Factor (VIF) shows that a large number of features with a VIF 
with a VIF>10 show a high multicollinearity (see table). A 
multicollinearity has a negative impact on the interpretability of the later 
subsequently created models. -->

__Name of Dataset:__    Human Activity Recognition Using Smartphones Data Set  
__Source:__  https://archive.ics.uci.edu/ml/datasets/human+activity+recognition+using+smartphones  
__Data Creator/Publisher:__  Jorge L. Reyes-Ortiz(1,2), Davide Anguita(1), Alessandro Ghio(1), Luca Oneto(1) and Xavier Parra(2)
1 - Smartlab - Non-Linear Complex Systems Laboratory  
__Date of Publication:__  2012-12-10  
__Data Type:__   csv  
__Number of Features:__  563  
__Number of Observations:__  10299  
__Correlation Analysis:__  most features are very correlated, as they are all derived from two sensors (accelerometer and gyroscope)

Just some of the 564 features listed below  

| Feature  | Data Type|
|-----|------|
|tBodyAcc-mean()-X                   |   float64  |
|tBodyAcc-mean()-Y                   |   float64  |
|tBodyAcc-mean()-Z                   |   float64  |
|tBodyAcc-std()-X                    |   float64  |
|tBodyAcc-std()-Y                    |   float64  |
|tBodyAcc-std()-Z                    |   float64  |
|tBodyAcc-mad()-X                    |   float64  |
|tBodyAcc-mad()-Y                    |   float64  |
|tBodyAcc-mad()-Z                    |   float64  |
|tBodyAcc-max()-X                    |   float64  |
|tBodyAcc-max()-Y                    |   float64  |
|tBodyAcc-max()-Z                    |   float64  |
|tBodyAcc-min()-X                    |   float64  |
|tBodyAcc-min()-Y                    |   float64  |
|tBodyAcc-min()-Z                    |   float64  |
|tBodyAcc-sma()                      |   float64  |
|angle(tBodyAccMean,gravity)         |   float64  |
|fBodyBodyGyroJerkMag-kurtosis()     |   float64  |
|fBodyBodyAccJerkMag-max()           |   float64  |
|fBodyBodyAccJerkMag-energy()        |   float64  |
|fBodyGyro-bandsEnergy()-1,24.2      |   float64  |
|fBodyGyro-bandsEnergy()-25,48.2     |   float64  |
|subject                             |   int64  |
|Activity                            |   str {"STANDING"; "SITTING"; "LAYING"; "WALKING"; "WALKING_DOWNSTAIRS"; "WALKING_UPSTAIRS"}  |


## Data Preparation
__Dimensionality Reduction:__ 1 column with the subject id 'subject'-->only for filtering, must be removed   
__Missing Data:__  no missing data  
__Unbalanced Data:__  Oversampling wwith imblearn.over_sampling.RandomOverSampler  
__Multicollinearity:__  All Features with a VIF over 10 are discarded (522 Features are discarded)  
at the end 39 Features are left  

## Modelling and Evaluation

__Algorithms:__  Logistische Regression; Random Forest; Decision Tree; Support Vector Machine; KNN (K-Nearest-Neighbours)   
__Output:__  is the Person / cow (WALKING, SITTING, LAYING, STANDING)  
__Data Split:__  train test split  
__Evaluation Metrics:__  
| model_type | accuracy_train	|accuracy_test|
|-----|------|---|		
|KNN|	0.874911|	0.791342|
|RandomForest	|1.000000|	0.852140	|
|LogReg |	0.808102|	0.769455	|
|DecisionTree|	1.000000 |	0.653696	|
|SVM |	0.814144|	0.766051	|

## Deployment

__Target Group:__  Cow Farmers  
__Benefits:__  It can be recognized which behavior should be promoted, which animals are "out of line". Also one can be recognized with these data anomalies.  

__Integration:__  Each cow gets a sensor. The sensors communicate wirelessly with a central receiver in the pasture. This sends the data to the cloud. There they are analyzed. Anomalies can be detected in real time, and the farmer receives a notification.  


<a id="German_version"></a> 

# Analyse der Bewegung und Aktivität von freilaufenden Rindern (Deutschsprachige Version)  

## Geschäftsverständnis
Landwirte geraten immer weiter unter wirtschaftlichen Druck. Beispielsweise kam 
es durch die Coronapandemie zu teuren logistischen Problemen. Gleichzeitig
stellen immer mehr Konsumenten höhere Anforderungen an eine artgerechte 
Tierhaltung. Diese Marktbedingungen erscheinen für Landwirte problematisch, 
da letzterer Aspekt natürlich mit gewissen Kosten verbunden ist und ein 
generelles Umdenken notwendig macht.
Durch neue Technologien wie z.B. Künstliche Intelligenz und der Verwendung 
von Sensoren können die Prozesse effizienter gestaltet und gleichzeitig die 
Anforderungen des Tierschutzes besser erfüllt werden.
Ein Problem der Landwirte ist, dass sie ihre Tiere nicht gezielt bzw. individuell 
umsorgen können. Das Wissen darüber, welche Aktivitäten z.B. besonderen 
Einfluss auf die Milchproduktion oder Fleischqualität haben, kann bisher nicht 
umfänglich erfasst werden. Somit sind auch keine gezielten Maßnahmen zur 
Förderung bestimmter Aktivitäten möglich. Denkbare Maßnahmen wären die
gezielte Motivation zu mehr Bewegung einzelner Tiere oder die Optimierung der 
Zucht. Bisher ist es jedoch schwierig kontinuierliche Aktivitätsprofile der Tiere zu 
erstellen.
Ein weiteres Problem der Landwirte ist, dass eine frühzeitige Erkennung von
Veränderungen des Gesundheitszustandes einzelner Tiere oft nicht möglich ist.
Zwar ist die regelmäßige Kontrolle des Zustandes einer Herde rechtlich 
vorgeschrieben, jedoch können gerade in größeren Betrieben auf Grund der 
großen Anzahl an Tieren, gesundheitliche Veränderungen erst spät erkannt
werden. Oft bleibt im Krankheitsfall nur die Behandlung mit Antibiotika oder 
anderen teuren Medikamenten. Gewissen Verhaltensänderungen können jedoch 
frühzeitig erste Hinweise liefern. Gesunde Rinder beispielsweise bewegen sich 
normalerweise recht viel und reduzieren ihre Aktivität, wenn sie erste 
Krankheitszeichen entwickeln. Eine frühe Erkennung dieser 
Bewegungsreduzierung wäre von großer Bedeutung für einen Landwirt.
Healthy Cattle plant, zur Lösung der oben genannten Probleme, eine 
Aktivitätsklassifizierung zur Erstellung von Aktivitätsprofilen und zur frühzeitigen
Erkennung von Krankheiten zu entwickeln. Die Hypothese ist, dass mit Hilfe von 
typischen Sensoren eines Smartphones und der Verwendung eines Machine 
Learning Algorithmus, die Aktivitäten klassifiziert werden können.
Healthy Cattle möchte für die geplante Lösung zunächst testen, ob mit Hilfe von 
typischen Sensoren eines Smartphones eine ausreichend genaue Klassifizierung 
von Aktivitäten möglich ist. Um dies möglichst kostengünstig testen zu können, 
werden für einen ersten Prototypen keine eigenen Daten verwendet, sondern im 
Internet zugängliche Daten aus einem ähnlichen Setup genutzt.  

__Konzern:__  
__Industrie:__  
__Anwendungsbereich:__  
__Unternehmensziel:__  
__Beschreibung:__  
__Lösung:__  

## Datenverständnis
Der Datensatz dieser Hausarbeit stammt von Anguita, Ghio et al. und wurde 
abgerufen von Kaggle.com unter: https://www.kaggle.com/uciml/human-activity-recognition-with-smartphones.
Der Original Datensatz ist auf https://archive.ics.uci.edu/ml/datasets/human+activity+recognition+using+smartphones.
In einem Experiment haben 30 Probanden mit einem auf Hüfthöhe befestigten 
Smartphone einen festgelegten Bewegungsablauf durchgeführt. Dabei wurden 
mit Hilfe der verbauten Sensoren die linearen Beschleunigungs- und 
Winkelgeschwindigkeitssignale auf jeweils drei Achsen erfasst. Die einzelnen 
Datenpunkte wurden je nach Aktivität klassifiziert bzw. gelabelt. Durch 
verschiedene Filterverfahren wurden diese anschließend von Rauschen befreit
und weitere zeit- der frequenzbezogene Features extrahiert. Aus diesen wurden 
weitere Features wie z.B. Mittelwert, Standardabweichung, Minimal- und 
Maximalwert, Median usw. berechnet.
Das zu Grunde gelegte Machine Learning Problem ist in den Bereich Supervised 
Learning einzuordnen, da auf gelabelten Daten gelernt wird. Jeder Datenpunkt 
im Datensatz besitzt eine Reihe von Features - berechnet aus der Sensorwerten - und ein Target - die Aktivitätsklasse.
Der zur Verfügung stehende Datensatz besteht aus 10299 Beobachtungen 
(Observations). Es gibt keine fehlenden Werte und es existieren auch keine 
Duplikate.
Die Anzahl der Features ist sehr groß, was eine umfängliche Analyse der 
einzelnen Features stark erschwert. Eine grafische Überprüfung auf 
Multikollinearität mit Hilfe der Korrelationsmatrix ist deshalb nicht sinnvoll. Eine 
Überprüfung des Variance Inflation Factor (VIF) ergibt, dass sehr viele Features 
mit einem VIF>10 eine hohe Multikollinearität aufweisen (siehe Tabelle). Eine 
hohe Multikollinearität hat negative Auswirkungen auf die Interpretierbarkeit der 
später erstellten Modelle.

__Name des Datensatz:__  
__Quelle:__  
__Datenersteller:__  
__Veröffentlichungsdatum:__  
__Datenformat:__   csv?  
__Beschreibung des Datenrahmens:__  
__Anzahl der Merkmale:__  
__Anzahl der Beobachtungen:__  
__Standortparameter:__  
__Verteilungsparameter:__  
__Korrelationsanalyse:__  


## Datenaufbereitung

__Dimensionsreduktion:__  
__Ausreißer:__  
__Fehlende Daten:__  
__Unausgeglichene Daten:__  
__Datenkonvertierung:__  
__Verteilungsfunktion:__  
__Merkmal skalierung :__  
__Test auf Multikollinearität:__  

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

## Business Understanding


## Data Understanding
