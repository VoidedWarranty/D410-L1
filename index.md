# Boston Housing Analysis 

For this first lab, we are just doing some real quick and easy analyses of a classic dataset to start to come to grips with the tools and techniques of data science. The dataset in question is Boston Housing (which I've found in the course of doing this lab is actually included [directly in scikit!](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_boston.html)), a dataset that includes a solid 506 entries and 17 dimensions.

## The Dataset
The purpose of the boston housing dataset is to predict the price of a given house with the plethora of other information provided, including location, local crime rates, age, tax rate, etc. However, for this analysis we are going to try to predict the price using only one feature variable: the number of rooms. As you can see in this image: ![](img1.jpg)

there is an easily apparent linear correlation between these two variables. However, although the general trend is clear, it is equally apparent that the relationship cannot be expressed as a function, as there are many instances in which one specific number of rooms has multiple different prices. Thus, any model solely using this one feature variable is going to contain some degree of error, and we are going to have to try a couple of different regression models to try and maximize our predictive power.

## The Techniques
We are going to analyze this dataset using five general techniques, each of which will be explored more deeply as we cover them.

### Linear Regression
The first model up on the block is a simple linear regression. Linear regressions are just about as simple as you can go, outputting a predictive line in a form just like we learned about in 3rd grade `y=mx+b`, where the slope and intercept are chosen to best fit the data at hand. Simple doesnt always mean bad though, especially in cases like these where the relationship closely follows a linear trend. ![](img2.jpg)

### Locally Weighted Regression
With this second model, we start to get a little bit more complicated. Locally weighted regressions work similarly to linear regressions, but instead of taking the data as a whole, the model instead only uses training data that are local to the point in question. The degree to which different points are weighted in this case is given using a kernel function, which essentially smooths out the weighting based on the function in question. Though pretty much any function could be used as a kernel, the ones that are going to serve a useful purpose generally take this sort of shape: ![](img3.jpg)
and are sized such that they can capture all the points close enough to be useful while excluding those that would snarl the data. I didn't bother including any kernels outside the ones we defined in class, as all three of those gave nearly identical trend lines and MAEs within $20 of each other, as you can see below. ![](img4.jpg)
