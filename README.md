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
>![LR_graph](https://user-images.githubusercontent.com/107355282/233765629-8a608837-7476-4838-8162-2176e3c3e70b.png)
From the plot, it appears that there is a positive linear relationship between height and weight - as height increases, weight tends to increase as well.
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
