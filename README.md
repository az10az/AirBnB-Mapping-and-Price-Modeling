# AirBnB-Price-Modeling
AirBnB Price Modeling of San Francisco, San Diego, and Los Angeles rentals using Multiple Linear Regression in scikit-learn. Visualizations were created in Bokeh. 

## San Francisco AirBnB Listings
![ScreenShot](https://github.com/az10az/AirBnB-Price-Modeling/blob/master/bokeh_plot-3.png)

## Los Angeles AirBnB Listings
![ScreenShot](https://github.com/az10az/AirBnB-Price-Modeling/blob/master/bokeh_plot-2.png)

## San Diego AirBnB Listings
![ScreenShot](https://github.com/az10az/AirBnB-Price-Modeling/blob/master/bokeh_plot.png)

# Overall Summary:
In this project, I built a MLR model to predict AirBnB listing prices for listings in San Francisco, Los Angeles, and San Diego. I was able to iteratively build and improve several models that provided a decent R^2 value of approximately 0.4. When analyzing cities individually, I had more success with San Diego, achieving an R^2 value of approximately 0.6, but this could not be achieved with the other cities. Overall, while this model produces a reasonable estimate of price, particularly at the lower end of the price range, owners with homes above 1000 dollars would not be wise to use this model. Owners in the San Diego area would receive considerable benefit from applying this model to their pricing strategy, as the mean absolute error was just 60 dollars. Additional feature engineering as shown in this project, would continue to improve the model performance.
This project allowed me to utilize my instruction in Python as well as several of the major data science packages / libraries to conduct an analysis on a typical type of problem that a company like AirBnB routinely develops solutions for.

# Limitations:
Estimating rental prices is a difficult challenge because the target variable is subject to hundreds of variables. A MLR model is appropriate for linear relationships between the target and input variables. However, it is likely that price does not follow linear relationships for many variables. This negatively impacts the ability of an MLR model to produce reliable predictions. I believe this may have happened in my model, as the error terms grew drastically at the higher end of the price range, with the linear regression model being unable to properly fit the more opulent rentals. In such cases, a different statistical approach may be more appropriate.
One major limitation in the dataset is that price is variable on most AirBnB listings. Owners generally adjust their prices based on day of the week and time of the year, and this data is not available from the current dataset. Removing this seasonality and variability on pricing would certainly allow for a more robust model, as this model currently assumes that pricing is uniform for a particular listing.
Perhaps the most prohibitive limitation in this dataset is the impact an owner can have on the price of a listing based on their actual revenue desires. Most owners will try to maximize revenue, but there are many factors that determine whether the full revenue potential of a listing is reached. For example, some owners perform their own cleaning and must factor in time when evaluating the price they will place on their listing. An experienced owner, as well, may have had more time to finely tune their pricing than an inexperienced one. Over time, such an owner would gravitate towards improved yield, which may or may not be associated with higher or lower price in the listing. It is very difficult to ascertain from the data whether these factors exist and to what degree they play a role in listing price.
# Areas to Extend:
This model may improved by identifying stronger features. A future direction of this project would be to employ Principal Component Analysis to identify classifiers for segments of the listing data. For example, PCA would be well-suited to identify homes that are actually wedding venues or part of a specific region or area that is not captured by the current dataset as a city or neighborhood value. Implementation of these features, as shown in the project, would continue to improve the model performance.
Other area of improvement would include:
Rate listing descriptions based on sentiment analysis.
Creation of more features such as length of listing description or number of amenities
Include economic data from other data sources (homes for sale, average salaries, etc. in an area).
Develop a yield-based model that includes expected yearly revenue for a listing.
