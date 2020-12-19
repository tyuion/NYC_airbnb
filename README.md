# Note
This is the second version of this notebook. In this version, I
1. add more analysis, such as the top 10 neighbourhoods with the most listings and the top 10 most and least expensive neighbourhoods in Manhattan and Brooklyn, in the data exploratory analysis section.
2. add Ridge Regression, Lasso Regression, grid search, and feature importance study in the data modeling section.
3. update code and add some other discussions.

# Motivation

Airbnb has been widely used these days by people for traveling. Here, I explore the NYC Airbnb dataset to get some insights, especially for the following questions:

1. What is the status of the Airbnb market in NYC?
2. Which factors affect the price?
3. Can we predict the price?

# Dataset
The dataset is from Kaggle (https://www.kaggle.com/dgomonov/new-york-city-airbnb-open-data). It has around 49,000 observations with 16 columns. 

# Documents
There are two files in the repository. NYC_airbnb_v2.ipynb is the Jupyter notebook regarding the data analysis, visualization, and predication. AB_NYC_2019.csv is the dataset used in this project.

# Libraries
Libraries used in this work include NumPy, Pandas, Matplotlib, Seaborn, Wordcloud, and Sklearn.

# Conclusions

1. What is the status of Airbnb market in NYC?¶
- Most of the listings in NYC are in Manhattan and Brooklyn. Both of them have more than 20,000 listings, which are over 85% of the overall listings. The neighbourhood with the most listings is Williamsburg in Brooklyn. 
- Around 52% of listings are entire home/apt, and 45% are private room. Only 2% are shared rooms. Among different neighbourhood groups, Brooklyn has the most private rooms, while Manhattan has the most entire homes/apts.
- The median price in Manhattan is ~$150, which is much higher than other neighbourhood groups (less than $100). 
- The top 10 most expensive neighbourhoods in Manhattan are between $200 to $300. The most expensive neighbourhood is Tribeca. The top 10 least expensive neighbourhoods in Manhattan are between $70 to $130. The cheapest neighbourhood is Washington Heights.
- The availability is lower in Brooklyn and Manhattan compared to other locations.
- Some words are quite popular in the name such as 'private', 'beautiful', 'cozy', 'modern', and 'quiet'. 

2. Which factors affect the price?
- Location: The price in Manhattan is much higher than in other locations.
- Room type: The entire home/apt is much more expensive than the private room and shared room. The private room is slightly more expensive than the shared room.
- Host listings count: It looks like the listings that the calculated_host_listings_count equals to 1 are more expensive.
- Minimum nights: No clear trend.
- Availability: No clear trend.

3. Can we predict the price?
- Five models are used to predict the price: Linear Regression, Ridge Regression, Lasso Regression, Decision Tree, and Random Forest. Random forest gives a better result than other models.
- Grid search is used to improve the model further. The best model gives an R2 score of 0.561.
- According to the model, the most important features are room type and location.

The main findings can also be found at my medium post (https://medium.com/@tyuion1215/newyorkcity-airbnb-data-analysis-visualization-and-predication-8397943066f9)

# Acknowledgement
Must give credit to Kaggle for the data (https://www.kaggle.com/dgomonov/new-york-city-airbnb-open-data).
