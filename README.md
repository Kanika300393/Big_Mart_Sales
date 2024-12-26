# Big Mart Sales Prediction

![image](https://github.com/user-attachments/assets/e13681cc-35fa-434f-9504-ec03b6f25712)



## Overview

This project involves building a machine learning model to predict sales at Big Mart stores based on various product and store attributes. The model uses the XGBoost Regressor and is trained on the Big Mart sales dataset. The project demonstrates data preprocessing, exploratory data analysis, and model evaluation.

## Features

- Data cleaning and handling of missing values.
- Label encoding of categorical variables.
- Feature engineering to create a model-ready dataset.
- Use of the XGBoost Regressor for sales prediction.
- Model evaluation using R-squared scores on both training and testing datasets.

## Dataset

The dataset used for this project contains the following columns:

| Column Name            | Description                                                                            |
|------------------------|----------------------------------------------------------------------------------------|
| **Item_Identifier**     | Unique identifier for the item.                                                       |
| **Item_Fat_Content**    | Indicates if the item is low fat or regular.                                           |
| **Item_Type**           | Category of the item (e.g., dairy, beverages).                                         |
| **Item_Weight**         | Weight of the item.                                                                    |
| **Item_Visibility**     | The visibility of the item in the store.                                               |
| **Item_MRP**            | Maximum Retail Price (MRP) of the item.                                                |
| **Outlet_Identifier**   | Unique identifier for the outlet.                                                     |
| **Outlet_Size**         | Size of the outlet (Small, Medium, Large).                                             |
| **Outlet_Location_Type**| Location type of the outlet (e.g., Urban, Semiurban, Rural).                          |
| **Outlet_Type**         | Type of the outlet (e.g., Supermarket, Grocery Store).                                |
| **Outlet_Establishment_Year** | Year of outlet establishment.                                                      |
| **Item_Outlet_Sales**  | Target variable representing the sales of the item in the outlet.                     |

## Project Workflow

### 1. Data Collection and Initial Analysis

- Load the dataset using pandas.
- Inspect the dataset to check for missing values and general structure.

### 2. Handling Missing Values

- Replace missing values in **Item_Weight** with the column mean.
- Handle missing values in **Outlet_Size** by using the mode of the respective **Outlet_Type**.

### 3. Data Preprocessing and Encoding

- Apply label encoding to categorical variables such as **Item_Identifier**, **Item_Fat_Content**, **Item_Type**, **Outlet_Identifier**, **Outlet_Size**, **Outlet_Location_Type**, and **Outlet_Type** to convert them into numerical values suitable for machine learning.

### 4. Splitting Features and Target

- Separate the dataset into features (**X**) and the target variable (**Item_Outlet_Sales**).

### 5. Model Training

- Split the dataset into training and test sets.
- Train the **XGBoost Regressor** model using the training set.
- Make predictions for both training and test datasets.
- Evaluate model performance using **R-squared** values for both the training and test datasets.

### 6. Model Evaluation

- Calculate and display the **R-squared** values for both training and testing datasets.
- Evaluate how well the model performs in predicting sales.

## Visualizations

The following visualizations help understand the distribution of key features:

 **Item Weight Distribution**: Shows the distribution of item weights across the dataset.

![Item_Weight](https://github.com/user-attachments/assets/c910bc45-71a5-4d09-93f8-a8cefa910580)

 **Item Visibility Distribution**: Displays the visibility of items in the store.

![Item_Visibility](https://github.com/user-attachments/assets/85d3079e-05b2-4238-bad6-0f9789c147f0)


 **Item MRP Distribution**: Distribution of item prices.

![Item_MRP](https://github.com/user-attachments/assets/de5e0102-9cab-4d00-894a-59644179eae9)


 **Item Outlet Sales Distribution**: Shows the distribution of item sales.

 ![Item_Outlet_Sales](https://github.com/user-attachments/assets/c70a629a-8e26-48cf-850e-42bede8a2f95)


 **Outlet Establishment Year Distribution**: Distribution of outlet establishment years.

 ![Outlet_Establishment_Year](https://github.com/user-attachments/assets/a0c4ae50-dbae-4055-af5a-4e79db3e2367)

## Results

**Training R-squared Value**: Indicates how well the model fits the training data.

**Testing R-squared Value**: Indicates how well the model generalizes to unseen data.

**The R-squared values** for both training and testing data help assess the model's predictive performance. A higher R-squared value indicates a better model fit.


## Conclusion
This project demonstrates how to predict sales at Big Mart stores using machine learning techniques. The XGBoost Regressor provided a solid model fit with decent R-squared scores. Data preprocessing, including handling missing values and label encoding, significantly improved the quality of the dataset. The next steps could involve improving the model with hyperparameter tuning or using other regression algorithms.

