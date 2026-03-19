# Introduction
This project documents an automated data pipeline built for a luxury watch reseller to track auction market prices. The system collects daily auction data, processes it into structured datasets, and delivers it through Google Sheets document and Tableau dashboard used for purchasing and resale decisions.
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
* End users interact with data through both Google Sheets and Tableau.
* Custom filters and formulas in Google Sheets enables easy price tracking for non-tech users.
* Averages and accesible watch images through Tableau Dashboard.

## Dataset
* ~250 auctions collected daily
* 50.000+ total auction records
* Continuously growing dataset
### Key fields include:
* Watch brand and model
* Final bidded price
* Whether seller accepted the price
* Date 
* Images of the watch
* Other fields requested by the client
## Systems Key Features
* Fully automated data collection pipeline
* Continuous dataset growth with historical tracking
* User friendly Google Sheet document and Tableau dashboard.
* Custom filters for quick exploration
* Interactive dashboard for different price and time ranges.
* Designed specifically for non-tech end users
## Usability
### Google Sheets
* Custom made filtering bars for brand and model
* Dropdown choice list for sorting
* Evaluate historical sales data
### Tableau Dashboard
* Dropdown price and time period choice list for easy filtering
* Dropdown brands section
* Interactive models and ads section
* Images section for easy recognition
## Business Impact
The system is actively used by the seller to support operations. It enables:
* Evaluation of comparible sales before purchasing
* More informed buying and selling decisions.
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
* Expand analysis and visulization capabilities
## Final Thoughts
This is a special project in my career, till now I have always felt like I was lacking in entrepreneurship. Seeing an obvious problem and delivering a working solution for a real client both increased my self-confidence in my tech skills and my soft skills.


