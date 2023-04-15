# Stocks 1983 to today
Data Analyst of stock escaly indexs correlation to inflation of country.
Data is collector using Stock prices for various companies are obtained from Google Finance through the utilization of the googlefinance() function, and are stored in an .xlsx file format. The stock data is classified and categorized into individual sheets, which correspond to a specific company. The table contains data for each day from the beginning of data collection up to March 2023, including the opening, high, low, and closing prices for the stock, as well as the volume of trades. The prices are denominated in the local currency of the respective country.
Drive Stocks file link: https://docs.google.com/spreadsheets/d/1ElCXYXv-NjAmMKy7fQ1bjI05q1xij5hZ2DCLrJs0A5w/edit?usp=share_link
Alongside the stock data, two other files are used: the Inflation consumer prices (annual %) and the Wholesale price index (2010 = 100).
The Wholesale price index is a measure of the average price of a basket of goods and services in a given economy, including both agricultural and industrial goods at various stages of production and distribution, and may also include import duties. The Laspeyres formula is typically used to calculate the index.
The Inflation consumer prices (annual %) file measures the annual percentage change in the cost to the average consumer of acquiring a basket of goods and services. The basket may be fixed or changed at specified intervals, such as yearly. The Laspeyres formula is typically used to calculate the index. Both of these files provide valuable context for understanding the performance of the stock market and the broader economic conditions that may be affecting it.

excel file is auto update using setting of google sheet called Recalculation which updates TODAY() funcation in "=GOOGLEFINANCE(company, "all", "1/1/1980", TODAY())"
then i want to use the file from google sheets in notebook dictly using gspread but this lib is giving error 
