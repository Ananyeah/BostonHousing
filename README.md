# ExploringAProblem

## Domain of the Problem :
  
  Sources:
   (a) Origin:  This dataset was taken from the StatLib library which is
                maintained at Carnegie Mellon University.
   (b) Creator:  Harrison, D. and Rubinfeld, D.L. 'Hedonic prices and the 
                 demand for clean air', J. Environ. Economics & Management,
                 vol.5, 81-102, 1978.
   (c) Date: July 7, 1993
  

## How has data science or machine learning been used to solve this or similar problems in the past?

Past Usage:
   -   Used in Belsley, Kuh & Welsch, 'Regression diagnostics ...', Wiley, 
       1980.   N.B. Various transformations are used in the table on
       pages 244-261.
    -  Quinlan,R. (1993). Combining Instance-Based and Model-Based Learning.
       In Proceedings on the Tenth International Conference of Machine 
       Learning, 236-243, University of Massachusetts, Amherst. Morgan
       Kaufmann

# Problem Statement

## The inputs


    1. CRIM      per capita crime rate by town
    2. ZN        proportion of residential land zoned for lots over 
                 25,000 sq.ft.
    3. INDUS     proportion of non-retail business acres per town
    4. CHAS      Charles River dummy variable (= 1 if tract bounds 
                 river; 0 otherwise)
    5. NOX       nitric oxides concentration (parts per 10 million)
    6. RM        average number of rooms per dwelling
    7. AGE       proportion of owner-occupied units built prior to 1940
    8. DIS       weighted distances to five Boston employment centres
    9. RAD       index of accessibility to radial highways
    10. TAX      full-value property-tax rate per $10,000
    11. PTRATIO  pupil-teacher ratio by town
    12. B        1000(Bk - 0.63)^2 where Bk is the proportion of blacks 
                 by town
    13. LSTAT    % lower status of the population
    14. MEDV     Median value of owner-occupied homes in $1000's
    
    Number of Instances: 506


## The type of data science or machine learning you intend to do

This is a supervised learning : prediction problem, but for this exercise I'm just going to exploratory analysis.

- Redundancy: Find how each 'independent' variable is actually defined by other independent variables
- Find correlation and look at it visually. It suggests redundancy too, but also can be used to find the strength of predicting a target.

## The outputs

- The benchmark or an initial goal on what would be considered worthy enough to have a model predict this as opposed to basic methods of estimation.
- The train set and the fit on the train set.
- The test set's fit and 
- A classification matrix.

## According to Tom Mitchell's rigorous definition of a machine learning problem:

A computer program is said to learn from 
experience E (in this case the training census data)
with respect to some class of tasks T (salary earned)
and performance measure P (fit, accuracy wrt test and validation data), 
if its performance at tasks T, as measured by P, improves with experience E.

# A description of the dataset including:
## The types of the data :

2 variables : CHAS and ZN are categorical.
The rest are not normally distirbuted.


# A proposed solution 
Linear Regression

# A benchmark model
Mean would be a good benchmark

# A performance metric used to assess the performance of your proposed solution
R^2

# Learning:

Scaling helps with comparing columns
Log transform helps with converting non-normal to normal but won't work on negative and 0 values.
Scaling should be done after applying the transform.
Outliers are 1.5 times interquartile range.