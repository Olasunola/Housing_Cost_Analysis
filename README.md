<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100"/>


# Housing prices in Berlin

Alexander, Lam-Tuyen, Leo, Mayowa

Data Analytics, August 2020, Berlin


## Content

- Project Description
- Questions & Hypotheses
- Dataset
- Database
- Workflow
- Organization
- Links


## Project Description

Berlin housing prices have been increasing drastically for the last decade. We want to determine the average housing price for different neighbourhooods in Berlin by retrieving the data currently advertised online.

Afterwards, we compare our insights with the data we downloaded from kaggle, which is retrieved in April 2020. That way we can find out whether there was any movement in prices since the start of the Corona crisis and now.


## Questions & Hypotheses

1. How much do prices differ in different neighbourhoods (defined by zipcodes) in Berlin? 
We assume the prices near the center being more expensive than the districts further away.
2. Has there been any price movement since the start of the Corona crisis? 
We assume that there might be a slight decrease in prices, since many people are low on budget and the demand for a new apartment might decrease.


## Dataset

1. We downloaded a dataset from kaggle which entails the rental prices in Berlin in April 2020: https://www.kaggle.com/phanindraparashar/germany-housing-rent-and-price-data-set-apr-20?select=apr20_rental_no_duplicates.csv. This dataset entails various features that are not relevant to our purpose, so we extract only the columns of interest.

2. We webscraped from immonet.de. 


## Database

What is the structure of your database? Have you created more than one table and if yes, how are they related to each other?


## Workflow & problems encoutered

We decided on the topic of finding out the current rental prices in Berlin.
We downloaded a dataset from kaggle where the author webscraped from immobilienscout24.de.
To have comparable data we intended to extract data from immobilienscout24 with API. Since we encounted difficulty with the temporary token and authorization issue, we decided to webscrape instead. Facing 405 error even having tried out various walk-arounds, we looked for other websites to scrape from. We started with immowelt.de, but the ads don't follow the same structure, so we could extract data from the sponsored ads, but not from the standard ones. Eventually, we switched to immonet.de and succeeded there.

When we started to do some analysis with the obtained dataset, we realized that each value in our dataset has 41 duplicates, meaning our dataset of over 1k rows has decreased to 25 unique rows. This indicates that we actually scraped from the first page 41 times instead of scraping the 41 pages.

After taking a few deep breaths, we fixed the loop to the extent that it skips the pages where there is an advertisement. Meaning, we loose data of a whole page every 4 pages. We encoutered that problem because our loop doesnt't iterate each item, but only each page. As the result of this data loss, we could retrieve 700+ rows instead of possible 1000+ rows.


## Organization

We used Trello to outline the list of tasks. 

How did you organize your work? Did you use any tools like a kanban board?

What does your repository look like? Explain your folder and file structure.


## Links

Repository: https://github.com/Lsacy/real_estate 
Slides: 

immoscout: https://www.immobilienscout24.de
immowelt: https://www.immowelt.de 
immonet: https://www.immonet.de 

