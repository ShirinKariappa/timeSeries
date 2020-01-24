**Time Series:** Number of data points listed in a timely order. Here date are in equal intervals of time.  
**for ex:** data for every one hour ,30 mins or a day.

**Holt-Winters model:**
It is one of the model to predict the present or future data points using time series data.  

**The main parameters that should be considered while forecasting time series data are :**  
***Average:*** finding the mean of the data points.  
***trend:*** It is nothing but the slope. check if the dataset has positive or negative trend.  
***Seasonality:*** The time series is said to be seasonal if it has repeating patterns throughout the data.  

Holt-Winters method internally uses ***exponential smoothing*** to encode lots of values from the past and use them to predict “typical” values for the present and future.

**What is Exponential smoothing?**  
It uses exponentially weighted moving average (EWMA) to “smooth” a time series.i.e.,It makes the data stationary by removing random flutuations in the data.  

**Different types of moving avarage:**  

refer-*https://www.investopedia.com/ask/answers/071414/whats-difference-between-moving-average-and-weighted-moving-average.asp*  

**Simple Moving Average:** finding the average of data points. i.e., (sum of data points/number of data points)  
**ex:**  

Date | opening stock price  
------------ | -------------  
July 16	| $90.90  
July 17	| $90.36  
July 18	| $90.28  
July 19	| $90.83  
July 20	| $90.91  

(P1+P2+P3+P4+P5)/5  
P = Period  
($90.90+$90.36+$90.28+$90.83+$90.91)/5 = $90.656  

**Weighted Moving Average:** Weights are assigned to each data point. The most recent data point will have heavier weight than the oldest data point.  
**ex:**  

Date | opening stock price|weights  
------------ | ------------- |-------- 
July 16	| $90.90 | 5/15
July 17	| $90.36 | 4/15
July 18	| $90.28 | 3/15
July 19	| $90.83 | 2/15 
July 20	| $90.91 | 1/15

((90.9*(5/15))+(90.36*(4/15))+(90.28*(3/15))+(90.83*(2/15))+(90.91*(1/15)))=$90.62
So in this case, the contribution of the fifth record in the calculation of average will be more when compared to the first record.  

**Exponential Moving Average:**
EMAs are also weighted toward the most recent prices, but the rate of decrease between the one price and its preceding price is not consistent. The difference in decrease is exponential. Rather than every preceding weight being 1.0 smaller than the weight in front of it, you might have a difference between the first two period weights of 1.0, a difference of 1.2 for the two periods after those, and so on.  

*If your data is stationary and it doesn't have any trend and seasonality then, Simple Exponential Smoothing will work.  
If your data is not stationary and it has trend then Holt’s exponential smoothing will work.It is also called as "Double exponential smoothing".  
If your data has both trend and seasonality then try Holt-Winters methd ,which is aslo called as "triple exponential smoothing".*

**Validating Forecasting Models:**
The usual way to quantify the accuracy of a forecast is to calculate the differences between the predicted values and the actual values.The difference represent how far off the prediction was from the actual value.To find the overall accuracy,you can combine these differences into a single value by taking the average or the sum of squared values. The result is a value that is smaller if the forecast is better, and larger if the forecast is worse.  


