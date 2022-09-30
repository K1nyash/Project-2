# Project-2
OVERVIEW

In this project i take the role of a data scientist tasked to model the formula of predicting  a price of a house in the northwestern county, King County in Washington State in the United States of America.
The population was 2,269,675 in the 2020 census  making it the most populous county in Washington, and the 13th-most populous in the United States. The county seat is Seattle also the state's most populous city.

BUSINESS & DATA UNDERSTANDING.
The stake holder for this was a real estate firm found in the King county to assist them in price determination.
Using the data “kc_house_data.csv” I am to make the predictive model.

The data has 21597 rows and 20 columns.

I started of with the base model with “price” as the dependent variable and sqft_living as the independent variable. Sqft_living is the square footage of living space in the home. I started with it as it had the highest correlation with price and also showed a linear relationship with price.


Aside sqft_living the other continuous cloumn that I used was sqft_lot which is the Square footage of the lot.
Didn't have as strong of a linear relationship as sqft_living but still maintained a linear relationship. But it was the only one that was not removed after removing the columns that could lead to multicellularity .

From the data, the top ten zip-code area with the largest mean of prices are depicted in the bar graph below. The top being Medina,Washington (98039) followed by Bellevue, Washington (98004).

My approach was that views surrounding a house from the data will greatly affect the price together with the condition of the house.
These were the only categorical data points I used.



MODELING


The base model formula achieved up-to 95% confidence ;

	y = ([282 - 291])Sqft_living + ([-65,400 - -45,000]) USD + 175,000 USD

Multi-linear model of sqft_living with sqft_lot.

	y = ([282 - 291])Sqft_living + ([ -0.3 - -0.05])sqft_lot + ([-65,400 - -45,000]) USD + 175,000 USD


Multi-linear model of sqft_living with sqft_lot with views.

	y = ([259 - 268])Sqft_living - ([-0.41 - -0.23])Sqft_lot + ([143,200 - 9,880])view_Average + ([174,900 - 16,200])view_Fair + ([212,400 - 13,800])view_Good + ([600,900 16,600])view_Excellent - 25,800 USD + 167,100 USD	



REGRESSION RESULTS

From the models created , I have decided to favor Multi-linear model of sqft_living with sqft_lot with views.

Since it explained the largest percentage, about 60% of the variance observed in price variable.


CONCLUSION.
Despite the formula I favor, the errors are still probable and for a more accurate prediction of the price I recommend the real estate firm to create models for each zip uniquely as they have different pricing per zip-code with the highest being Medina,Washington (98039) with a mean price of 2,215,069 $ and the lowest zip-code  Auburn, Washington  (98002) with a mean price of  233,924 $.
