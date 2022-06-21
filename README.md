# Project 2 - Ames Housing Data and Kaggle Challenge - Kyle Ness

There are a lot of factors that go into the pricing of residential real estate. Some of these may be obvious and their effects on price well-known, like the total area of a home in square feet or the number of bedrooms and baths the house has. Others, however, may be more abstract or subjectively valued, like whether a house has a masonry veneer or how long the frontage of the house's lot is. Further, there may be many significant interactions between the independent variables of a house that also affect valuation. 

In analyzing the Ames, Iowa housing dataset consisting of 2,051 observations on 80 independent variables for homes sold between 2006 and 2010, it should be possible to arrive at a model that will accurately estimate a given home's sale price despite the complexity of the task. Through discovery of this model, this report seeks to help the average homeowner be more informed about their property's value and valuations in residential real estate markets in general. Success in this pursuit will be determined by coming to a model that outperforms the baseline median sale price model (assumed to have an R^2 value of 0). This best-performing model can then be used by homeowners to predict their own home's potential sale price by plugging in its characteristics. Additionally, this analysis will reveal the most important features in home valuation, which may greatly aid prospective renovators in getting the best bang for their buck.

Linear regression, Ridge regression, and Lasso regression models will be explored. Variants of linear regression models may be looked into by selecting for specific features. 

### Dictionary: http://jse.amstat.org/v19n3/decock/DataDocumentation.txt

### Analysis - Summary
Analysis was conducted on a dataset containing 2,051 observations on 80 features of houses sold in Ames, Iowa. After data cleaning, EDA, and relationship plotting, 4 different regression models were explored, namely: one unscaled, one ridge, and one lasso, each using all independent variables possible, as well as another multiple regression model using only top 10 features most correlated with house sale price. Each of these models were evaluated using R^2 values in the notebook, and later scored on Kaggle using mean squared error. R^2's ranged from ~0.93 to ~0.82 on the test set. The best model was the first multiple regression using unscaled features.

### Conclusion and Recommendations
Out of the four models explored in this analysis, the first multiple regression model incorporating all possible features shared between the train and test sets without any use of scaling appears to perform the best, albeit by a very slight margin over the Lasso CV and Ridge CV models. These models may rank differently using an evaluation metric besides R-squared, but this was not looked into. So, if there is a homeowner in need of help with their valuation, they should be referred to this unscaled multiple regression model. Any of the models created and tested herein would be of better use to a homeowner than simply assuming median sale price (baseline). 

As for recommendations / insights from this data specifically, some of the most important factors in improving sale price for a home seem to be the total area of the home in square feet, the overall quality of the home, the exterior design / maintenance, the size and car capacity of the garage, and how new the house is. Some of these were anticipated in the problem statement. Alas, if a homeowner is aiming to increase the sale value of their home, they should focus most on improving their standing in these features. For example, adding an extension to the house would very likely add value to the home. 

In the future, analysis should be done to see how much value each type of renovation adds to a home's resale value net renovation-related expenses. Such analysis would show what renovations offer the best return on investment for a homeowner. This information would be essential if the renovations are being done solely to boost resale value.

### Datasets Source:
Obtained from Ames, Iowa Assessor’s Office:
"Data set contains information from the Ames Assessor’s Office used in computing assessed values for individual residential properties sold in Ames, IA from 2006 to 2010."