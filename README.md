# DirectionalTrend MT4

This is a custom indicator for MetaTrader 4 (MT4) developed by the Forex Robot Easy Team. The indicator calculates the trend direction based on the comparison of current price levels with the moving averages of the high and low prices.

## Indicator Settings

- **TimeFrame:** The time frame for trend calculation. The default value is PERIOD_D1, which corresponds to the daily chart.

## Indicator Initialization

The `OnInit()` function is responsible for initializing the indicator. It sets up the indicator buffer and assigns a short name to the indicator.

## Indicator Calculation

The `OnCalculate()` function is called for each new tick to calculate the trend. It receives the necessary data (open, high, low, close prices, etc.) for the current and previous bars.

The function first determines the number of bars to calculate by subtracting the previously calculated bars from the total number of bars. If there are previously calculated bars, one additional bar is included in the calculation.

The trend is then calculated for each bar. The function compares the current high and low prices with the moving averages of the high and low prices calculated using the specified time frame. If the current price is above both moving averages, the trend is considered upward and assigned a value of 1. If the current price is below both moving averages, the trend is considered downward and assigned a value of -1. Otherwise, if the current price is between the moving averages, no trend is detected and a value of 0 is assigned.

The calculated trend values are stored in the `TrendBuffer` indicator buffer.

## Product Description

This code snippet showcases the functionality of the DirectionalTrend MT4 indicator developed by the Forex Robot Easy Team. The indicator helps traders identify the prevailing trend in the market based on the comparison of current price levels with the moving averages of the high and low prices.

With its ability to detect upward and downward trends, traders can use this indicator to make informed trading decisions. The DirectionalTrend MT4 indicator can be applied to any chart and time frame, allowing traders to analyze trends across different markets.

Please note that ForexRobotEasy is not the official developer of this product. We are showcasing this sample code to demonstrate the indicator's functionality. To find the official developer of this product and access detailed reviews and trading results, please visit the following link: [DirectionalTrend MT4 Review - Innovative Forex Trend Indicator](https://forexroboteasy.com/forex-robot-review/directionaltrend-mt4-review-innovative-forex-trend-indicator/).

To use the indicator in your own trading, you can search for it on the MQL5 website or consult the official developer for further information.
