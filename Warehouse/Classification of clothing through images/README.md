# Classification of clothing through images
>see __German Version__ [below](#German_version)

<a href="https://colab.research.google.com/github/AlexRossmann/machine-learning-services/blob/main/Warehouse/Classification%20of%20clothing%20through%20images/notebook.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Notebook In Google Colab"/></a>  



## Business Understanding

__Corporation:__ na  
__Industry:__ Fashion  
__Area of Application:__ Logistics  
__Business Objective:__ Identification of clothing through images.    
__Description:__ Returned items must be able to be restocked and sold. For this purpose, the goods must be identified and labeled. An ML service is to be used to support this process.   
__Solution:__ Manual recognition by humans and manual labeling of clothing.  

## Data Understanding

__Data Frame:__ fashion-mnist_test     
__Source:__ Kaggle, https://github.com/zalandoresearch/fashion-mnist  
__Data Creator:__ Zalando   
__Date of Publication:__ 2017   
__Data Type:__ CSV  
__Description of Data Frame:__ The dataset consists of item images from the Zalando company. In total 60,000 training images and 10,000 test images are included, which were scaled to 28x28 pixels and converted to a grayscale image.   
__Number of Features:__ 28x28 pixel + label    
__Number of Targets:__ 1  
__Data Type per Feature:__ Integer  
__Data Type per Target:__ Integer    
__Number of Observations:__ 70.000  
__Location parameter:__ na   
__Distribution parameter:__ na  
__Correlation Analysis:__ na  

## Data Preparation  

__Dimensionality Reduction:__   
__Outlier:__   
__Missing Data:__     
__Unbalanced Data:__      
__Data Conversion:__ Scaling to grayscale color with a value between 0-1, convert the image shape from 784 to 28x28 (only if loaded as CSV with 784 columns), Convert the labels to categorial data (10 Categories)      
__Distribution Function:__ na  

__Feature Scaling:__    
__Multicollinearity:__    

## Modelling and Evaluation

__Algorithms:__  Convolutional Neural Network (CNN)  
__Hyperparameter:__ The first and second convolutional layer is parameterized with 32 filters and a kernel size of 3 and no padding   
__Output:__ supervised learning, classification  
__Activation Function:__ A ReLu (Rectified Linear Unit) is used as the activation function. A softmax function is used as the activation function for the output.  
__Data Split:__ 60.000 samples as train data, 10.000 samples as test data    
__Model Description:__ Initially, some adjustments were made to ensure that some criteria for the model were met. 10% of the training data is used for validation. The architecture or model of the CNN is based on the LeNet-5 architecture. However, the model has been modified in some places. A maximum pooling layer was removed and a dropout layer was added. At the end the model consists of two Convolutional Layer, afterwards follows a maximum pooling layer. After the pooling layer follows a data-Preparation layer follows to convert the matrices to a one-dimensional array so that they can be processed by the two Fully-Connected layers. In addition, a Dropout layer was added to counteract overfitting by randomly discarding 40% of the data per iteration.   

__Evaluation Metrics:__ Accuracy=93,24%, Error=21%    

__Additional Information:__    

## Deployment

__Service:__ 
__Target Group:__ Online stores, fashion stores, logistics  
__Benefits:__ Cost savings, time savings, automation of processes.  
__Integration:__    

<a id="German_version"></a> 

# Classification of clothing through images (Deutschsprachige Version)  

## Geschäftsverständnis

__Unternehmen:__ na  
__Branche:__ Mode  
__Anwendungsbereich:__ Logistik  
__Geschäftsziel:__ Identifikation von Kleidung durch Bilder.    
__Beschreibung:__ Retouren müssen wieder aufgefüllt und verkauft werden können. Zu diesem Zweck müssen die Waren identifiziert und etikettiert werden. Zur Unterstützung dieses Prozesses soll ein ML-Dienst eingesetzt werden.   
__Lösung:__ Manuelle Erkennung durch Menschen und manuelle Beschriftung der Kleidung.  

## Datenverständnis

__Datenrahmen:__ fashion-mnist_test     
__Quelle:__ Kaggle, https://github.com/zalandoresearch/fashion-mnist  
__Datenersteller:__ Zalando   
__Datum der Veröffentlichung:__ 2017   
__Datentyp:__ CSV  
__Beschreibung des Datenrahmens:__ Der Datensatz besteht aus Artikelbildern der Firma Zalando. Insgesamt sind 60.000 Trainingsbilder und 10.000 Testbilder enthalten, die auf 28x28 Pixel skaliert und in ein Graustufenbild umgewandelt wurden.   
__Anzahl der Merkmale:__ 28x28 Pixel + Label    
__Anzahl der Ziele:__ 1  
__Datentyp pro Merkmal:__ integer    
__Datentyp pro Ziel:__ integer      
__Anzahl der Beobachtungen:__ 70.000  
__Parameter "Standort":__ na   
__Verteilungsparameter:__ na  
__Korrelationsanalyse:__ na  

## Datenaufbereitung  

__Dimensionalitätsreduktion:__ na   
__Ausreißer:__   
__Fehlende Daten:__     
__Unausgewogene Daten:__      
__Datenkonvertierung:__ Skalierung in Graustufenfarbe mit einem Wert zwischen 0-1, Konvertierung der Bildform von 784 in 28x28 (nur wenn als CSV mit 784 Spalten geladen), Konvertierung der Etiketten in kategoriale Daten (10 Kategorien)      
__Verteilungsfunktion:__ na  
__Merkmal Skalierung:__    
__Multikollinearität:__    

## Modellierung und Auswertung

__Algorithmen:__ Faltungsneuronales Netz (CNN)  
__Hyperparameter:__ Die erste und zweite Faltungsschicht ist mit 32 Filtern und einer Kernelgröße von 3 und keinem Padding parametrisiert   
__Output:__ überwachtes Lernen, Klassifikation  
__Aktivierungsfunktion:__ Als Aktivierungsfunktion wird eine ReLu (Rectified Linear Unit) verwendet. Eine Softmax-Funktion wird als Aktivierungsfunktion für die Ausgabe verwendet.  
__Datenaufteilung:__ 60.000 Proben als Trainingsdaten, 10.000 Proben als Testdaten    
__Beschreibung des Modells:__ Zu Beginn wurden einige Anpassungen vorgenommen, um sicherzustellen, dass einige Kriterien für das Modell erfüllt werden. 10 % der Trainingsdaten werden für die Validierung verwendet. Die Architektur oder das Modell des CNN basiert auf der LeNet-5-Architektur. Allerdings wurde das Modell an einigen Stellen modifiziert. Eine Maximum-Pooling-Schicht wurde entfernt und eine Dropout-Schicht wurde hinzugefügt. Am Ende besteht das Modell aus zwei Convolutional Layer, danach folgt ein Maximum Pooling Layer. Nach der Pooling-Schicht folgt eine Data-Preparation-Schicht, um die Matrizen in ein eindimensionales Array umzuwandeln, damit sie von den beiden Fully-Connected-Schichten verarbeitet werden können. Zusätzlich wurde eine Dropout-Schicht hinzugefügt, um einer Überanpassung entgegenzuwirken, indem 40% der Daten pro Iteration zufällig verworfen werden.   

__Auswertungsmetriken:__ Genauigkeit=93,24%, Fehler=21%    

__Zusätzliche Informationen:__    

## Einsatz

__Dienst:__ 
__Zielgruppe:__ Online-Shops, Modegeschäfte, Logistik  
__Vorteile:__ Kosteneinsparungen, Zeitersparnis, Automatisierung von Prozessen.  
__Integration:__
