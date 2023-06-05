# Linear_Regression

>Linear regression is a statistical method used to model the relationship between a dependent variable (also called the response or target variable) and one or more >independent variables (also called the predictors or explanatory variables) by fitting a linear equation to the observed data.
>
>The goal of linear regression is to find the best-fitting line through the data, which can be used to make predictions or to understand the relationship between the >variables. The line is typically represented as:
>
>y = b0 + b1 * x1 + b2 * x2 + ... + bn * xn
>
>where y is the dependent variable, x1, x2, ..., xn are the independent variables, b0 is the intercept, and b1, b2, ..., bn are the coefficients that determine the slope >of the line.
>
>Linear regression can be used for both simple linear regression, where there is only one independent variable, and multiple linear regression, where there are two or >more independent variables.

## Example Of Linear Regression

>Suppose we want to model the relationship between a person's weight (dependent variable) and their height (independent variable). We have collected data from 50 >individuals and their weights and heights are recorded in a dataset.
>
>First, we would plot the data to see if there is a linear relationship between the variables. Here's what the plot might look like:
>
>![LR_graph](https://user-images.githubusercontent.com/107355282/233779483-28ec04c1-e91d-4f36-9965-26dde6b94bda.png)

>From the plot, it appears that there is a positive linear relationship between height and weight - as height increases, weight tends to increase as well.
>
>Next, we would fit a linear regression model to the data. We would specify weight as the dependent variable and height as the independent variable. The model equation >would be:
>
>weight = b0 + b1 * height
>
>where b0 is the intercept and b1 is the slope.
>
>We would use a method like least squares to estimate the values of b0 and b1 that best fit the data. Once we have estimated these coefficients, we can use the >equation to make predictions for new values of height.
>
>For example, if we want to predict the weight of a person who is 6 feet tall, we would plug 6 into the equation:
>
>weight = b0 + b1 * 6
>
>and solve for weight.

### Advantages:

>***Simplicity***: Linear regression is a relatively simple and easy-to-understand method for modeling the relationship between variables. It is a linear approach, >which makes it easy to interpret and explain the results.
>
>***Flexibility***: Linear regression can be used for both simple and multiple regression analysis, which allows for modeling complex relationships between multiple >independent variables and a dependent variable.
>
>***Efficiency***: Linear regression is computationally efficient and can be performed quickly on large datasets.
>
>***Prediction***: Linear regression can be used to make predictions of future outcomes based on the relationship between the independent and dependent variables.
>
>***Interpretation***: The coefficients of the independent variables in a linear regression model can be used to interpret the relative importance and direction of the >relationship between the variables.
>
>***Hypothesis testing***: Linear regression can be used to test hypotheses about the relationship between the independent and dependent variables, and to determine if >the relationship is statistically significant.
>
>Overall, linear regression is a powerful tool for modeling relationships between variables and making predictions about future outcomes.

#### Disadvantages

>**Linearity assumption**: Linear regression assumes that the relationship between the dependent and independent variables is linear. If the relationship is not >linear, the model may not fit the data well and produce inaccurate predictions.
>
>**Outliers**: Linear regression is sensitive to outliers, which can have a significant impact on the estimated coefficients and the model's predictive accuracy.
>
>**Multicollinearity**: If the independent variables in a multiple regression model are highly correlated with each other, it can lead to multicollinearity, which can >make it difficult to interpret the coefficients and make accurate predictions.
>
>**Non-independence of errors**: Linear regression assumes that the errors are independent and identically distributed. If there is non-independence of errors, such as >in time series data, the model may not be appropriate.
>
>**Overfitting**: Linear regression can overfit the data if the model is too complex or if there are too many independent variables relative to the sample size, which >can lead to poor generalization to new data.
>
>**Lack of robustness**: Linear regression can be sensitive to changes in the data and the model assumptions, which can make it less robust than other modeling >techniques.
>
>Overall, while linear regression is a useful tool for modeling relationships between variables, it has limitations and may not be appropriate for all types of data or >research questions.

** This Algorithm might tend to overfit.**

# Code for training,testing and finding the predictions and accuracy of the model

## Importing the required module ##

> import numpy as np
> 
> from sklearn import datasets
>   
> from sklearn import linear_model
>     
> from sklearn.model_selection import train_test_split
>   
> from matplotlib import pyplot as plt
>     
> import pandas as pd
>     
> from sklearn.preprocessing import LabelEncoder
     
### Reading the csv file/dataset

> data = pd.read_csv('/content/HousingData.csv')
>
> print(data.head())   //printing the dataset
>     
> // output of dataset
>
>      CRIM    ZN  INDUS   CHAS   NOX     RM   AGE    DIS    RAD  TAX    PTRATIO  \
> 0  0.00632    18.0    2.31    0.0   0.538   6.575   65.2   4.0900     1   296     15.3   
> 1  0.02731     0.0    7.07    0.0   0.469   6.421   78.9   4.9671     2   242     17.8   
> 2  0.02729     0.0    7.07    0.0   0.469   7.185   61.1   4.9671     2   242     17.8   
> 3  0.03237     0.0    2.18    0.0   0.458   6.998   45.8   6.0622     3   222     18.7   
> 4  0.06905     0.0    2.18    0.0   0.458   7.147   54.2   6.0622     3   222     18.7   
>
>       B    LSTAT   MEDV  
> 0  396.90     4.98   24.0  
> 1  396.90     9.14   21.6  
> 2  392.83     4.03   34.7  
> 3  394.63     2.94   33.4  
> 4  396.90      NaN   36.2  

x = data[[
    'CRIM',
    'INDUS',
    'NOX',
    'DIS',
    'RAD'
]]
     
y = data[['TAX',
          'ZN',
          'CHAS',
          'AGE',
          'MEDV'
]]
     
y = np.array(y)  // Converting y into array form
     
print(x, y)  






