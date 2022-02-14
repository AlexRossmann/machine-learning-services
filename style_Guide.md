# Style Guide
for this Repository

All notebooks shall adhere to this guide.

File structure:
```
├─── Name of ML use case  
    +-- data.csv  
    +-- notebook.ipynb  
    \-- README.md  
```
The names of the files shall be as shown above.  
If there are multiple data files you can use a data folder.  
Make sure you adjust your filepath stings in your notebook!  

# For notebooks
- name of notebook is notebook.ipynb
- all import Statements on Top of the the file
- everything is in english: Variables, comments, figure title, figure axis, and Markdown text

## adhere to PEP 8
https://www.youtube.com/watch?v=D4_s3q038I0&t=1182s  
! use automatic formatting with something like autopep8 or [black](https://github.com/psf/black)  
[howto](https://www.youtube.com/watch?v=Zrxi86KMT7k) for jupyter notebook

## notebook structure
a notebook should have this structure

1. Business Understanding
2. Data and Data Understanding  
2.1. Import of Relevant Modules  
2.2. Read Data  
2.3. Data Cleaning  
2.4. Descriptive Analytics  
2.4.1. Continous Features  
2.4.2. Categorical Features  
3. Data Preparation  
3.1. Reduce Customer ID  
3.2. Recoding of Categorical Variables  
3.3. Test for Multicollinearity  
3.4. Feature Scaling  
3.5. Undersampling   
3.6. Create Test and Training Data  
4. Modelling and Evaluation  
4.1. Logistic Regression  
4.2 Evaluation  
4.3. Interpretation  
4.4. Model Optimization  
5. Deployment  

## Variable names
use snake_case always
no camelCase !!

### Variables:  
data_raw = pd.read_csv("data.csv")  
data_cleaned  
data_1  
data_2  
data_3  
y = data["Target Variable"]  
x = data.drop(["TargetVariable"])  
x = scaler.fit_transform(x)
X_train, X_test, y_train, y_test = train_test_split(X_resampled, y_resampled, random_state=110)  
model_lin_regression = LinearRegression()  
model_lin_regression.fit(x_train,y_train)  
model_nearest_neighbors = NearestNeighbors().fit(x_train)  