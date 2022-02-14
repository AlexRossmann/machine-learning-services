# Title
>see __German Version__ [below](#German_version)

## Business Understanding

__Corporation:__   
__Industry:__   
__Area of Application:__   
__Business Objective:__   
__Description:__  
__Solution:__  

## Data Understanding

__Name of Dataset:__    
__Source:__  
__Data Creator/Publisher:__  
__Date of Publication:__  
__Data Type:__   
__Description of Data Frame:__  
__Number of Features:__  
__Number of Targets:__  
__Number of Observations:__  
__Location parameter:__  
__Distribution parameter:__  
__Correlation Analysis:__  

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

__Dimensionality Reduction:__  
__Outlier:__  
__Missing Data:__  
__Unbalanced Data:__  
__Data Conversion:__  
__Distribution Function:__  
__Feature Scaling:__  
__Multicollinearity:__  

## Modelling and Evaluation

__Algorithms:__  
__Hyperparameter:__   optimierung der Trainingsrate / Batch size, ...    
__Output:__  
__Data Split:__  train test split  
__Model Description:__  
__Evaluation Metrics:__  
__Additional Information:__  

## Deployment

__Service:__  
__Target Group:__  
__Benefits:__  
__Integration:__  

<a id="German_version"></a> 

# Titel (Deutschsprachige Version)  

## Geschäftsverständnis

__Konzern:__  
__Industrie:__  
__Anwendungsbereich:__  
__Unternehmensziel:__  
__Beschreibung:__  
__Lösung:__  

## Datenverständnis

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
