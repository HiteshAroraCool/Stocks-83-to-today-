# Stocks 1983 to Today: Data Analysis of Stock Correlation to Inflation
This project focuses on analyzing the correlation between stock market indices and inflation in various countries. The data is collected from WorldBank.org for inflation data and Google Finance for stock details of indices and companies. Python notebooks are used for data cleaning and extraction, and Tableau is used for data analysis.

## Data Collection
* Stock data for various companies is obtained from Google Finance using the googlefinance() function and stored in an .xlsx file format. The stock data is categorized into individual sheets for each company, containing daily data from the beginning of data collection up to March 2023, including opening, high, low, and closing prices, as well as trading volume. The prices are denominated in the local currency of the respective country.
* Alongside the stock data, two other files are used: the Inflation Consumer Prices (Annual %) and Wholesale Price Index (2010 = 100).
* The Wholesale Price Index is a measure of the average price of a basket of goods and services in a given economy, including both agricultural and industrial goods at various stages of production and distribution. The Laspeyres formula is typically used to calculate the index.
* The Inflation Consumer Prices (Annual %) file measures the annual percentage change in the cost to the average consumer of acquiring a basket of goods and services. The basket may be fixed or changed at specified intervals, such as yearly. The Laspeyres formula is typically used to calculate the index. Both of these files provide valuable context for understanding the performance of the stock market and the broader economic conditions that may be affecting it.
## Data Analysis Process
* The Excel file with stock data is updated automatically using the "Recalculation" setting in Google Sheets, which updates the TODAY() function in the formula "=GOOGLEFINANCE(company, "all", "1/1/1980", TODAY())".
* Initially, attempts were made to use the data from Google Sheets directly in the notebook using the gspread library, but due to errors, the traditional download and upload method was used.
* The WorldBank.org file with inflation data was cleaned and uploaded to Kaggle, and any empty rows were removed using Excel to avoid issues with Kaggle's data upload process.
* A custom function was created in Python to properly format and clean the data from both the stock and inflation datasets, including transposing the DataFrame, dropping empty rows, and renaming columns.
* Data was extracted only for the countries of interest and stored in separate dataframes.
* The same procedure was followed for extracting stock data from sheets of indices and companies for India and the USA, and concatenating the 'close' column with Date as the index in the dataframes, with columns set as stock names.
* Finally, the cleaned and formatted dataframes were downloaded for further analysis in Tableau.
# Findings
(You can write about your findings in this section.)

## Kaggle Links
* Notebook link: https://www.kaggle.com/code/bcscuwe1/stocks-83-today
* Dataset link: https://www.kaggle.com/datasets/bcscuwe1/stocks83-today
* Drive Stocks file link: https://docs.google.com/spreadsheets/d/1ElCXYXv-NjAmMKy7fQ1bjI05q1xij5hZ2DCLrJs0A5w/edit?usp=share_link
