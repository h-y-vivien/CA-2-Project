# CA-2-Project: Analyzing daft.ie share listings in Ireland

### Description

This project is 




### About the dataset
**Website**: daft.ie
According to daft.ie, it is considered to be Ireland's No. 1 Property website, founded in 1997 by Eamonn and Brian Fallon.
daft.ie enables users to create listings/ads for properties. Daft.ie provides 4 main sections: 
    - Buy: ads/listings about properties to buy
    - Rent: ads/ listings about properties to rent
    - Share: ads/ listings about rooms to rent
    - New Homes: ads/ listings about new properties to buy
    
**Date and time of scraping:** 13.04.2024 1:00 am
    
The webscraped dataset only focuses on "Share" listings contains the following informations: 

- **"Address":** address of the room
- **"Room":** specifies whether the room has single, double or is twin or shared room. A listing can advertise multiple rooms in a house or apartment.
- **"Bath":** specifies whether the room has an en-suite bathroom or the bathroom is shared between housemates.
- **"Property_type":** specifies whether the property is a house or an apartment
- **"Bedrooms_available":** specifies how many bedrooms are available on the property
- **"Available_from":** specifies when the room is available to move in to.
- **"Available_for":** specifies how long the room is available for.
- **"Sharing_with":** specifies how many people currently live on the property.
- **"Owner_occupied":** specifies whether the owner lives on the property or not.
- **"Preferences":** specifies which gender is preferred for room.
- **"Date_entered/renewed":** displays the date when the listing was first entered/ renewed.
- **"Property_views":** displays how many times the listing has been viewed.
- **"Latitude":** Latitude of the address.
- **"Longitude":** Longitude of the address.
- **"Pre_processed_desc":** description of the listing after Text Pre-processing.
- **"Desc_length":** word count for the description before text pre-processing.
- **"Price_per_month":** renting price for the room per month.
- **"County":** the county in which the room is located.
- **"adjective":** number of adjectives used in the description

#### Interactive Mapbox 
Currently, it is not possible to upload an interactive plotly dash map on github. So in order to deploy to the interactive map the following prerequisites are necessary. 

###### Prerequisites
To create maps with Mapbox, you will need Mapbox access token. Each access token is personal. Therefore, you will need to register on [mapbox.com](https://account.mapbox.com/auth/signin/?route-to=%22https%3A%2F%2Faccount.mapbox.com%2Faccess-tokens%2F%22) and create a personal access token. 

###### Packages

The main packages needed to create the maps are 'dash' and 'plotly'. To install, copy the following code and run it in a Python 3 enviroment.

```
pip install dash
pip install plotly
       
```
#### Process

##### Webscraper 

##### Feature Extraction and Data Cleaning

##### Data Analysis

### Authors
- Hing Yee Vivien Huynh - [Github](https://github.com/h-y-vivien) [Linkedin](https://www.linkedin.com/in/hing-yee-vivien-huynh/)

See the list of group project members 
    
