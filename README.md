# Quantitative-Momentum-Investing-Strategy

## (THIS IS NOT FINANCIAL ADVICE. PERSONAL PROJECT ONLY)

In this project, I have created a momentum investing strategy. The first part is only focused on a 6-month increase, and the second part is focused on a more steady growth. 

## Quantitative Momentum

Quantitative Momentum is an investing strategy that chooses the stocks to buy based upon their momentum, which means I am looking for stocks that have a tendency to keep moving in their current direction. This strategy is based upon the thought that stocks that have historically performed well will continue to perform well in the future. 

In this project, I am looking for stocks to buy based on their upward momentum or their consistent raising in prices. I will be looking to build an equal-weighted portfolio of the top 50 stocks with the biggest positive momentum within the S&P500. An equal-weighted portfolio allows us to spread the risk across multiple assets.

## The Process

First, I collected the list of current constituents of the S&P500 from the list on Wikipedia. Then, I used the Schwab API to gather historical data on all the stocks. From there, I calculated the percentage change in based upon the the current price and whatever the previous price was at that specific time difference. 

For the 6-month change,  I sorted the stocks based upon the size of the positive change and kept the top 50 movers. To calculate how many of each stock we buy, I divided the size of the portfolio by the number of stocks to buy (50 stocks). I, then, used that resuluting number and divided that by each stocks current price. I rounded that down to the closest integer to ensure that we don't buy more than we actually could. 

To look for a more steady growth, I collected the prices of each stock at 1-year ago, 6-months ago, 3-months ago, and 1-month ago, and calculated the percentage change from each time difference. After that, I calculated their return percentiles based on all the other stocks in the S&P500. Next, I took the average of the percentiles to create and High Quality Momentum (HQM) Score. A high HQM Score indicates that the stock outperformed other stocks across these different time ranges, and it shows that the growth they are experiencing is consistent. I kept the stocks with the top 50 HQM Score and repeated the process in which we determine how many of each stock to buy.
