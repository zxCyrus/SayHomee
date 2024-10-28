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
To to view the dynamic heat map, please use [this link](https://nbviewer.org/github/zxCyrus/SayHomee/blob/main/notebooks/SayHomee%20Data%20Sciencec%20Challenge.ipynb) by nbviewer.
The heat map is rendered by folium, which is not natively supported by GitHub. If you want to view the dynamic heat map, see the Model notebook.
This is a screenshot of the heat map.
<img width="976" alt="Screen Shot 2024-10-28 at 12 30 59 AM" src="https://github.com/user-attachments/assets/ec95ea4a-b853-4086-b6f4-6b569e7c7a60">

## Pacakge required
folium for the geo heat map. Installation pip install folium.
Other common packages: warnings, pandas, numpy, matplotlib, seaborn, sklearn, datetime

## Dataset Description
This dataset contains house listing sale prices for Greater Los Angeles Area. As you can see from my chosen parameters, I scraped house listing for sale from 2024-04-01 till 2024-10-25. The dataset is scraped from realtor using HomeHarvest library.

Along with list price (target/dv) it consists of other 56 house features: Certainly! Here’s the general dataset description:
1. **property_url**: URL link to the listing on Realtor.com.
2. **property_id**: Unique identifier for each property.
3. **listing_id**: Unique ID for each listing instance.
4. **mls**: Multiple Listing Service (MLS) identifier, indicating the source MLS.
5. **mls_id**: MLS-specific ID for each listing.
6. **status**: Current status of the listing (e.g., "FOR_SALE").
7. **text**: Description of the property.
8. **style**: Style or type of the property (e.g., "MULTI_FAMILY," "SINGLE_FAMILY").
9. **full_street_line**: Full address line.
10. **street**
11. **unit**
12. **city**
13. **state**
14. **zip_code**
15. **beds**: Number of bedrooms.
16. **full_baths**: Number of full bathrooms.
17. **half_baths**: Number of half bathrooms.
18. **sqft**: Square footage of the interior living space.
19. **year_built**: Year the property was originally built.
20. **days_on_mls**: Number of days the property has been listed on the MLS.
21. **list_price**: Current listing price.
22. **list_price_min**: Minimum list price
23. **list_price_max**: maximum list price
24. **list_date**: Date when the property was listed.
25. **sold_price**: Price at which the property was last sold, if available.
26. **last_sold_date**: Date of the last sale of the property.
27. **assessed_value**: Tax-assessed value of the property.
28. **estimated_value**: Estimated market value of the property.
29. **new_construction**: Indicates if the property is a new construction.
30. **lot_sqft**: Square footage of the lot.
31. **price_per_sqft**: Price per square foot of the property.
32. **latitude**: Geographic coordinates
33. **longitude**: Geographic coordinates 
34. **neighborhoods**: Neighborhood information: e.g. Central LA, Silver Lake, Central LA, Hollywood Hills	
35. **county**: County where the property is located.
36. **fips_code**: FIPS (Federal Information Processing Standards) code for location.
37. **stories**: Number of stories in the building.
38. **hoa_fee**: Homeowners Association fee, if applicable.
39. **parking_garage**: Information on garage parking availability.
40. **agent_id**: Details of the listing agent
41. **agent_name**: Details of the listing agent
42. **agent_email**: Details of the listing agent
43. **agent_phones**: Details of the listing agent
44. **agent_mls_set**: Details of the listing agent
45. **broker_id**: Brokerage company info
46. **broker_name**: Brokerage company info
47. **builder_id**: Builder details
48. **builder_name**: Builder details
49. **office_id**: Info about real estate office managing the listing
50. **office_mls_set**: Info about real estate office managing the listing
51. **office_name**: Info about real estate office managing the listing
52. **office_email**: Info about real estate office managing the listing
53. **office_phones**: Info about the real estate office managing the listing.
54. **nearby_schools**: Nearby schools' information.
55. **primary_photo**: URLs to primary photos of the property.
56. **alt_photos**: URLs to alternate photos of the property.

## Conclusions
<img width="381" alt="Screen Shot 2024-10-28 at 12 36 36 AM" src="https://github.com/user-attachments/assets/7d96216e-d840-4f7a-853e-032e09414b96">
<br>
Linear Regression: Choose linear regression when simplicity is key and there’s no clear need for penalizing coefficients
Lasso Regression (Best for Sparsity): Choose Lasso when prioritizing a simpler model with fewer less-impactful features (coefficients closer to zero).
Ridge Regression (Best for Collinearity): Choose Ridge when suspecting collinearity between predictors but want to retain all features
My Model Choice: Since I prefer features simplicity, I choose Lasso as my final model
