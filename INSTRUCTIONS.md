# Web scraping

In this project, we are going to obtain and analyze data about Tesla's profit, which we will previously store in a DataFrame and in a sqlite database.

## Step 1: Install dependencies

Make sure you have the Python `pandas` and `requests` packages installed to be able to work on the project. In case you do not have the libraries installed, run them in the console:

```bash
pip install pandas requests
```

## Step 2: Download HTML

The download of the HTML of the web page will be done with the `requests` library, as we saw in the module theory.

The web page we want to scrape is the following: [https://ycharts.com/companies/TSLA/revenues](https://ycharts.com/companies/TSLA/revenues). It collects and stores information about the growth of the company every three months, since June 2009. It stores the text scraped from the web in some variable.


## Step 3: Transform the HTML

The next step to start extracting the information is to transform it into a structured object. Do this using `BeautifulSoup`. Once you have interpreted the HTML correctly, parse it to:

1. Find all the tables.
2. Find the table with the quarterly evolution.
3. Store the data in a DataFrame.


## Step 4: Process the DataFrame

Next, clean up the rows to get clean values by removing `$` and commas. Remove also those that are empty or have no information.


## Step 5: Store the data in sqlite

Create an empty instance of the database and include the clean data in it, as we saw in the database module. Once you have an empty database:

1. Create the table.
2. Insert the values.
3. Store (`commit`) the changes.


## Step 6: Visualize the data

What types of visualizations can we make? Suggest at least 3 and plot them.