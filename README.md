# Introduction
This project documents an automated data pipeline built for a luxury watch reseller to track auction market prices. The system collects daily auction data, processes it into structured datasets, and delivers it through Google Sheets document and Tableau Dashboard used for purchasing and resale decisions.
## Overview
While visiting a second-hand luxury watch store, I learned that the business also sells products through online auction platforms. During our discussion, it became clear that they lacked reference points and they were making their purchases and sales through feelings and experience only. Without access to historical pricing data, there was a risk of underpricing items when selling or overpaying when purchasing. Given the niche nature of the market, consistently tracking auction prices is essential for making informed, data-driven decisions.
## My Solution
The solution is an automated pipeline that collects auction data, processes it, and presents it in a user-friendly format:

Automated scraping → Data cleaning → CSV storage → Google Sheets documents → Tableau Dashboard

## Pipeline Architecture    
**1. Data Collection**
* Implemented in Python using Selenium and BeautifulSoup
* Scrapes auction listings and results from online marketplaces.

**2. Scheduling**
* Automated my system with Windows Task Scheduler
* Runs twice daily:
    * Afternoon: collects auctions ending the same day
    * Midday: collects results of auctions that ended previous day.

**3. Data Storage**

* Data is cleaned and structured using Pandas into CSV file.
* Uploaded and updated automatically using Google Sheets AppScript
* Stored in Google Sheets

**4. Data Access**
* End users interact with the data through both Google Sheets and Tableau.
* Custom filters and formulas in Google Sheets enables easy price tracking for non-tech users.
* The Tableau dashboard provides filtering by time period and price ranges, along with a section displaying images of selected watch models

## Dataset
* ~250 auctions collected daily
* 50000+ total auction records
* Continuously growing dataset
### Key fields include:
* Watch brand and model
* Final bid price
* Whether seller accepted the price
* Date 
* Images of the watch
* Other fields requested by the client
## Key Features
* Fully automated data collection pipeline
* Continuous dataset growth with historical tracking
* User-friendly Google Sheets Document and a Tableau Dashboard.
* Custom filters for quick exploration
* Interactive dashboard for different price and time ranges.
* Designed specifically for non-tech end users
## Usability
### Google Sheets
* Custom filtering options for brand and model selection
* Dropdown menus for sorting results
* Evaluate historical sales data
### Tableau Dashboard
* Dynamic filters for time periods (last month, last 3 months, all time)
* Filtering by price brackets
* Interactive sections for models and listings exploration
* Dedicated section displaying images of selected watch models for easier recognition
## Business Impact
The system is actively used by the seller to support operations. It enables:
* Evaluation of comparable sales before purchasing
* More informed buying and selling decisions
* Increase in profit by 10-20% monthly since the start of the project
## Tools Used
* Python (Selenium, BeautifulSoup, Pandas)
* Google Sheets (AppScript)
* Tableau
* Windows Task Scheduler
## Note
The full scraping implementation is private as it was developed for a client. This repo focuses on the pipeline design, data structure, usability and output.
## Future Improvements
* Deploy the pipeline to a cloud environment for improved reliability.
* Store data in a database instead of CSV for scalability
* Expand analysis and visualization capabilities



