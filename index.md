# Boston Housing Analysis 

For this first lab, we are just doing some real quick and easy analyses of a classic dataset to start to come to grips with the tools and techniques of data science. The dataset in question is Boston Housing (which I've found in the course of doing this lab is actually included [directly in scikit!](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_boston.html)), a dataset that includes a solid 506 entries and 17 dimensions.

## The Dataset
The purpose of the boston housing dataset is to predict the price of a given house with the plethora of other information provided, including location, local crime rates, age, tax rate, etc. However, for this analysis we are going to try to predict the price using only one feature variable: the number of rooms. As you can see in this image, there is an easily apparent correlation between these variables that appears to increase fairly linearly.
