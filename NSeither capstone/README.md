## Data Feature Engineering and Risk Assessment 
----
Entrepreneurs have the daunting task of simply getting a business up and running. This reqires a fair amount of passion and hutzzpah and sometimes emotions get high and cloud the judgement of when to get into a market. The first vehicle was not made by Henry Ford, and the first steam ship was not made by Vanderbuilt, yet we know their names because they waited for the right timing to release their product. This project provides a signal to entrepreneurs about when to enter into a certain industry by looking a a data driven lagging and leading signals. 

## Data

Two data sources needed:

1. Custom dataframe provided in the repo
2. New data from DB Nomics API


## Notebook table of contents. 

1. EDA: reading in the data and cleaning the data. 

2. Feature Engineering: Looking at the data with feature engineering to provide economic analysis and risk assesment looking at the lagging features.

3. VAR model:  Using VAR model to see the possibility of using our engineered features in a predictive model.

4. Applying a Stochastic Oscillator model to derrive a risk measurement of economic health. 


## Methods and Models

Use VAR timeseries modeling to create a multivariate timeline and pass it into a stochastic oscilator to determine when to enter or exit the private business industry in colorado springs. 

The ARIMA model will provide a measure of local economy health. The Stochasitic oscilator provides the benchmarks or indicators of a healthy or unhealthy economy. 

Why Stochasitc Oscillators?

Stochastic oscillators help stock traders know when to buy or sell a particular stock based on historical market signals. They have been incredibly accurate as a tool for traders. 

Why are we using them? Stochastic Oscillators do not predict what tomorrow's stock price will be, only the probabability of the direction a stock market may take based on historical trading volume. Historically this method is more accurate than random chance. This follows the same basic fundementals as the economy as far as predictability. No one has one magic algorithm to predict what the economy will do tomorrow, but we can look at signals like unemployment, monetary metrics like tax revenue, and consumer price index. 

Why an ARIMA model? 

We are assuming that not one single variable like gdp is enough to accurately measure an economy. Instead we use unemployment, sales tax revenue, and the consumer price index. unemployment for obvious reasons, tax revenue because it is an accurate and meaurable metric for consumer spending, and consumer price index because as tax revenue and cpi are measured together, if revenue and cpi diverge, then the local economy cannot support inflation and is indicative of a depressed economy. All three combined will determine a better overall picture of an economy. 

Instead of stock market prices as an indicator, we use a ARIMA timeseries model to mimick a stock market time series data. The ARIMA model is a twist on stock prices since we are combinning consumer price index, revenue and use tax revenue, and unemployment to create a multi-variate timeseries model. This will have an added benefit of cross validating our data with projections.  



## Findings . 

We were able to find data and insights for lagging and leading business signals. Notebook 2 shows the relationship and risk for an entrepreneur to enter into the colorado springs market if their were an economic down turn. Entrepreneurs should be prepared to accrue enough capital to withstand two to three years of prolonged economic recession. One key feature to keep in mind is the unemployment rate. Of all the features, unemployment was the greatest factor in determining economic health. 

When we looked at the same engineered data and passed it through a VAR model, the summary statistics showed that the AIC loss was too large to be considered reliable. 

The stochastic oscillator model provided the most promising results. WIth the proper data engineering, we were able to distill economic data and receive a reliable signal to make inferences about the direction of the economy. This will help entrepreneurs know when to enter a market when costs are low and provide enough time to build cash reserves to withstand the next impending downturn. 

In my research I have not seen stochastic oscillators used in this application before.


## Future applications

1. Incorporate into a web application to assist investors and for entrepreneurs in determining risk.
2. Further granularization with the adoption of the top 50 tracked industries. 
3. Standarization into the underwriting process for bank loan operations and procedures.

## Source:
**Data** - U.S. Bureau of Labor Statistics. https://www.bls.gov/regions/mountain-plains/co_coloradosprings_msa.htm

**Data** - https://coloradosprings.gov/sales-tax/page/sales-tax-information

**Data** - U.S. Bureau of economic analysis. https://apps.bea.gov/itable/iTable.cfm?ReqID=70&step=1#reqid=70&step=1&isuri=1

**Data** - API Source. https://db.nomics.world/BEA/


<details>
<summary>Citations</summary>
<br>

    
-CPI and the effects from recessions
    
https://pocketsense.com/recessions-effects-cpi-8135118.html   
    
-Primer on Stochastic Oscillators  https://www.investopedia.com/articles/technical/073001.asp#:~:text=key%20takeaways,a%20high%20degree%20of%20accuracy.&text=it%20can%20be%20beneficial%20to,strength%20index%20(RSI)%20together.</details>

