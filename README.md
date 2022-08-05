# Flatiron Phase 2 Project - Jung Lim Fan Club 
~Jordan Mang, Garrett Hall, Charles Pan


## Project Overview

In this project, we have been tasked to analyze the King County, Washington real estate data and provide a business problem as well as a solution based off the data set. Our business problem is that we have a 'client' whos goal is to buy a real-estate lot for the purposes for producing a 3-D Model Home for advertising purposes. They are looking for a real-estate with a great view, poor house condition (for easy tearing down purposes), good location (for decent re-sell value), and a reasonable price estimate. Our primary objective is to offer three recommendations based off our findings, and our secondary objective is to analyze key components in the data that would lead to the three recommendations.


### Approach

We will go attempt to achieve our primary objective in 3 steps.

1. Exploratory Data Analysis (EDA): We will look and analayze the entire data set, and explore the purpose and relation each column has with each other as well as the primary objective. Afterwards, we will trim the unnecessary information, remove or fill null values, convert data from strings to numeric datatypes, investigate correlation through a heat map to find good predictors of price, and create necessary charts to demonstrate relationship or trends in the data/market.

2. Variable Selection: Similar to the prior step, this is where we use the correlation heatmap as well as personal knowledge on the market to pick the dependent and independent variables for our objective. The dependent variable will be price as no other variable is as important since our client has no interest in other features if the price is unreasonable. The independent variables we have chosen based off the heat map were zipcode (location), whether the property has a waterfront or not, square footage of living space, the build quality/grade of the building, and the view. Zipcode has a huge impact on the price and should definitely be on the list as no one wants to spend five million dollars to live in the sticks. Waterfront had a huge impact on the price, and while waterfront increases the price of the property by a lot; we deemed it unnecessary as the cost was a bit too high for our client. The square footage of living space also impacts the price since more land more money, but more importantly we had to find locations with a decent count of larger homes. The build quality of the home also affected price but mostly excellent built homes were well above the cost of others; in our case, we chose lower quality homes for lower-cost basis and easier tear-down. The view was the last variable as our client was looking to use the house for promotional material for their business.

3. Model Accuracy - Our variables we chose had a clear impact on price and we chose to build our model off that. With price as the dependent variable, our model had a R-squared of .751. This means that our model was able to account for 75.1% of the total house market which was decent enough for us. We ran a train-test-split from the model and came out with a lr.score (confidence score) of .747, a mean absolute error of 10,373.82, and a mean squared error of 26335.73. This shows that our training model has a margin of error of around $10,307 dollars.


### The Data

This project uses the King County House Sales dataset, which can be found in  `kc_house_data.csv` in the data folder in this assignment's GitHub repository. Below are the columns in the data set.

* `id` - Unique ID of the house
* `date` - Date the house was sold
* `price` - Price the house was sold at (Prediction Target)
* `bedrooms` - The number of bedrooms
* `bathrooms` - The number of bathrooms
* `sqft_living` - Square footage of living space
* `sqft_lot` - Square footage of the entire lot
* `floors` - Number of floors
* `waterfront` - Whether the house has a waterfront or not
* `greenbelt` - Whether the house has a greenbelt or not
* `nuisance` - Whether the house has a nuisance nearby or not
* `view` - The grade/quality of the view (None/Average/Good/Fair/Excellent)
* `condition` - The condition of the house (Poor/Fair/Good/VGood/Average)
* `grade` - Overall grade based off house build quality (1-12) 
* `heat_source` - The type of heat source the house has (Gas/Oil/Electricity)
* `sewer_systen` - Whether the sewer system is public or private
* `sqft_above` - Square footage above ground
* `sqft_basement` - Square footage in the basement
* `sqft_garage` - Square footage of the garage
* `sqft_patio` - Square footage of the patio
* `yr_built` - The year the house was built
* `yr_renovated` - The year the house was renovated
* `address` - Address
* `lat` - Latitude
* `long` - Longitude

- Insert Dataframe Head -

### Findings and Conclusion



