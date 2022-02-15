# Machine Learning Service Repository
## Goal
The goal of this repository is to help businesses to figure out the value of applying Machine Learning (ML) in their business activity's. With the ML Services documented in this repository you can learn how ML used to create value. In the accompanying notebook and the attached data you can learn by example how the data is explored, how relevant conclusion are drawn from the data visualizations and how a ML model is created, trained and deployed.

## Introduction    

This repository contains 25 publicly available use cases that can be used as a machine learning service. These use cases include data frames from different application areas such as medicine, marketing, IoT, etc. The models were all implemented using the Python programming language and are stored in this repository as Jupyter Notebooks. The repository was structured according to application areas or industries. The services listed below can be found in the respective folders.  
All data files are stored in google cloud storage in [this bucket](https://storage.googleapis.com/ml-service-repository-datastorage)  

see [List of Use Cases](#List_of_Use_Cases), for a structured list of all examples in this repository  
see [Usage](#Usage) for an explanation on how to use this repository and how to run the notebooks.

one example Use Case has been deployed by creating a REST API opn top of the tensorflow model. You may look at the code on the [repository](https://github.com/Dustin-dusTir/ml-services-api), check out the [API docs](https://predict-wine-quality-api.herokuapp.com/docs) or try out the [frontend](https://predict-red-wine-quality-with-ml.netlify.app/) to predict the quality of your red Wine.


![ML](https://images.unsplash.com/photo-1526925539332-aa3b66e35444?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=465&q=80)

<a id="List_of_Use_Cases"></a>   

## List of Use Cases 

### CRM:
1. Customer Churn Prediction
2. Customer Satisfaction Airlines
3. Increase customer satisfaction
4. Sentiment analysis on amazon reviews

### Automotive:
5. Improvement of components for autonomous motor vehicles

### Warehouse:
6. Classification of clothing through images

### Success Prediction: 
7. Prediction of Successful or Failed Startups
8. Prediction of Successfully Financed Projects

### Online Retail: 
9. Size prediction for online fashion retailer

### Rating:
10. Accommodation rating
11. What Quality does the Red wine have
12. Digital Valuation of Real Estate

### Forecast:
13. Forecast of required vehicles in the city center
14. Sales Forecast for retail store

### Health:
15. Healthcare system finding causes and patterns for common diseases
16. Risk prediction of heart disease

### Insurance:
17. Predicting mental illness for health insurance
18. Prediction Interest for car insurance
19. Insurance Fraud detection

### Marketing:
20. Generation of Individual Playlists
21. Predicting clicks on online advertising by Facebook

### Tourism:
22. Prediction cancellation of hotel bookings
23. Flight delay prediction      

### Agriculture:
24. Analysis of the movement and activity of free-ranging cattle

### Maintenance:
25. Prediction of IoT system failures based on sensor data

<a id="Usage"></a>  

## Usage
There are two ways you can run the python notebook yourself, as described below.  
Or you click  the google colab button in the README, to run the notebook in the cloud (for free).  
example: <a href="https://colab.research.google.com/github/AlexRossmann/machine-learning-services/blob/main/CRM/Customer%20Churn%20Prediction/notebook.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Notebook In Google Colab"/></a>  



### Setup python virtual environment
To setup the virtual environment download [python 3.8](https://www.python.org/downloads/release/python-389/), and run the following commands.
We recommend using python 3.8, as this release is the most reliable with the tensorflow module.   
All notebooks in this repo have been verified to run with *python 3.8* and the dependencies listed in *requirements.txt*

```bash
py -3.8 -m venv venv
venv\Scripts\Activate.ps1
pip install --upgrade pip
pip install -r requirements.txt
```
or (in VSCode) drag and drop the *setupPython.ps1* script into your Terminal and press Enter

Then open the notebooks (and README ) inside VSCode   
or run
```bash
jupyter notebook
```
in the same terminal.
