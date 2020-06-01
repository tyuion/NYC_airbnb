# Motivation

Airbnb has been widely used these days by people for traveling. Here, I try to explore the NYC airbnb dataset to understand the airbnb market in NYC. In particular, to get some insights regarding the following questions:
1. What is the difference among the neighbourhood of NYC?
2. Which factors affect the price?
3. Can we predict the price?

# Dataset
The dataset is from Kaggle (https://www.kaggle.com/dgomonov/new-york-city-airbnb-open-data). It has around 49,000 observations with 16 columns. 


# Documents
There are two files in the repository. NYC_airbnb.ipynb is the Jupyter notebook regarding the data analysis, visualization and predication. AB_NYC_2019.csv is the dataset used in this project.


# Libraries
Libraries used in this work include numpy, pandas, matplotlib, seaborn, wordcloud, and sklearn.

# Conclusion
1. The listings show a clear difference among the neighbourhoods of NYC, incuding the numbers of listing, room type, availability,
and price.
2. The price is mainly affected by the location and room type. Meanwhile, there are interesting correlations between price and 
some other features (e.g., the minimum_nights, calaculated_host_listings_count).
3. The price is predicted using three different models: linear regression, decision tree, and random forest. Random forest give the best result with a R2 score of 0.44. The score is still not high. It might because the features used are not quite correlate with the price. More features are needed for a better result.
