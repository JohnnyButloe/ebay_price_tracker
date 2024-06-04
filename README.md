Overview

The eBay Price Tracker is a Python script designed to scrape eBay listings for M1 MacBook Air prices, process the data to remove outliers, calculate the average price, and save this information to a CSV file. The script uses BeautifulSoup for web scraping, NumPy for statistical operations, and the CSV module for file operations.

Features

Scrape Prices from eBay: Extracts prices of M1 MacBook Air listings from eBay search results.
Remove Outliers: Filters out price outliers to provide a more accurate average.
Calculate Average Price: Computes the average price of the listings.
Save to CSV File: Saves the date and average price to a CSV file for record-keeping.

Components

get_prices_by_link(link):
Fetches the HTML content of the provided eBay link.
Parses the HTML to find and extract prices of the listed items.
Returns a list of prices as floats.

remove_outliers(prices, m=2):
Converts the list of prices to a NumPy array.
Removes prices that are more than m standard deviations away from the mean.
Returns the filtered array of prices.

get_average(prices):
Computes the mean of the given list of prices using NumPy.
Returns the average price.

save_to_file(prices):
Gets the current date and formats it.
Rounds the average price to two decimal places.
Appends the date and average price to a CSV file named prices.csv.

Main Execution Block:
Calls the get_prices_by_link function to fetch the prices.
Calls remove_outliers to filter the prices.
Prints the average of the filtered prices.
Saves the average price and the current date to the CSV file.
