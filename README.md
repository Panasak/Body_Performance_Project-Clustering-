# Body Performance Project: Project Overview
This project uses clustering to group individual datas into 4 cluters (A ,B ,C ,D) based on their attributes and athletic performance.
* Create a tool that cluster datas into different clutsters to help determined the level of athleticism of people
* Optimized K-mean, Support Vector Machine, and K Nearest Neighbors using GridsearchCV and the elbow mathod to reach the best model
## Code and Resources Used
* **Python Version:** 3.7
* **Packages:** pandas, numpy, matplotlib, seaborn, scikit learn
* **Kaggle Dataset:** https://www.kaggle.com/kukuroo3/body-performance-data
## About The Data
The data contains the following columns:
* age : 20 ~64
* gender : F, M
* height_cm : (If you want to convert to feet, divide by 30.48)
* weight_kg
* body fat_%
* diastolic : diastolic blood pressure (min)
* systolic : systolic blood pressure (min)
* gripForce
* sit and bend forward_cm
* sit-ups counts
* broad jump_cm
* class : A, B ,C ,D (A: best) / stratified

## EDA
I looked at the distributions of the data and the value counts for the various categorical variables. Below are a few highlights from the pivot tables.

![alt text](https://github.com/Panasak/body_performance_project/blob/main/EDA/age.png)
![alt text](https://github.com/Panasak/body_performance_project/blob/main/EDA/box.png)
![alt text](https://github.com/Panasak/body_performance_project/blob/main/EDA/corr.png)
![alt text](https://github.com/Panasak/body_performance_project/blob/main/EDA/fat.png)
## Model Building
First I transformed the categorical variables into dummy variables. I also scaled the data and split the data into train and test sets with a test size of 30%.
I tired three different models and evaluated them using accuracy. I chose accuracy because it is relatively easy to interpret and outliers aren't particularly bad in for this type of model.
I tried three different models:
* **K Nearest Neighbors**
* **Support Vector Machine** 
* **K-mean**
## Model Performance
The K-mean model outperformed the other approaches on the test and validation sets
* **K-mea:** accuracy = 0.71
* **Support Vector Machine:** accuracy = 0.69
* **K Nearest Neighbors:** accuracy = 0.61
