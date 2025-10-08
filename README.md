# VOIS_AICTE_Oct2025_SydelWivelAfonso

It looks like you've been working on a data analysis project for Airbnb open data! That's great. A good README file will help others understand your project, its goals, and your findings.

Here is a suggested README.md structure based on the provided Python notebook code and outputs.

Airbnb Open Data Analysis
Overview
This project analyzes publicly available Airbnb open data to uncover trends and relationships within the dataset. The analysis covers key areas such as listing distribution, pricing, host performance, and property characteristics.

Dataset
The analysis uses the 1730285881-Airbnb_Open_Data.xlsx file, which was loaded into a pandas DataFrame.

Tools and Libraries
The following Python libraries were used for data cleaning, processing, and visualization:

numpy

pandas

matplotlib.pyplot

seaborn

plotly.express

Data Cleaning and Preprocessing
The initial dataset underwent several cleaning and preprocessing steps to ensure data quality and consistency:

Duplicate Handling: Duplicate records were identified and removed.

Column Removal: Irrelevant columns (house_rules and license) were dropped.

Data Type Conversion and Cleaning:

Price and service fee columns were cleaned by removing $ and , symbols and converted to a float data type.

These columns were renamed to price_$ and service_fee_$ for clarity.

Other columns were converted to appropriate types: id and host id to string, last review to datetime, and Construction year to int.

Data Imputation/Removal: All remaining rows with any missing values (NaN) were dropped.

Outlier Handling: Outliers were removed from the availability 365 column by dropping records where the value was greater than 500.

Data Correction: A spelling mistake in the neighbourhood group column (brookln) was corrected to 'Brooklyn'.

Key Findings & Visualizations
The analysis addressed several key questions, yielding the following results:

1. Property Types and Their Count
The bar chart showed the distribution of room types:

Entire home/apt and Private room are the most common listing types, with 44,161 and 37,474 listings respectively.

Shared room (1,646) and Hotel room (108) are significantly less frequent.

2. Neighbourhood Group with the Highest Number of Listings
The count of listings by neighbourhood group is:

Neighbourhood Group	Count
Brooklyn	34,621
Manhattan	34,560
Queens	11,124
Bronx	2,267
Staten Island	816
brookln (uncorrected)	1

Export to Sheets
Brooklyn has the highest number of listings, followed closely by Manhattan.

3. Average Price by Neighbourhood Group
The average price for listings across the neighbourhood groups:

Manhattan has the highest average price per listing.

4. Relationship Between Construction Year and Price
The line plot suggests an inverse relationship between the average price and the construction year, meaning older buildings tend to have a higher average price.

5. Host Identity Verification and Review Rate
Host Identity Verified	Average Review Rate Number
verified	3.28
unconfirmed	3.27

Export to Sheets
Verified hosts have a slightly higher average review rate than unconfirmed hosts, but the difference is minimal.

6. Correlation Between Price and Service Fee
The correlation coefficient between price_$ and service_fee_$ is approximately 0.99999.

This indicates an extremely strong positive linear correlation, suggesting the service fee is calculated as a direct percentage or fraction of the listing price.

7. Average Review Rate by Neighbourhood Group and Room Type
The average review rate varies by both location and room type.

Brooklyn has the highest average review rate for a Hotel room (3.83).

The single Private room entry in the uncorrected brookln neighbourhood group has the highest rate (4.0). For corrected and populated groups, Private rooms on Staten Island (3.49) have a high average.

Overall, review rates across most of the major neighbourhood groups and room types cluster between 3.2 and 3.4.

8. Top 10 Hosts by Listing Count
Host Name	Calculated Host Listings Count
John	117,175
David	104,136
Alex	95,958
Michael	72,130
Sarah	60,394
Jessica	55,274
Maria	54,618
Kazuya	52,260
Daniel	51,902
Lisa	48,154

Export to Sheets
John is the host with the most listings by a significant margin.
