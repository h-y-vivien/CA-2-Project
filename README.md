# CA-2-Project: Analyzing daft.ie share listings in Ireland

### Description

This project is data analysis project created as a submission for module in the postgraduate course "Data Analytics" at Dublin Business School. The objective of assignment is to aquire, pre-process and analyze data. It is up to the students which methods are used to reach the objectives as long as Python is used for the assignment.
If not specified in the notebook files or on this file, then the work was done by the author.

For the source of information, [daft.ie](https://www.daft.ie/) was chosen.

**Why daft.ie ?**

Ireland is facing a major housing crisis for years, the price of houses, apartments and rooms are constantly increasing. This is affecting tenants, a prospective house buyer and landlords. By analyzing daft.ie listings, we want to understand the housing crisis from the perspective of landlords offering rooms on their properties. In order to do that, the following steps are necessary: 

    1. aquire data from daft.ie
    2. clean data set and feature engineering
    3. Data Analysis

### About the dataset

**Website**: daft.ie

According to daft.ie, it is considered to be Ireland's No. 1 Property website, founded in 1997 by Eamonn and Brian Fallon.
daft.ie enables users to create listings/ads for properties. Daft.ie provides 4 main sections: 

    - Buy: ads/listings about properties to buy
    - Rent: ads/ listings about properties to rent
    - Share: ads/ listings about rooms to rent
    - New Homes: ads/ listings about new properties to buy
    
**Date and time of scraping:** 13.04.2024 1:00 am
    
The webscraped dataset only focuses on "Share" listings containing the following informations: 

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

The CSV file is available on: [daft.ie share listings](https://github.com/h-y-vivien/CA-2-Project/blob/main/final_daft_listings.csv)

For more information on how this dataset was created, please check the below.

### Process

#### Data Aquisition
Daft.ie is build in a way, that each listing requires the user to click on the listing to access more information on each room. In order to scrape all the necessary information, the first step is to scrap all "href"/ links leading to each individual listing. Each "href" is saved in a txt file and will be used in a second webscraper, which actually scrapes each individual listing for information.

The process is described in the [Webscraper Notebook](https://github.com/h-y-vivien/CA-2-Project/blob/main/Webscraper.ipynb)

#### Feature Extraction and Data Cleaning
The dataset created needs to be cleaned in order to create new features and conduct data analysis. 

The process is described in [Feature Extraction and Data Cleaning](https://github.com/h-y-vivien/CA-2-Project/blob/main/Feature%20Extraction%20and%20Data%20Cleaning.ipynb)

When the counts of adjectives in each listing were created, the txt files by were used: 

- [english-adjectives.txt](https://gist.github.com/hugsy/8910dc78d208e40de42deb29e62df913) by [hugsy](https://gist.github.com/hugsy)
- [Positive-Adjective-List.txt](https://gist.github.com/Xeoncross/5381806b18de1f395187) by [Xeoncross](https://gist.github.com/Xeoncross)

#### Data Analysis
The data analysis part is split into 3 different notebooks. Each notebook displays the individual data analysis conducted on the dataset. 

- [by Hing Yee Vivien Huynh](...)
- [by Aoife Murphy](https://github.com/h-y-vivien/CA-2-Project/blob/main/Data%20Analysis/AoifeMurphy.ipynb) ([click to here to see her individual contribution report](...))
- [by Arkam Shaikh](https://github.com/h-y-vivien/CA-2-Project/blob/main/Data%20Analysis/ArkamShaikh.ipynb) 


### About the Interactive Mapbox 
The notebook [Interactive Mapbox](https://github.com/h-y-vivien/CA-2-Project/blob/main/Mapbox.ipynb) contains a map with the location of each room offered (only if Latitude and Longitude for address given is available.)

Currently, it is not possible to upload an interactive plotly dash map on github. So in order to deploy to the interactive map the following prerequisites are necessary. 

#### Prerequisites
To create maps with Mapbox, you will need a Mapbox access token. Each access token is personal, this is why my personal token is hidden in the notebook. Therefore, you will need to register on [mapbox.com](https://account.mapbox.com/auth/signin/?route-to=%22https%3A%2F%2Faccount.mapbox.com%2Faccess-tokens%2F%22) and create a personal access token. 

##### Packages

The main packages needed to create the maps are 'dash' and 'plotly'. To install, copy the following code and run it in a Python 3 enviroment.

```
pip install dash
pip install plotly
       
```

##### Deploy interactive map
To gain access to the map, simply run the [Interactive Mapbox](https://github.com/h-y-vivien/CA-2-Project/blob/main/Mapbox.ipynb) and click on blue link.

[run dash](run _dash.jpg)

If done correctly, it should deploy an interactive map: 

[Interactive map](rooms on daft.ie.png)


### Author
- Hing Yee Vivien Huynh - [Github](https://github.com/h-y-vivien) [Linkedin](https://www.linkedin.com/in/hing-yee-vivien-huynh/)

## Group members
- Aoife Murphy - [Github](https://github.com/aoifemurph1) [Linkedin](https://www.linkedin.com/in/aoife-murphy-14b4611a8/y) 
- Mohd Arkam Shaikh

