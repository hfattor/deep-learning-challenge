# deep-learning-challenge
Use machine learning and neural networks to create a binary classifier to predict whether fictional organizations will be successful.

In <a href='https://colab.research.google.com/drive/1JYV34hptTVWeiQB3JI5TLielwiLkFg63?usp=share_link'> Google Collaboratory</a>

## Overview
The purpose of this neural network learning model is to predict the success of an organization that is funded by the fictional nonprofit foundation Alphabet Soup. The dataset includes the following information:

* EIN and organization ID columns
* Application type
* Industry affiliation
* Government organization classification
* Use case for funding
* Organization type
* Active status of the organization
* Organization income classification
* Special considerations for the application
* Amount requested in funding from Alphabet Soup
* Whether or not the money was used effectively

The application type and government organization classification had a high number of variables, so the data was preprocessed to reduce the number of variables in each of these categories to 7 (with variables that had below a certain threshold of answers grouped together in an 'Other' category). 

## Results

The target for the model was to predict whether or not the money was used effectively (the 'IS_SUCCESSFUL' column in the dataset). Features of the model included the following columns:

* APPLICATION_TYPE
* AFFILIATION
* CLASSIFICATION (Government organization classification)
* USE_CASE (Use case for funding)
* ORGANIZATION (Organization type)
* INCOME_AMT (Organization income classification)
* SPECIAL_CONSIDERATIONS (Special considerations for the application)

Columns deemed irrelevant to the model included the following: 

* EIN 
* NAME (organization ID columns)
* STATUS (Active status of the organization)
* ASK_AMT (Amount requested in funding from Alphabet Soup)

These columns were removed before splitting the data into training and testing datasets. 

The model built had 3 hidden layers, with a total of 9,841 parameters input. The initial input dimensions were 40. Two layers were sigmoid, as this activation function is useful for predicting probabilities, while a rectified linear unit function was used for one layer to help simplify the output. 

While the goal of the model was to predict the success of the organization funded with over 75% accuracy, this was not achieved. Additional epochs were added (100 and 150 were tested) with no increase in model accuracy. Layer inputs were shifted as well with no change in accuracy. The number of variables in the 'APPLICATION_TYPE' column was expanded to 7 with no change in accuracy. 

The model has 73% accuracy in predicting the success of funded organizations.

## Summary

With more information about the application type and the government classification variables, the value of these inputs may be deemed more or less important to include in the model. Future models could expand or reduce the number of features to see what affects accuracy. Additional layers could be added to increase accuracy. 
