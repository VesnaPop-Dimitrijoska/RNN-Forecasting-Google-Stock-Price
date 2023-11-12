# Project Title:
Forecasting Google Stock Price with a SimpleRNN, LSTM and GRU univariate and multivariate RNN models
#
---
# Project Description:
Forecasting Google Stock Price with a SimpleRNN, LSTM and GRU univariate models for the target column 'Open'.      
Forecasting Google Stock Price with a SimpleRNN, LSTM and GRU multivariate models for the target "Open", by using "Low", "High", and "Open" as features. (given t, predict t+1)
#
---
# Table of Contents:

  1. Data Analysis
  4. Model Training
  5. Model Hyperparameter Optimization
  6. Model Prediction
  7. Model Evaluation
  8. Results and Conclusion
#
---
# Dataset: 
1. `Google_Stock_Price_Train.csv`  
2. `Google_Stock_Price_Test.csv`

---
# Preliminary analysis of a dataset:
---
### Shape of a Dataset:     
Shape of the Train dataset is: 1258 rows x 3 columns (without index column - Date column).     
Shape of the Test dataset is: 20 rows x 3 columns (without index column - Date column).

### NaN values:  
There are no NaN values. 

### Data types:  
Data types are correct but they are converted in more efficient data type with smaller precision.  

### Descriptive statistics:
The summary statistics is showing that data are on a similar scale, but should be scaled in order to be easily computed. 

#
# RESULTS
####
### 1) n_step = 1
![image](https://github.com/VesnaPop-Dimitrijoska/RNN-Forecasting-Google-Stock-Price/assets/144008804/98d494f2-fdf4-4c59-9281-5f1397370cc7)
![image](https://github.com/VesnaPop-Dimitrijoska/RNN-Forecasting-Google-Stock-Price/assets/144008804/4e7acaac-32ba-468d-ac3a-b81b8b68cfb2)

---     
####
### 2) n_step = 3
![image](https://github.com/VesnaPop-Dimitrijoska/RNN-Forecasting-Google-Stock-Price/assets/144008804/480edda8-bf00-42d8-a3b1-9cc99688995a)
![image](https://github.com/VesnaPop-Dimitrijoska/RNN-Forecasting-Google-Stock-Price/assets/144008804/e6be20d2-5845-41f0-906d-2c3d21b2c67f)

---     
####
### 2) n_step = 7
![image](https://github.com/VesnaPop-Dimitrijoska/RNN-Forecasting-Google-Stock-Price/assets/144008804/0046998c-c824-41d4-93ab-3ecc5767ca14)
![image](https://github.com/VesnaPop-Dimitrijoska/RNN-Forecasting-Google-Stock-Price/assets/144008804/2650a643-1efd-4ded-8f1f-6fa12e920fe7)

---    
####
## CONCLUSION: 
I experimented with multiple architectures, with different RNN layers, and different time steps. 
Here I'm using the same architecture but for different RNN models and different time steps: 1, 3, and 7 days.
The best model performance was achieved for the models with a time step of 1 day.     
As expected **multivariate model performed better than the univariate one**.

**Note:**      
I'm using batch_size = 1, because it gave me the best model performance. First I used more complex architecture for the model, trying to get the best model performance in order to predict Google Stock Price for real :-). This probably made the model more sensitive to batch size parameter, so the result varied a lot depending on this parameter. Then I changed it into a smaller architecture, so the result became less dependent on batch size.

---
#
# License
MIT License
#

