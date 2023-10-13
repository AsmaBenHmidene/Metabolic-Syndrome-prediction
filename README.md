# Metabolic Syndrome Prediction
## Objective:
To predict metabolic syndrome based on common risk factors

### Business problem:
   Metabolic syndrome (MetSyn) is a cluster of risk factors including hypertension, hyperglycemia, and abdominal obesity. Metabolism-related risk factors include diabetes and heart disease. 
 All of these variables raise medical costs. Developing a prediction model that can quickly identify persons at high risk of MetSyn and offer them a treatment plan is crucial. Early prediction of metabolic syndrome will highly impact the quality of life of patients as it gives them a chance for making a change to the bad habit and preventing a serious illness in the future.

### Data:
[ The dataset for analysis came from the NHANES initiative]( https://data.world/informatics-edu/metabolic-syndrome-prediction)

For this dataset, there are 2401 rows and 14 columns.


## Methods
To prepare this data, the data was cleaned, and the following processes were performed:
### Exploratory Data Analysis
    - During the exploratory data analysis, boxplots and histograms were visualized for numeric datatype column. 
    - Also, barplots were visualized for categorical column. 
    - This gave a good baseline for all of the numeric and categorical columns for univariate EDA.

#### Visual 1 
![sample image](image0.png)

> This histogram shows that the average of the sales are around $2,181.29.


## Results
 ### Expanatory Data Analysis
    - To visualize the data for explantory purposes, two bargraphs and one regplot were chosen.
    - The bargraphs were chosen to show how the categories compare to each other. 
    - Finally, a regplot was chosen to show the trend of sales when coorelated to the maximum retail price of the product. 

#### Visual 2 
![sample image](image1.png)

>Who is most affected by metabolic syndrome?
>Hispanic and Mexican Americans are more likely to get metabolic syndrome (20%), followed by white poeple (18%) and Black poeple(16%). The least to get metabolic syndrome are Asian with only 11% of affected people.

#### Visual 3 
![sample image](image2.png)

>  Regular products represent the principle sales and more specifically seafood. Fruits and vegetables come in the second position even though they represent the main products offered for sales.

> For Low fat item, starchy foods represent the most selled product.

#### Visual 4 
![sample image](image3.png)

> The scatterplot correlating Item outlet sales with item MRP shows 4 groups:
> - Items with MRP between 20 and 70 (group 1) show the lowest sales average,
> - followed by Items with MRP between 80 and 140 (group 2),
> - then Items with MRP between 140 and 200 (group 3)
> - and finally Items with sales between 210 and 270 (group 4) that represent the highest items'sales .

> There is a positive correlation between the outlet sales and MRP: The sales increase whith the increase of the MRP of the product.

## Model
 ### Maching Learning Using the Following Models:
    Three prediction models were tested:
       - LogisticRegression
       - k-nearest neighbors
       - Random Forest

    All the 3 models were tuned to get a better metrics results using grid_search.

 ### Models Evaluated & Results
 
- Logistic Regression Model:

  - Training R^2: 0.562
  - Testing R^2: 0.567
 
  - Training RMSE: 1,139.10
  - Testing RMSE: 1,092.86
  

- Decision Tree Regressor Model:
  
  - The training r2 is: 1.0.
  - The testing r2 is: 0.176.
 
  - Training RMSE: 0.00
  - Testing RMSE: 1,507.47


- In case of the linear regression model:
  - Coefficient of Determination/R2: The model performs almost equally on the training data and the test data (R2 0.562 for training data vs. 0.567 for test data).
  - Root Mean Squared Error (RMSE) Interpretation: On average, our model is incorrect by about 1.09 thousand dollars, almost the same error value predicted with the training data (This metric penalizes larger errors).
  
This model represent a good balance between the training data and testing data prediction.

- In case of the regression tree model:
  - Coefficient of Determination/R2: The model performs much more better on the training data (R2 1.0. for training data vs. 0.176 for test data).
  - Root Mean Squared Error (RMSE) Interpretation: On average, our model is incorrect by about 1.5 thousand dollars, while the error value predicted with the training data is equal to 0.00.
  
This model is overfited, it makes good predictions on a training set, but poor predictions on a testing set.

- The Final Model Chosen is the Linear Regression Model.

## Recommendations:

The properties of products and and outlets that play crucial roles in increasing sales are as follow:

 1. Outlet types: since Supermarket Type3 shows the highest sales average (3700), it will be recommended to increase the number of this type of supermarket instead of Supermarket Type 1 which represent the main type among all outlets(65%). 
    
 2. Properties of products: Regular products represent the principle sales and more specifically seafood. Fruits and vegetables come in the second position even though they represent the main products offered for sales in the outlets. Those products are essentials for daily food consumption 
For Low fat item, starchy foods represent the most selled product.

Fruits and vegetables, seafood and starchy foods are essentials products for daily food consumption, which explain why they represent the main sales in the outlets. It is recommended to increase the quantity of seafood presented for sales because according to data, seafood are the least frequent item in all outlets. 

 4. From the correlation between outlets sales and MRP of product, we can conclude that Items with MRP between 140 and 270 represent the highest items'sales. It is recommended to increase the visibity of those products to increase outlets sales. 
 
 5. Model Performance
- Overall, the best model is definitely the linear regression model, by far it outperformed the regression tree model.


## Limitations & Next Steps

  Other factures can play an important role to confirm the proposed recommendation, for example, increasing the number of supermarket type 3 might be costy due to the dimension of those market or their location.Collecting more information will help to make a final decision. Therefore, as a next step, it will be recommended to study in deepth the sales in supermarket type 3 and considere it a model to ameliorate the sales in the other type of outlets.


### For further information

For any additional questions, please contact: Asma Ben Hmidene **asmabhpython@gmail.com**
