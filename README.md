# SayHomee DS Challenge
## Model and Analysis: 
Exploratory data analysis and price prediction on Greater Los Angeles area house listing price dataset scraped from realtor.com. The complete analysis can be found in [this Jupyter Notebook](https://github.com/zxCyrus/SayHomee/blob/main/notebooks/SayHomee%20Data%20Sciencec%20Challenge.ipynb) in the notebook folder. 
	- The notebook also included some important visualization to demonstrate the dataset values and stats details
	- Model used: Multiple Linear Regression, Lasso Regression, Ridge Regression
 

## Scraped Raw Data: 
The raw scraped dataset can be found in the data folder. I utilized the open-source [HomeHarvest](https://github.com/Bunsly/HomeHarvest) Python library to scrape housing listing data from [realtor.com](https://www.realtor.com/)

## Slide: 
A concise slide presentation can be found in the presentation folder

## House Listing Heatmap
The heat map is rendered by folium, which is not natively supported by GitHub. If you want to view the dynamic heat map, see the Model notebook.
This is a screenshot of the heat map.
<img width="976" alt="Screen Shot 2024-10-28 at 12 30 59 AM" src="https://github.com/user-attachments/assets/ec95ea4a-b853-4086-b6f4-6b569e7c7a60">

## Pacakge required
folium for the geo heat map. Installation pip install folium.
Other common packages: warnings, pandas, numpy, matplotlib, seaborn, sklearn, datetime

## Dataset Description
This dataset contains house listing sale prices for Greater Los Angeles Area. As you can see from my chosen parameters, I scraped house listing for sale from 2024-04-01 till 2024-10-25. The dataset is scraped from realtor using HomeHarvest library.

Along with list price (target/dv) it consists of other 56 house features: Certainly! Here’s the general dataset description:
property_url: URL link to the listing on Realtor.com.
property_id: Unique identifier for each property.
listing_id: Unique ID for each listing instance.
mls: Multiple Listing Service (MLS) identifier, indicating the source MLS.
mls_id: MLS-specific ID for each listing.
status: Current status of the listing (e.g., "FOR_SALE").
text: Description of the property.
style: Style or type of the property (e.g., "MULTI_FAMILY," "SINGLE_FAMILY").
full_street_line: Full address line.
street
unit
city
state
zip_code
beds: Number of bedrooms.
full_baths: Number of full bathrooms.
half_baths: Number of half bathrooms.
sqft: Square footage of the interior living space.
year_built: Year the property was originally built.
days_on_mls: Number of days the property has been listed on the MLS.
list_price: Current listing price.
list_price_min: Minimum list price
list_price_max: maximum list price
list_date: Date when the property was listed.
sold_price: Price at which the property was last sold, if available.
last_sold_date: Date of the last sale of the property.
assessed_value: Tax-assessed value of the property.
estimated_value: Estimated market value of the property.
new_construction: Indicates if the property is a new construction.
lot_sqft: Square footage of the lot.
price_per_sqft: Price per square foot of the property.
latitude: Geographic coordinates
longitude: Geographic coordinates
neighborhoods: Neighborhood information: e.g. Central LA, Silver Lake, Central LA, Hollywood Hills
county: County where the property is located.
fips_code: FIPS (Federal Information Processing Standards) code for location.
stories: Number of stories in the building.
hoa_fee: Homeowners Association fee, if applicable.
parking_garage: Information on garage parking availability.
agent_id: Details of the listing agent
agent_name: Details of the listing agent
agent_email: Details of the listing agent
agent_phones: Details of the listing agent
agent_mls_set: Details of the listing agent
broker_id: Brokerage company info
broker_name: Brokerage company info
builder_id: Builder details
builder_name: Builder details
office_id: Info about real estate office managing the listing
office_mls_set: Info about real estate office managing the listing
office_name: Info about real estate office managing the listing
office_email: Info about real estate office managing the listing
office_phones: Info about the real estate office managing the listing.
nearby_schools: Nearby schools' information.
primary_photo: URLs to primary photos of the property.
alt_photos: URLs to alternate photos of the property.

## Conclusions
<img width="381" alt="Screen Shot 2024-10-28 at 12 36 36 AM" src="https://github.com/user-attachments/assets/7d96216e-d840-4f7a-853e-032e09414b96">
Linear Regression: Choose linear regression when simplicity is key and there’s no clear need for penalizing coefficients
Lasso Regression (Best for Sparsity): Choose Lasso when prioritizing a simpler model with fewer less-impactful features (coefficients closer to zero).
Ridge Regression (Best for Collinearity): Choose Ridge when suspecting collinearity between predictors but want to retain all features
My Model Choice: Since I prefer features simplicity, I choose Lasso as my final model
