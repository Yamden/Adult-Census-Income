# Adult-Census-Income
This dataset is Adult Census income collected by the U.S. Census Bureau in 1994 and 1995.
Data can be found on kaggle: https://www.kaggle.com/uciml/adult-census-income

Some of the steps that had to be made to cleanup the data was to re-classify most of the columns as factors in order for me to predict and test on them. In addition to that there were many rows that had NA or certain variables that had missing values and those needed to be filled in. I also had to re-classify if a person made more than 50k or less than 50k to make it easier to factor the income. In addition to that, there was 2 columns that I removed because I deemed them not important to the data - These were the fnlwgt (final weight of that census believes the entry represents) and education.num (number of years of education).

I used Logistic Regression here because you could evaluate the amount a person could make based on the given information. In this case, it's a simple if they made more than 50k or less than 50k, but using the information you could predict either. The results of the Logistic Regression were as followed:
ACC: 84%
The accuracy of the logistic regression was quite high at 84%. Taking a closer look, the sensitivity was at 96%, meaning that the model could find 96% of all the predicted incomes that are more than 50k. Specificity is at 48%, meaning that the model could find 48% of all predicted incomes less than 50k. This model was good at predicting those that made more than 50k, but not so much for those that makes less than 50k.

I used Naive Bayes here due to the large data set that is given. By comparing the 50k income with the different variety of classes that are provided. In this case, those that make more than 50k can be compared to those that make less to generate a prediction. The results of the Naive Bayes are as follows:
ACC: 80%
The accuracy is actually quite high and with the sensitivity at 94%, that means the model could find 94% of all the predicted incomes that are more than 50k. Specificity is at 41% meaning that the model could find 41% of all predicted incomes less than 50k. The Naive Bayes was good at predicting those that made more than 50k, but not so much for those that make less than 50k.

I used a Decision Tree because with many variables, the model could split the dataset into smaller models to evaluate the complexity if a person could make more than 50k or not. In this case, the decision tree split relationship into occupation into education followed by their income.
ACC: 84%
The model recorded an 84% accuracy, which is quite high. 


# RESULTS ANALYSIS #
Ranking the algorithms from best to worst:
1. Logistic Regression
2. Decision Tree
3. Naive Bayes

The reason why Naive Bayes was ranked last was because it had the lowest accuracy. I think this attributed to the large dataset and Naive Bayes operates on strong assumptions, so as a result it had a lower accuracy compared to the other models. The decision tree was next best because the data was split up into a binary operation that allowed the decision tree to predict if they made greater than 50k or less than 50k. A binary predictor worked best for the decision tree and as a result the model was able to predict on either binary predictions. Logistic Regression worked the best because it was predicting an income of either >50k or <50k, both of these values converted to a binary to make it easier for the Logistic Regression to predict. The model only had to predict weather, yes they made greater than 50k, or no they didnt make greater than 50k, which is why I think it had such great success. Additionally the reason why I think all the models predicted a low specificity is because their was a greater quantity to predict on for those that made less than 50k than those that made more than 50k. There are fewer occupations and certain degrees that allow the population to make more than 50k, so in that sense this could also explain why there was a high sensitivity and a low specificity. 

All the model scripts were able to learn from the data and this is useful to know because if you wanted to know on certain incomes in a demographic than using these algorithms would be best, if you stuck with a binary prediction for the income. The decision tree would be best if you wanted to observe the breakdown for each attribute, but the logistic regression would be best if you wanted data to tell you if a certain demographic is making a certain income amount. 
