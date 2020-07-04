# Olist - Churn Analysis

***Authors: Daniel Vigild Juhász & Lau Johansson*** <br /> <br />

## Overview
This repository contains hand-in assignment for the DTU course 42578 Advanced Business Analytics. 

The analysis is made on the Brazillian e-commerce public dataset of orders made at [Olist store](https://olist.com/).

The dataset is public available at Kaggle: https://www.kaggle.com/olistbr/brazilian-ecommerce


## Business case
In the project we wish to analyse customer churn: when customers have bought their first item on Olist, what has an impact on whether or not they purchase something again in the future?

We've found that the churnrate is 87.5%.  A customer with more than one order spends on average 96 Brazilian Reals (114 DKK) more than a customer with only one order. Having 84075 customers churning from Olist, making them return, could **bring** in around **8 million Brazilian Reals (9.5 million DKK)**.

## Methods
Our analysis is structured around the following steps:

* 	Text analytics of the review messages, including topic modelling.

*	Logistic regression, using variables about the first order of the customer and the topics found during text analysis.

*	Build Keras feed-forward neural networks that can be used to predict customer churn based on variables about the first order of the customer and results from the text analysis.

## Results

The results below shows how well our models are to predict customers returning to Olist. 

The best model, model 3, uses numeric order variables (price, freight value, product weight etc.) and review comment messages converted to tf-idf representation. 


| Model   | Variables                                             | Performance (F1-score) |
|---------|-------------------------------------------------------|------------------------|
| Model 1  | Numeric order variables                               | 69%                    |
| Model 2 | Numeric order variables + Topics from topic modelling | 82%                    |
| Model 3 | Numeric order variables + Single words                | 88%                    |


## Read more
Read our executive summary [here](https://github.com/LauJohansson/Olist_churn_analysis/blob/master/Executive_Summary_Olist.pdf) <br />
Look at the jupyter notebook [here](https://github.com/LauJohansson/Olist_churn_analysis/blob/master/Olist_churn_analysis.ipynb)


