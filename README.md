# Spring-2021-capstone-

This project focuses on the effects of company financial information on the scale at which they report (i.e.ones, thousands, millions of dollars). Specifically, the focus was to determine why companies switch from one reporting denomination to another. The analyis of the problem was done through both exploratory data analysis and predictive modeling. The data was pulled from the SEC edgar database. The files in this README contain the code used in the completion of this project from data collection to modeling. 

## Files

### Data-collection
This notebook contains the steps taken to pull the data from the SEC database and put it in a dataframe. The final product is three dataframes contain information from balance sheets, income statements, and statements of cash flows. 

### Data-cleanining
Once the data had been collected it was cleaned in order for further analysis to be performed. The cleanining was done at the individual statement level as well as after merging the three dataframes. Key cleaning steps were to remove unneccessary rows and convert some columns to numerical values. 

### Feature-engineering
Three features were added to the merged dataframe:
- Switch - the size of the switch (i.e. ones to thousands) a company made from one period to the next
- Switch type - the movement of the switch  (i.e. up or down)
- Numerical changes - changes from one period to the next of the numerical columns

### EDA
Assets and net income were explored further by doing exploratory data analysis. They were compared to scale, switch type, and each other. This was done to determine which features would be most useful in  creating a model. 

### Modeling
Modeling was done through two approaches:
- Including the change columns
- Not including the change columns

This was done to see if these columns had any predictive value or if total assets and net income were enough to make predictions. Random forest classifiers and decision tree classifiers were used in each approach to try and predict the type of switch a company would make. 
