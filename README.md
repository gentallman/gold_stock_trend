


# Gold Stock Trend Analysis and Predicition
<p align="center">
<img src="https://github.com/gentallman/gold_stock_trend/blob/main/asset/gold_stock_trend.png" width="60%" height="60%">
</p>

## Problem statement

The volatility and complexity of the gold market present challenges for investors, analysts, and researchers seeking to understand its behavior and make informed decisions. Leveraging a comprehensive dataset of daily gold prices spanning from January 19, 2014, to January 22, 2024, sourced from Nasdaq, this project aims to address key questions and objectives related to historical trends, predictive modeling, trading strategy development, market sentiment analysis, and statistical insights.

## Project Objectives 

- Time Series Analysis
- Advanced Modeling
- Trading Strategy Development
- Market Sentiment Analysis
- Statistical Analysis

## About data

[Data Source - Nasdaq](https://www.nasdaq.com/market-activity/commodities/gc:cmx)

- Date: Unique identifier for each trading day.
- Close: Closing price of gold on the respective date.
- Volume: Gold trading volume on the corresponding date.
- Open: Opening price of gold on the respective date.
- High: The highest recorded price of gold during the trading day.
- Low: The lowest price recorded for gold in the trading day.


## Time Series Analysis

### **Long-Term Trend** 

![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/47579b85-4daa-4ba4-8d68-0a1267969609)
> - The graph illustrates a consistent upward trend in gold prices over the years, notably since approximately 2019, with prices rising from around $1200 to nearly $2000.
> - Although fluctuations indicate volatility, the overarching trend remains positive.
> - Understanding the drivers behind these fluctuations, including economic conditions, investor sentiment, and seasonal factors, offers valuable insights for decision-making.

### **Seasonality and Residuals**   
![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/e118cf7e-0073-4af7-b17f-e2b856b649e0)
> - The graph illustrates a consistent upward trend in gold prices over the years, notably since approximately 2019, with prices rising from around $1200 to nearly $2000.
> - Although fluctuations indicate volatility, the overarching trend remains positive.
> - Understanding the drivers behind these fluctuations, including economic conditions, investor sentiment, and seasonal factors, offers valuable insights for decision-making.

### **Cyclical Patterns**

![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/3f93a324-9563-4c2b-ad6b-0d8142a479a5)

> - The holiday shopping season, spanning from November to December, contributes to a rise in gold demand as consumers seek gifts.
> - The wedding season in India, reaching its peak from October to January, drives heightened demand as gold holds cultural significance in Indian weddings.
> - Additionally, the Hindu festival of Diwali, occurring in October or November, stimulates increased gold purchasing as it is considered auspicious.
> - Conversely, during the summer months between May and August, gold prices may experience a dip or slower activity, potentially due to reduced market participation or seasonal preferences

## Advanced Modeling

- Traditional statistical models like ARIMA and SARIMA, found in the `statsmodels.tsa` package, are adept at capturing time series patterns and seasonality.
- Holt-Winters, available in `statsmodels.tsa.holtwinters`, is employed for exponential smoothing, enabling the forecasting of trends and seasonal effects.
- Prophet, part of the fbprophet (now prophet) library developed by Facebook, stands out as a robust time series analysis tool, offering accurate predictions by considering dynamic trends and outliers.
- In addition, deep learning models, specifically LSTM-based, are implemented using `Sequential`, `LSTM`, and `Dense` from `tensorflow.keras.models` and `tensorflow.keras.layers`.
- For data preparation and evaluation, `train_test_split` from `sklearn.model_selection` is utilized to split the data into training and test sets.
- Furthermore, performance metrics such as mean absolute error (`mean_absolute_error`) and mean squared error (`mean_squared_error`) from `sklearn.metrics` are employed to assess the models' effectiveness.

I intend to utilize all available data up to the conclusion of 2023 as our training dataset. Subsequently, we will employ the data from the year 2024 as our test set, aiming to forecast across the entirety of the dataset

#### Different modeling techniques, including ARIMA, SARIMA, Holt-Winters, LSTM, and Prophet, were employed to forecast gold prices. While each model has its strengths, none of them perfectly capture the market dynamics, suggesting the need for continuous refinement and evaluation of forecasting methodologies. Based on actual and predicition graph analysis with performance score `prophet` is best model.

![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/aeeb094d-e9e2-488a-9d14-bac1224a38d0)
> - The real gold prices (black line) go up slowly over time, with some ups and downs now and then. The forecasted prices (orange line) mostly follow the trend of real prices but have some changes because of the ups and downs. Overall, the prophet model's guesses go along with the main trend of gold prices, catching both the rises and falls.

## Trading Strategy Development

### Moving Average Crossover Strategy 
- This strategy likely involves using two moving averages (short-term and long-term) to identify optimal entry and exit points.
- When the short-term moving average crosses above the long-term moving average, it generates a buy signal. Conversely, a cross below indicates a sell signal.
- The consistent portfolio value indicates that this strategy aims for steady growth over time.

### Reverse Trading Strategy
- This strategy might involve counter-trend trading, where positions are taken opposite to prevailing market trends.
- Signals are generated based on volume analysis rather than price analysis. If the current volume exceeds the average volume, a sell signal (-1.0) is generated; otherwise, it's a hold (0.0).
- It could be based on technical indicators, sentiment analysis, or other factors.
- The sharp fluctuations in portfolio value indicate higher risk but also potential for substantial gains.

### Risk-Return Tradeoff:
- The Moving Average Crossover Strategy prioritizes stability, while the Reverse Trading Strategy seeks higher returns.
- Traders must weigh risk against potential rewards when choosing between these approaches.

![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/fcb8b82d-af53-4502-ad8c-7ae92108c0f4)
> - The blue line, symbolizing the Moving Average Crossover Strategy, maintains a consistently stable portfolio value throughout the backtesting period, showing minor fluctuations but overall steadiness.
> - In contrast, the orange line representing the Reverse Trading Strategy displays significant volatility, with notable peaks and troughs, indicating a more unpredictable performance.
> - Both strategies intersect at multiple points on the graph, reflecting moments of alignment or divergence. Analyzing these intersections can offer insights into market conditions and potential adjustments to the strategies.

## Market Sentiment Analysis

### Gold Stock during the Pandemic Years

![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/cd958845-71fc-43b9-8b90-7ba9b9e658c0)
Analysis of gold stock during the pandemic years reveals a notable upward trend in prices until around mid-March. Following this period, prices experienced a decline attributed to pandemic-induced lockdowns. Subsequently, the graph displays a significant upward trend in gold prices in May, peaking in August 2020. The impact of varying lockdown measures implemented at different times in different countries contributed to fluctuations in prices until the end of 2021.

### Impact of Russia – Ukraine Conflict
![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/c880a4fe-bca2-418f-a5f0-e4f6270e6a74)
> - The analysis of gold price fluctuations underscores the impact of the Russia-Ukraine conflict, which commenced in late February 2022.
> - Initially, gold prices sharply declined, reaching a low around $1900, coinciding with the conflict's onset in July 2022. By the end of September 2022, the prices hit their lowest point at $1600.
> - However, as the conflict progressed, a gradual recovery ensued, leading to a notable peak around December 2022.
> - The overall trend depicted an upward trajectory with intermittent fluctuations, culminating in a peak near January 2024, with gold prices nearly reaching $2050. This period, termed the "War Slowdown," reflects rising gold prices amid a reduction in conflict intensity or uncertainty.

### Exploring the Relationship Between Trading Volume and Gold Prices

![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/ffef2c31-9e03-486b-8e31-27df3b4e5ab5)

The scatter plot shows how volume (the amount of trading activity) affects the closing price of gold. When there's low trading activity, the closing price tends to stay within a narrow range. But when trading activity picks up, the closing price can vary more widely. We see more data points when trading activity is low, but fewer when it's high. This suggests there might be a connection between trading volume and the closing price, but we need more analysis to be sure.

## Statistical Analysis

![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/baee0dd7-00ab-4f48-84b0-b7764ff417c9)

### Shapiro-Wilk Test for Normality:
- **Test statistic**: The Shapiro-Wilk test is used to assess whether a dataset follows a normal distribution. The test statistic value (**0.8725** in this case) is compared to critical values to determine the level of departure from normality. A value closer to 1 suggests the data is more likely to be normally distributed.
- **p-value**: This is the probability of observing the data if the null hypothesis is true (i.e., if the data were drawn from a normal distribution). A small p-value (e.g., **2.987e-41**    ) indicates strong evidence against the null hypothesis, suggesting that the data significantly deviates from normality.

### Pearson Correlation Coefficient:
- This coefficient measures the strength and direction of a linear relationship between two variables.
- For example, the **correlation coefficient between 'Close' and 'Volume' is approximately 0.0228**. A value close to 0 indicates **a weak linear relationship**, suggesting that changes in 'Volume' are not strongly associated with changes in 'Close’.
- The **correlation coefficient between 'Close' and 'Open' is approximately 0.999**, indicating a **very strong positive linear relationship**. This suggests that 'Close' and 'Open' prices move almost perfectly in tandem, with 'Close' prices being almost identical to 'Open' prices, but with a slight difference due to factors such as market activity between opening and closing.

## Key Takeways

- Gold prices have shown a consistent upward trend since 2019, despite fluctuations, indicating long-term investment potential. COVID-19 made prices go up and down quickly, but overall, it showed that gold is a safe thing to invest in when things get tough, so its prices went up.
- Seasonal Fluctuations: Gold prices exhibit regular patterns influenced by various factors such as cultural events, economic conditions, and demand fluctuations. Understanding these seasonal variations is essential for interpreting short-term price movements.
- Different modeling techniques, including ARIMA, SARIMA, Holt-Winters, LSTM, and Prophet, were employed to forecast gold prices. While each model has its strengths, none of them perfectly capture the market dynamics, suggesting the need for continuous refinement and evaluation of forecasting methodologies.
- The Moving Average Crossover strategy prioritizes stability, while the Reverse Trading strategy aims for higher returns but entails greater volatility. Traders must consider the risk-return tradeoff when selecting a strategy.
- External events, such as the COVID-19 pandemic and geopolitical conflicts like the Russia-Ukraine conflict, significantly impact gold prices. These events introduce volatility and uncertainty into the market, influencing investor behavior and driving fluctuations in prices.
- Statistical tests, including the Shapiro-Wilk test for normality and Pearson correlation coefficient, provide additional insights into the distribution of data and the strength of relationships between variables, aiding in robust analysis and interpretation.

## Recommendations
Looking ahead, predicting gold prices will depend on understanding how the market changes and what factors affect it, like the economy, global tensions, and new technology. Improving predictive models with advanced techniques and data analysis can help make more accurate forecasts. It's important to stay alert to emerging risks and opportunities in the market, adapting strategies accordingly. Overall, flexibility and using the latest tools will be key to making informed decisions about gold investments in the future.

## Contact

Author: Smit Rana


LinkedIn: [linkedin.com/in/smit98rana/](https://www.linkedin.com/in/smit98rana/)https://www.linkedin.com/in/smit98rana/

