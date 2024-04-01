<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100"/>


# Rental prices in Toronto

Alexander, Olasunkanmi, Lam-Tuyen, Leo, Mayowa

Data Analytics, August 2020, Toronto


## Content

- Project Description
- Questions & Hypotheses
- Dataset
- Database
- Workflow
- Organization
- Links


## Project Description

Toronto housing prices have been increasing drastically over the last decade. In this project, we aim to determine the average rental price for different neighbourhooods in Toronto defined by zipcodes. We then compare insights gained from our retrieved data with the a dataset from kaggle, which reflects rental prices in April 2020. That way we can find out whether there was any price movement since the start of the Corona crisis.


## Questions & Hypotheses

1. How much do prices differ in different neighbourhoods (defined by zipcodes) in Toronto? 
We assume the rental prices near the city center being more expensive than the districts further away.
2. Has there been any price movement since the start of the Corona crisis? 
We assume that there might be a slight decrease in prices, since many people are low on budget and the demand for a new apartment might decrease.


## Dataset 

1. We downloaded a dataset from kaggle which contains the rental prices in Toronto in April 2020: https://www.kaggle.com/phanindraparashar/Canada-housing-rent-and-price-data-set-apr-20?select=apr20_rental_no_duplicates.csv. This dataset comprises various features that are not relevant to our purpose, therefore we extract only the columns of interest.

2. We webscraped from immonet.de. 


## Database

We have 3 datasets:
immoscout is the dataset we downloaded from kaggle.
immonet is the dataset we retrieved through webscraping.
WE also merged both of them into one common dataset for better comparison and calculation.


## Workflow & problems encoutered

We decided on the topic of finding out the current rental prices in Toronto.
We downloaded a dataset from kaggle where the author webscraped from immobilienscout24.de. To have comparable data, we intended to extract data from immobilienscout24 via API. First, we encounted problems with the temporary token and authorization. Later, after some success with accessing the data through the API sandbox playground, we found out in order to get full datasets we have to pay. So we changed our strategy to webscrape instead. 

Facing 405 error (anti-scraping bots) even after having tried out various walk-arounds, we looked for other websites to scrape from. We chose immowelt.de, but faced similiar problems. Eventually, we switched to immonet.de and after a few attemps we managed to gather the data from there.

When we started to do some analysis with the obtained dataset, we realized that each value in our dataset has 41 duplicates, meaning our dataset of over 1,000 rows has decreased to 25 unique rows. This indicates that we actually scraped from the first page 41 times instead of scraping the 41 pages. 

We fixed the scraping loop to the extent that it skips the pages whereever there is an advertisement. Meaning, we loose data of a whole page every 4 pages. We encoutered that problem because our loop didn't iterate each item, but only each page. As the result of this data loss, we could retrieve 700+ rows instead of possible 1000+ rows.

After consultation with the TA, we managed to rewrite the scraping code, so that no more data was lost due to the page structure issue. Instead of scraping from the 41 search result pages, we scraped from the subpages, thus from every individual rental object page. That means we were scraping from over 1000 pages, with each page representing one single individual rental object in Toronto.


## Organization

Our Github contains 3 datasets: immoscout from April 2020 (downloaded), immonet from April 2020 (webscraped) and one merged one. 
It also contains 3 files of codes: webscraping, data cleaning and data analysis.


## Links

Repository: https://github.com/Lsacy/real_estate 

Slides: https://slides.com/lam-tuyen/deck

immoscout: https://www.immobilienscout24.de, 
immowelt: https://www.immowelt.de, 
immonet: https://www.immonet.de 

