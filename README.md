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

How much do prices differ in different neighbourhoods (defined by zipcodes) in Berlin? Has there been an increase or decrease in housing prices compared to the start of the Corona crisis? We assume that there might be a slight decrease in prices, since many people are low on budget and the demand for a new apartment might decrease.


## Dataset

1. We downloaded a dataset from kaggle which entails the rental prices in Berlin in April 2020: https://www.kaggle.com/phanindraparashar/germany-housing-rent-and-price-data-set-apr-20?select=apr20_rental_no_duplicates.csv 

2. We webscraped from immonet.de. This dataset entails various features that are not relevant to our purpose, so we extract only the columns of interest.


## Database

What is the structure of your database? Have you created more than one table and if yes, how are they related to each other?


## Workflow

We decided on the topic of finding out the current rental prices in Berlin.
We downloaded a dataset from kaggle where the author webscraped from immobilienscout24.de.
To have comparable data we intended to extract data from immobilienscout24 with API. Since we encounted difficulty with the temporary token and authorization issue, we decided to webscrape instead. Facing 405 error even having tried out various walk-arounds, we looked for other websites to scrape from. We started with immowelt.de., but the ads seem not to follow the same structure, therefore we switched to immonet.de.


## Organization

We used Trello to outline the list of tasks. 

How did you organize your work? Did you use any tools like a kanban board?

What does your repository look like? Explain your folder and file structure.



## Links

Include links to your repository, slides and kanban board. Feel free to include any other links associated with your project.

Repository: https://github.com/Lsacy/real_estate 
Slides
Trello

