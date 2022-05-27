# BIGMART SALES PREDICTION ANALYSIS
## ANALYSIS OF SALES BY FAT CONTENT AND FAT CONTENT SALES BY OUTLET TYPE  

Author: KRIT PATEL 

### Business problem:

How the Fat content of product aftect total sales and sales by Outlet Type.


### Data:
Data From : https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

Data set: https://drive.google.com/file/d/1syH81TVrbBsdymLT_jl2JIf6IjPXtSQw/view?usp=sharing

## Methods

IDENTIFY FEATURES

NUMERICAL FEATURES: Item_Weight, Item_Visibility, Item_MRP, Outlet_Establishment_Year


ORDINAL FEATURES: Outlet_Size, Outlet_Location_Type. 


NORMINAL FEATURES: Item_Type, Outlet_Type, Item_fat_Content

DATA CLEANING

Impute Mean for numerical data

Impute Most Frequent for categorical data. 

Replace Item_Fat_Content categories from 5 (Low Fat, low Fat, LF, Regular, reg) to 2 (Low Fat Regular)

DATA PREPROCESSING:

Pipeline numerical data to impute missing values with the mean and then scale

pipeline categorical data to impute missing values with most frequent and then one hot emcode

MODEL SELECTION:

R2 Score: R2 Score represpents the proportion of the variance for our target that is explained by our features. It also show us how bias model is to the data. 


Mean Squared Error (MSE): The Mean Squared Error exagerates the bigger errors as it squares all errors. This shows us the impact of big errors


Root MeanSquared Error (RMSE): This Test will show the same values as the target but they will also exagerate the larger errors.

VISUALIZATION:

histogram
BoxPlot
barchart
heatmap

## Results
We can see that the sale of Low Fat products are very competitive with Regular fat products. 
### 


#### Box Plot representing Sales by Fat Content
![3B7B890E-908D-4F70-A607-FB9AE1197C28](https://user-images.githubusercontent.com/103543062/170676767-c2464906-271c-4334-bd51-7d99a654c634.png)

This Boxplot graph indicates that the maximum quantity of regular fat items is slightly higher than that of low fat items.

This means that the market still favors regular fat content items over the lower fat content however they are very competitive. 

 However, there are outliers in some categories of low fat food where the sale of those products surpasses any outlier item in the regular category.

 This indicates that the market favors some low fat content products over regular fat.
 

#### Bar Chart representing the Fat Conntent Sales by Oulet Type
![E4F7EC4F-414B-4A7C-B4FA-88F65B126428](https://user-images.githubusercontent.com/103543062/170677269-a8967c08-1f25-4f9a-a362-a856cb890caa.png)

This Bar Chart shows us the sales of Low and Regular Fat products by different outlet types. By analyzing this graph we can tell that Grocery Stores sell the same amount of Low Fat and Regular Fat products. Type 2 Supermarkets sell more Low Fat products while Type 1 and 3 Supermarkets sell more of the Regular Fat products.

## Model Selection

Regression Tree Model: A regression tree is a series of questions designed to predict a continuous value. In the case of this data set, we will analyze how the feature columns affect the target column.


R2 Score = 0.5947099753159972, MSE Test = 1118185.973077762, RMSE Test = 1057.4431299496734

The model is underfit as the R2 Scores are very low indicating that the model has a high bias. This may be due to a lack of correlation in the features and target as shown by the heat map below

![2C04B766-B920-42F9-9033-6D4BF94DE750](https://user-images.githubusercontent.com/103543062/170680844-6f0a2b04-fe32-4e34-8ee2-48d4940af733.png)


## Recommendations:

Increase the either the amount of data or the amount features in the data set


## Limitations & Next Steps:

![3EA8727F-6F2A-42D9-9A81-4E04AD68571B](https://user-images.githubusercontent.com/103543062/170681717-93aefb15-b81b-42f9-b358-2c88dba688a3.png)

This heat map shows the correlation between different columns in the dataset. We can notice that there is very little correlation among the columns. The next step would be to introduce more features that can correlate with the target Item_Outlet_Sales to reduce the bias present in this model

### Contact Information
kritp144@gmail.com


For any additional questions, please contact **email**
