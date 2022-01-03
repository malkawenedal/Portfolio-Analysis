# A Whale Off the Port(folio)
by Nedal Mahanweh 

## Description 

-------------------------
This project will achieve three main goals 
*  Analyzes and visualizes the major metrics of the portfolios across multiple areas: volatility, returns, risk, and Sharpe ratios.
* Determine which portfolio outperformed the others using the historical daily returns of several portfolios: some from the firm's algorithmic portfolios, some that represent the portfolios of famous "whale" investors like Warren Buffett, and some from the big hedge and mutual funds. 
* Use this analysis to create a custom portfolio of stocks and compare its performance to that of the other portfolios, as well as the larger market (S&P TSX 60 Index).
## Prepare the Data
we read the data, detected , removed null values and  Joined  Whale Returns, Algorithmic Returns, and the S&P TSX 60 Returns into a single DataFrame with columns for each portfolio's returns. .

![returns-dataframe.png](Images/returns-dataframe.png)


## Conduct Quantitative Analysis
we Analyzed the data to see if any of the portfolios outperform the stock market (i.e., the S&P TSX 60).
#### Performance Analysis
determine if doeas any portfolio outperform the S&P TSX 60 by calculation and ploting the daily return and the cumulative returns for all portfolios


------------------------------------------------
![cumulative_return](Images/cumulative_return.png)

## Risk Analysis
The purpose of doing this part is to determine the risk of each portfolio by 
* Create a box plot for each portfolio using `plot.box()`
* Calculate the standard deviation for all portfolios using `std()`
* Determine which portfolios are riskier than the S&P TSX 60 using this formula 
`daily_returns_1_std > daily_returns_1["S&P TSX"].std()`
 
 * Calculate the Annualized Standard Deviation using this formula :
 `daily_returns_1_std_annual = daily_returns_1.std() * np.sqrt(252)`

 ## Rolling Statistics

 we aimed to determine the Risk changes over time and Analyze the rolling statistics for Risk and Beta by :
 * Calculating  and plot the rolling standard deviation for for all portfolios using a 21-day window.
* Calculating the correlation between each stock to determine which portfolios may mimick the S&P TSX 60.
* Choosing  one portfolio (Algo 1), then calculate and plot the 60-day rolling beta for it and the S&P TSX 60.

![rolling_60_day_beta](Images/rolling_60_day_beta.png)

## Sharp ratio
this part analyse return-to-risk ratio.

![sharp_ratio](Images/sharp_ratio.png)


##  Create a Custom Portfolio
The purpose of doing  this section, is building  my  own portfolio of stocks, calculating  the returns, and comparing  the results to the Whale Portfolios and the S&P TSX 60.

i chose 3 stocks( NASDAQ,S&P TSX 60,FB GOGL) with at last 1 year's worth of prices and created a DataFrame of the closing prices and dates for each stock.

![custome_portfolios](Images/custome_portfolios.png)

* Calculated the weighted returns for the portfolio assuming an equal number of shares for each stock.


* Joined my portfolio returns to the DataFrame that contains all of the portfolio returns.


![combined_Df](Images/combined_df.png)

* Re-ran the performance and risk analysis with your portfolio to see how it compares to the others.
* Includeded  correlation analysis to determine which stocks (if any) are correlated.

![correlation](Images/correlation.png)

![rolling_60_days](Images/rolling_60_day.png)







