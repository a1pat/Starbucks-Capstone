# Free Cappucino, Anyone? #
This a Capstone project for the Udacity Datascience Nanodegree program.

## Table of Contents ##
1. [Motivation](#motivation)
2. [Problem Statement](#problem_statement)
3. [Summary of Analysis](#summary_of_analysis)
4. [Summary of Results](#summary_of_results)
5. [File Descriptions](#file_descriptions)
6. [Libraries](#libraries)
7. [Acknowledgement](#acknowledgement)
8. [Author](#author)

A detailed analysis and results can be found [here](https://ashutosh-patwardhan.medium.com/free-cappuccino-anyone-55c3dd5af).

## Motivation<a name="motivation"></a> ##
Starbucks is interested in knowing how its Rewards mobile app users respond to various promotional offers. Who is likely to make a purchase in response to an advertisement, a discount offer, a BOGO (buy one get one free)? Who is likely to make a purchase even if there is no promotion?

## Problem Statement<a name="problem_statement"></a> ##

This project seeks to answer the following specific questions:
1. What are the customer demographics? What are the natural customer groups?
2. Which are the most popular promotional offers? Do some offers resonate more with certain customer segments? Are there any offers that don’t excite anybody?
3. How well can a model predict which offers are likely to be well received?

## Summary of Analysis<a name="summary_of_analysis"></a> ##
1. There are three sets of data - offer data, customer data and transaction data. The analysis starts with understanding the data: variable distributions, inter-variable relationships, and any data-related issues.
2. Prelimary exploration is followed by more in-depth understanding of customer data using PCA and K-Means clustering.
3. Transaction data is processed to categorize the outcome of each instance of each offer as either successful, unsuccessful, inconclusive, unsolicited or lost. The categorization is combined with customer data and offer parameters to determine what drives an offer's success rate.
4. Finally classification models are developed to predict the outcome of an offer as a function of customer attributes. A global model is developed to predict the outcomes for a new type of offer.

## Summary of Results<a name="summary_of_results"></a> ##
1. Eight data issues were identified during preliminary data exploration. These have the potential to create biases in the model. It is not possible to resolve these with available information. We caveat and proceed. A nonth issue related to incorrect labeling of completed offers was identified and addressed by re-labeling the completion transactions.
2. PCA and K_Means reveal that gender is the main differentiating attribute among customers. Further distinction can be made along age, income and membership year lines.
3. The most successful offers are found to have been sent using all of email mobile and social channels. Not surprisingly, income is the customer attribute that determines whether a customer completes an offer. Income is confounded with age, gender (F gender age and income are skewed to the high side while M gender age and income are skewed to the low side).
4. DecisionTree classifiers are fit to each offer and to a "global" data set. Classifier parameters are tuned using GridSearch. The accuracy metric for the **test set** is generally around 0.65 or higher which is considered acceptable. Optimal classifier parameters are obtained.

## File Descriptions<a name="file_descriptions"></a> ##
The following files and folders are in the root folder:
* 

## Libraries/Packages<a name="libraries_packages"></a> ##
The following python packages are used:
1. numpy
2. pandas
3. json
4. matplotlib
5. tqdm
6. sklearn

## Acknowledgement<a name="acknowledgement"></a> ##
[Udacity](http://www.udacity.com) provided the Starbucks data files (portfolio.json; profile.json; transcript.json).

## Author<a name="author"></a> ##
Ashutosh A. Patwardhan [GitHub](https://github.com/a1pat), [LinkedIn](https://www.linkedin.com/in/ashutosh-patwardhan/) did all the analysis and modeling.
