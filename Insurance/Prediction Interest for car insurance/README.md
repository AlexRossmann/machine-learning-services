# Prediction of interest in car insurance
>see __German Version__ [below](#German_version)

<a href="https://colab.research.google.com/github/AlexRossmann/machine-learning-services/blob/main/Insurance/Prediction%20Interest%20for%20car%20insurance/notebook.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Notebook In Google Colab"/></a>  



## Business Understanding

__Corporation:__ na    
__Industry:__ Insurance  
__Area of Application:__ CRM, Marketing    
__Business Objective:__ Prediction of customers who are interested in car insurance  
__Description:__ With this service it should be possible to actively refer regular customers to an offer  
__Solution:__ Random address without estimation   

## Data Understanding

__Name of Dataset:__ Janatahack Cross-sell Prediction      
__Source:__ Kaggle, https://www.kaggle.com/jassican/janatahack-crosssell-prediction     
__Data Creator/Publisher:__ na   
__Date of Publication:__ na  
__Data Type:__ CSV    
__Description of Data Frame:__ The data set consists of two files, train.csv and test.csv. Only train was used, because in test an important column for the analysis is missing. The train file consists of 381,109 rows and 12 columns.  
__Number of Features:__ 12   
__Number of Targets:__ 1   
__Number of Observations:__ 381109  
__Location parameter:__ na  
__Distribution parameter:__ na   
__Correlation Analysis:__ Mean correlation analysis between the attributes "age" and "policy_sales_channel".   

<!-- //Tabelle
def attribute_description(data):
    longestColumnName = len(max(np.array(data.columns), key=len))
    print("| Feature  | Data Type|")
    print("|-----|------|")
    for col in data.columns:
        description = ''
        col_dropna = data[col].dropna()
        example = col_dropna.sample(1).values[0]
        if type(example) == str:
            description = 'str '
            if len(col_dropna.unique()) < 10:
                description += '{'
                description += '; '.join([ f'"{name}"' for name in col_dropna.unique()])
                description += '}'
            else:
                description += '[ example: "'+ example + '" ]'
        elif (type(example) == np.int32) and (len(col_dropna.unique()) < 10) :
            description += 'dummy int32 {'
            description += '; '.join([ f'{name}' for name in sorted(col_dropna.unique())])
            description += '}'
        else:
            try:
                description = example.dtype
            except:
                 description = type(example)
        print("|" + col.ljust(longestColumnName)+ f'|   {description}  |')
 
attribute_description(data) -->

## Data Preparation

__Dimensionality Reduction:__ Column id is deleted, because it is not required   
__Outlier:__ removed   
__Missing Data:__      
__Unbalanced Data:__ yes       
__Data Conversion:__ Dummy variables created, discretization   
__Distribution Function:__ na  
__Feature Scaling:__ with StandardScaler    
__Multicollinearity:__      

## Modelling and Evaluation

__Algorithms:__ logistic regression    
__Hyperparameter:__ Model optimized by using thresholds      
__Output:__ Supervised learning, Classification  
__Data Split:__ 80% train, 20% test     
__Model Description:__ Qualitative model description: Since no linearity was found, a non-linear model is used, the Logistic Regression. The model works with categorical target values (dependent variable). It is used to predict "yes"/"no" (0/1) decisions. With the help of the value P>|z|, statistically non-significant variables can be read out. The features that have a value greater than 0.05 are removed. By reading out and visualizing the weighting of features, insight could be gained into which factors speak for interest and which against. There is more interest if the existing customer has had an accident. If the customer already has a policy, he or she does not consider it necessary to take out a new car insurance policy. Subsequently, an optimization was carried out with the help of the threshold values. At the expense of accuracy, a threshold of 0.25 was then selected, since a recall value of 0.8216 was achieved here with an acceptable accuracy of 0.7338.    
__Evaluation Metrics:__ Accuracy 0.73, Recall 0.82, Precision 0.29    
__Additional Information:__     

## Deployment
    
__Target Group:__ Insurance Sales    
__Benefits:__ Cost saving, time saving, customer acquisition, sales increase    
__Integration:__      

<a id="German_version"></a> 

# Prediction of interest in car insurance (Deutschsprachige Version)  

## Geschäftsverständnis

__Konzern:__ na    
__Industrie:__ Versicherung  
__Anwendungsbereich:__ CRM, Marketing    
__Unternehmensziel:__  Vorhersage von Kunden, die interessiert an einer Kfz-Versicherung sind  
__Beschreibung:__ Mit diesem Service soll es möglich sein, Stammkunden aktiv auf ein Angebot hinzuweisen  
__Lösung:__ Zufällige Ansprache ohne Abschätzung   

## Datenverständnis

__Name des Datensatz:__ Janatahack Cross-sell Prediction   
__Quelle:__ Kaggle, https://www.kaggle.com/jassican/janatahack-crosssell-prediction    
__Datenersteller:__ na    
__Veröffentlichungsdatum:__ na      
__Datenformat:__ csv      
__Beschreibung des Datenrahmens:__ Der Datensatz besteht aus zwei Dateien, Train.csv und test.csv. Genutzt wurde nur train, da in test eine für die Analyse wichtige Spalte fehlt. Die train Datei besteht aus 381.109 Zeilen und 12 Spalten.   
__Anzahl der Merkmale:__ 12    
__Anzahl der Beobachtungen:__ 381109    
__Standortparameter:__ na    
__Verteilungsparameter:__ na   
__Korrelationsanalyse:__ mittlere Korrelation zwischen den Attributen "age" und "policy_sales_channel" erkennbar    

## Datenaufbereitung

__Dimensionsreduktion:__ Spalte id wird gelöscht, da diese nicht erforderlich ist   
__Ausreißer:__ entfernt    
__Fehlende Daten:__      
__Unausgeglichene Daten:__ ja   
__Datenkonvertierung:__ Dummy-Variablen erstellt, Diskretisierung    
__Verteilungsfunktion:__ na    
__Merkmal skalierung :__ StandardScaler    
__Test auf Multikollinearität:__       

## Modellierung und Auswertung

__Algorithmen:__ Logistische Regression     
__Hyperparameter:__ Modell durch Verwendung von Schwellenwerten optimiert    
__Ausgabe:__ Supervised learning, Classification   
__Datenaufteilung:__ 80% Training, 20% Test     
__Modellbeschreibung:__ Qualitative Modellbeschreibung: Da keine Linearität festgestellt wurde, wird mit einem nicht-linearen Modell gearbeitet, die Logistische Regression. Das Modell arbeitet mit kategorischen Zielwerten (abhängige Variable). Sie wird dafür verwendet „ja“/ „nein“ (0/1) Entscheidungen vorherzusagen. Mit der Hilfe des Wert P>|z| lassen sich statistisch nicht signifikante Variablen auslesen. Die Features, welche einen Wert größer 0,05 haben, werden entfernt. Durch das Auslesen und Visualisieren der Gewichtung von Features konnte ein Einblick darüber gegeben werden, welche Faktoren für ein Interesse sprechen und welche dagegen. Ein Interesse besteht verstärkt dann, wenn der Bestandskunde einen Unfall hatte. Ist der Kunde schon bereits im Besitz einer Police, so hält er es selbst nicht für notwendig eine neue Kfz-Versicherung abschließen zu wollen. Im Anschluss dazu wurde eine Optimierung mit Hilfe der Schwellenwerte vorgenommen. Auf Kosten der Genauigkeit wurde daraufhin ein Threshold von 0,25 ausgewählt, da hier ein Recall-Wert von 0,8216 erreicht wurde bei einer akzeptablen Genauigkeit von 0,7338.     
__Bewertungsmetriken:__ Accuracy 0.73, Recall 0.82, Precision 0.29     
__Weitere Informationen:__      

## Bereitstellung

__Zielgruppe:__ Versicherungen     
__Leistungen:__ Kostenersparnis, Zeitersparnis, Kundengewinnung, Umsatzsteigerung    
__Integration:__     

