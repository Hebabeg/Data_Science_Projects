# Amazon Best Seller Books Analysis: A Data Science Project


## Introduction

This project explores and models data from a collection of Amazon's best-selling books from 2009 to 2019. The goal is to analyze trends in bestsellers and build classification models to predict the genre (Fiction or Non-Fiction) based on features like user ratings, number of reviews, price, and year.

## Dataset Overview

The dataset contains the following columns:

Name: Book title

Author: Author name

User Rating: Rating (1-5 scale)

Reviews: Number of user reviews

Price: Book price (USD)

Year: Year when the book was a bestseller

Genre: Either 'Fiction' or 'Non Fiction'

## Data Cleaning

Removed dollar symbols from prices.

Converted price to float.

Checked and confirmed absence of missing values.

Removed duplicate entries to prevent data leakage.

## Exploratory Data Analysis (EDA)

The following visualizations were used:

#### 1. Distribution of User Ratings

![image](https://github.com/user-attachments/assets/82e11a90-9659-4300-8b25-d1f5147c246e)

Observation: Most books have high ratings (between 4.5 and 5.0), indicating positive user feedback across bestsellers.

#### 2. Genre Distribution

![image](https://github.com/user-attachments/assets/3ed370f0-2d6d-42ca-836e-b65c22735f44)

Observation: Non-Fiction books dominate the dataset, showing a strong market interest in real-world or instructional content.
* 0 indicates Non Fiction and 1 indicates Fiction

#### 3. Number of Reviews vs. Rating

![image](https://github.com/user-attachments/assets/0900c558-eaad-4fdc-bfca-401645e3981e)

Observation: Fiction books tend to have more variance in the number of reviews but both genres span across high ratings.

#### 4. Price Distribution by Genre

![image](https://github.com/user-attachments/assets/bc43ba2a-a637-42b9-a43a-4261122ce8dc)

Observation: Non-Fiction books tend to have higher prices on average compared to Fiction books.

## Predicting Book Genre

The problem was framed as a binary classification task: Predict whether a book is Fiction (1) or Non-Fiction (0) based on numerical features.

#### Features Used:

User Rating, Reviews, Price, Year

#### Models Built:

Logistic Regression
Decision Tree Classifier
Random Forest Classifier
Deep Neural Network (DNN)

#### Data Preprocessing:

Train-test split (80-20) with stratification on genre.
Standardized input features for DNN.

#### Evaluation Metric:

Accuracy
Classification Report (Precision, Recall, F1-Score)
Confusion Matrix

## Results

![image](https://github.com/user-attachments/assets/4b5612e2-2cc7-4032-ab3d-0029c3d82547)

![image](https://github.com/user-attachments/assets/098af0bd-4952-4505-80d4-73f51cae4dd5)

![image](https://github.com/user-attachments/assets/4b4b31f2-3fb1-476a-86bf-498264bd56f5)

![image](https://github.com/user-attachments/assets/82c6868a-6172-411d-803a-41c1b08abead)

![image](https://github.com/user-attachments/assets/31272df9-ca1a-4189-aa01-1c78d4398398)

The best model was Decision Tree based on accuracy. The confusion matrix visualized true positives and false negatives, showing effective class separation.

![image](https://github.com/user-attachments/assets/d7a32363-09f5-4eb6-a10b-5c5c69b42b88)


## Feature Importance (Tree-Based Models)

Using the best-performing tree-based model, we plotted feature importances:

![image](https://github.com/user-attachments/assets/10b1bb7d-b18e-4543-ae92-9b1f7deebeb7)

Key Insight: The most important features were Reviews and Price, showing user engagement and feedback strongly influence a book's classification.

## Conclusion

This analysis demonstrates that simple metadata about best-selling books can be used to build reasonably accurate genre classifiers. Visuals help uncover patterns in pricing, review counts, and ratings, while ML models provide predictive insights





