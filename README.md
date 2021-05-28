# Real Estate Research

We all know that real estate plays an integral role in the U.S. economy. Residential real estate helps provide housing for families, and it happens to be the most significant source of wealth and savings for many people. Also, the home is the most extensive and most expensive purchase a person makes in his or her lifetime. Real estate trends have changed over time, and many factors weigh-in like recession, pandemic, market boom, etc. Therefore, understanding the real estate market is compelling to get more empowered as a buyer or seller.

## Objective

1. To create visualizations using Tableau to understand the various trends in the data and uncover some meaningful insights.

2. To build a price forecast model and determine the direction of future trends for informed decision-making.

## Data Understanding and Source

### Source- https://www.kaggle.com/zillow/zecon

1. The resources collected using Kaggle are state-wise historical data from Zillow with many other features like median rental prices, median prices over different categories of homes, ZHVI, ZORI which is used in the analysis.
2. The price forecasting model will use the past data to forecast the future trend and values. Hence, the dataset requires price data over time to build the price forecast model.

### Reveiw Variables

1. Zillow calculates a Zestimate, an estimate of value for each home. Zestimate is based on a suite of sophisticated “automated valuation models” (AVM). The models are re-trained three times a week based on the latest data, and each home’s Zestimate is updated daily
2. The dataset has the ZHVI (Zillow Home Value Index) and it is defined as the median of all Zestimates in a region or price tier.
3. Zillow Observed Rent Index (ZORI) - A smoothed measure of the typical observed market rate rent across a given region. ZORI is a repeat-rent index that is weighted to the rental housing stock to ensure representativeness across the entire market, not just those homes currently listed for-rent. The index is dollar-denominated by computing the mean of listed rents that fall into the 40th to 60th percentile range for all homes and apartments in a given region, which is once again weighted to reflect the rental housing stock.

## Forecasting Model-- Facebook Prophet

Prophet library utilizes the additive regression model y(t) comprising the following components.

1. Trend - models non-periodic changes.

2. Seasonality - represents periodic changes.

3. Holidays component - contributes information about holidays and events.

Prophet includes the components that need to be considered for real estate price prediction data as there is a trend observed along with some periodic changes in the prices. Also, considering the data available from 1996, the prophet time series forecasting model was chosen for analysis.

## Visualization

Tableau was used to visualize the Zillow data and find some interesting analysis and trends. 

Data cleaning jupyter notebook: Zillow_WB.ipynb
Tableau file: ZillowViz_AllStates_Workbook.twb
Tableau Public link: https://public.tableau.com/app/profile/pratixa3388/viz/ZillowViz_AllStates_Workbook/Zillow_Story

The visualizations include:
**1. Sales Trend (Yearly)** - Real Estate Market showing slightly upward trend for CA, NY, TX and WA. For FL trend seems to be stable.
**2. Listing Price vs Rental Price (Quarterly)** - It basically shows Listing price and Renting price trends. As per the analysis, Both Listing and Renting Price are inline because these both values affected by same factors like Neighborhood, School rating, crime rate for the particular location.
**3. Sales Statistics (Monthly)** - According to the Zillow data Estate Market is going higher during Spring and Summer. This can be attributed to the beginning of the academic year and preferable climate conditions
**4. Zestimate vs Actual Sales Price** - This analysis follows the Law of supply and demand. More Demand tends to rise in the price and more supply price falls. It shows the comparison between ML forecasting value (Zestimate) provided by Zillow and Actual price. Here Zillow's ML seems working for FL, NY and WA. But for CA and TX Zestimate seems bit off, people migration from CA to TX could be one of the reasons for it.
**5. Rental Density** - This geographical Visualization represents Renter Occupied Housing Unit density across USA by color gradient. The highest Rental value is for NY and the second highest one for CA.
**6. Occupation Statistics on Sales** - This map shows Distribution of White-Collar Occupation by county across USA considered as a potential buyers. County LA from CA has the highest numbers of sales among all the county from 5 selected states.

## Folder structure and getting started

1. The website have been created and HTML,CSS and JS in the folder Estate_Analysis_Website
    1. Index.html- Landing page
    2. Overview tab (about.html)- gives an overview of the project
    3. ML Model tab (model.html)- gives the understanding on the model used and various other models considered.
    4. Analysis
      1. Projection Comparison (analysis.html)- The table with the actual and forecast values for states considered is displayed.
      2. Forecast tab (analysis2.html)- Gives the visualizations of forecast until the year 2021.
    5. Visualizations (visualization.html)- Tableau story board.
    6. Teams tab (teams.html)- the members of the project team.
2. State wise data from kaggle is read in Google collaboratory file. Cleaned and converted to 5 dataframes for states CA, WA, NY, FL, TX. Link for the colab is : https://colab.research.google.com/drive/1HENWcPr8fOFXckZIB4u9DlfQLT-_TXFi?usp=sharing
3. Model Training is done in the colab for the 5 datasets and the forecast figures with the projection table is extracted. Link for the colab is : https://colab.research.google.com/drive/191JJ7szyNNE80tcR7YUEAlD5iRO2e-Wj?usp=sharing
4. FOr all the CSV's and the colab notebooks please use the google drive link: https://drive.google.com/drive/u/1/folders/1C20XRGT5dzPwZvMXg2YjwgONHbFVNgyT






