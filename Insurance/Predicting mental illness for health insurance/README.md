# Predicting mental illness for health insurance
>see __German Version__ [below](#German_version)

<a href="https://colab.research.google.com/github/AlexRossmann/machine-learning-services/blob/main/Insurance/Predicting%20mental%20illness%20for%20health%20insurance/notebook.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Notebook In Google Colab"/></a>  



## Business Understanding
The globally active insurance company New York Life Insurance Company
headquartered in the USA, serves private and business customers. The main area of business is the provision of physical health insurance in the sense of health insurance 
and preventive health care. In addition to traditional health insurance, this also includes accident insurance, term life insurance and occupational disability insurance. 
In our current society, people are not only exposed to classic physical 
diseases, but increasingly - for example due to overload at work or 
mental illnesses - for example, due to overloads at work or stress. The 
awareness of this type of illness and its classification as an "illness" has not yet penetrated 
has not yet penetrated all areas of society. 
For the insurance company New York Life Insurance Company, it therefore makes sense to 
to expand its business area and insure not only physical but also mental illnesses in the future, 
but also mental illness. In order to initially 
costs, the company does not create its own survey, but instead uses existing data (OSMI). 
existing data (OSMI Mental Health in Tech Survey 2016, 2020).   

__Corporation:__   New York Life Insurance Company  
__Industry:__   Insurance  
__Area of Application:__  Health insurance and preventive health care; accident insurance, term life insurance and occupational disability insurance   
__Business Objective:__  determine which of your customers are more likely to suffer from mental illness now or in the future.     
__Description:__  Which group of people, determined by age, gender, previous illness and job characteristics, has to pay a higher insurance premium in proportion. So that, in the event of a general claim and loss of working hours, sufficient coverage is guaranteed for the insurance to be able to finance additional treatment costs incurred for mental illnesses?  

## Data Understanding

__Name of Dataset:__    Mental Health in Tech Survey  
__Source:__  https://www.kaggle.com/osmi/mental-health-in-tech-survey/data  
__Data Creator/Publisher:__  OSMI Mental Health in Tech Survey 2016, 2020  
__Date of Publication:__  2016-11-03  
__Data Type:__   csv  
__Description of Data Frame:__  This dataset is from a 2014 survey that measures attitudes towards mental health and frequency of mental health disorders in the tech workplace.
__Number of Features:__  27  
__Number of Observations:__  1259  
__Location parameter:__  
__Distribution parameter:__  
__Correlation Analysis:__  

| Feature  | Data Type|
|-----|------|
|Timestamp                |   str [ example: "2014-08-27 15:22:50" ]  |
|Age                      |   int64  |
|Gender                   |   str [ example: "Male" ]  |
|Country                  |   str [ example: "United States" ]  |
|state                    |   str [ example: "OR" ]  |
|self_employed            |   str {"Yes"; "No"; "IL"}  |
|family_history           |   str {"No"; "Yes"}  |
|treatment                |   str {"Yes"; "No"}  |
|work_interfere           |   str {"Often"; "Rarely"; "Never"; "Sometimes"; "Yes"}  |
|no_employees             |   str {"6-25"; "More than 1000"; "26-100"; "100-500"; "1-5"; "500-1000"; "Often"; "Sometimes"}  |
|remote_work              |   str {"No"; "Yes"; "1-5"; "6-25"}  |
|tech_company             |   str {"Yes"; "No"}  |
|benefits                 |   str {"Yes"; "Don't know"; "No"}  |
|care_options             |   str {"Not sure"; "No"; "Yes"; "Don't know"}  |
|wellness_program         |   str {"No"; "Don't know"; "Yes"}  |
|seek_help                |   str {"Yes"; "Don't know"; "No"}  |
|anonymity                |   str {"Yes"; "Don't know"; "No"}  |
|leave                    |   str {"Somewhat easy"; "Don't know"; "Somewhat difficult"; "Very difficult"; "Very easy"; "Yes"}  |
|mental_health_consequence|   str {"No"; "Maybe"; "Yes"; "Very easy"; "Don't know"}  |
|phys_health_consequence  |   str {"No"; "Yes"; "Maybe"}  |
|coworkers                |   str {"Some of them"; "No"; "Yes"; "Maybe"}  |
|supervisor               |   str {"Yes"; "No"; "Some of them"}  |
|mental_health_interview  |   str {"No"; "Yes"; "Maybe"}  |
|phys_health_interview    |   str {"Maybe"; "No"; "Yes"}  |
|mental_vs_physical       |   str {"Yes"; "Don't know"; "No"; "Maybe"}  |
|obs_consequence          |   str {"No"; "Yes"; "Don't know"}  |
|comments;;;;             |   str [ example: "NA;;;;" ]  |

## Data Preparation

__Dimensionality Reduction:__  the columns 'Timestamp','state','comments;;;;' get dropped  
__Outlier:__  outliers in age get deleted  
__Missing Data:__  missing data in "self_employed" get filled with   "No". "work_interfere" gets dropped due to missing data  
__Data Conversion:__  42 different gender names get sorted into male and female  
all sting features get converted to (one-hot encoded) dummy variables

## Modelling and Evaluation

__Algorithms:__  decision tree, logistic regression, Random Forest  
__Hyperparameter:__   test for different tree depth for the decision tree  
__Data Split:__  train test split  80 / 20  
__Model Description:__  this model predicts how likely someone is to have some kind of mental illness ( like burnout)  
__Evaluation Metrics:__  

|model | accuracy |
|------|---------|
|decision tree| 73 % |
|Random Forest|   59 %     |
|logistic regression|   72 %  |

## Deployment

__Target Group:__  insurance   
__Benefits:__  decline candidates with a high likelihood of mental illness  
__Integration:__  this model could be integrated into the standard admissions process for new customers  
  
<a id="German_version"></a> 

# Vorhersage psychischer Krankheiten f??r Krankenversicherung (Deutschsprachige Version)  

## Gesch??ftsverst??ndnis
Das weltweit agierende Versicherungsunternehmen New York Life Insurance Company
mit Hauptsitz in den USA betreut Privat- und Gesch??ftskunden. Der Hauptgesch??ftsbereich liegt in der Absicherung der leiblichen Gesundheit im Sinne von Krankenkassen 
und gesundheitlicher Vorsorge. Dazu geh??ren neben der klassischen Krankenversicherung auch Unfallversicherungen, Risikolebensversicherungen und Berufsunf??higkeitsversicherungen. 
In unserer aktuellen Gesellschaft ist der Mensch nicht nur klassischen k??rperlichen 
Erkrankungen ausgesetzt, sondern zunehmend kommen ??? beispielsweise durch 
??berlastungen am Arbeitsplatz oder Stress ??? psychische Erkrankungen hinzu. Das 
Bewusstsein f??r diese Art von Erkrankung und die Klassifikation als ???Krankheit??? 
durchdringt jedoch noch nicht alle gesellschaftlichen Bereiche. 
F??r das Versicherungsunternehmen New York Life Insurance Company bietet es sich 
daher an, den Gesch??ftsbereich zu erweitern und zuk??nftig nicht nur k??rperliche, 
sondern auch psychische Erkrankungen zu versichern. Um zun??chst Kosten 
einzusparen, wird keine eigene Umfrage durch das Unternehmen erstellt, sondern auf 
schon bestehende Daten zur??ckgegriffen (OSMI Mental Health in Tech Survey 2016, 
2020). 

__Konzern:__  
__Industrie:__  
__Anwendungsbereich:__  
__Unternehmensziel:__  
__Beschreibung:__  
__L??sung:__  

## Datenverst??ndnis

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


# Vorhersage psychischer Krankheiten f??r Krankenversicherung

## Unternehmensbeschreibung 


## Problem- und Fragestellungen 
Die grundlegende Problem- und Fragestellung gem???? den vorliegenden Informationen 
und Zielsetzung lautet wie folgt: Welche Personengruppe, bestimmt durch Alter, 
Geschlecht, Vorerkrankung und Arbeitsplatzbeschaffenheit, muss im Verh??ltnis einen 
h??heren Versicherungsbeitrag leisten. Damit bei allgemeiner Inanspruchnahme und 
Arbeitsausfall ausreichend Deckung f??r die Versicherung garantiert ist, um zus??tzlich 
entstehende Behandlungskosten f??r psychische Erkrankungen finanzieren zu k??nnen? 
Welche zus??tzlichen Erkenntnisse k??nnen aus dem Datensatzes abgeleitet und dem 
Marketing zug??nglich gemacht werden? Um diese Fragen zu kl??ren, m??ssen die 
vorliegenden Daten zun??chst verstanden und anschlie??end ausgewertet werden. 
