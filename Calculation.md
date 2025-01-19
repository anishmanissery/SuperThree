## SuperThree Indicator Calculation
The SuperThree indicator is an enhanced version of the Supertrend, designed to identify uptrends, downtrends, sideways trends, and counter-trend momentum in the market. Below is a detailed explanation of the calculation and methodology used to determine these trends and counter-trend momentum.

#### Components of SuperThree
1. **ATR-Based Bands**: 
   - **ATR (Average True Range)** is calculated over a specified period (default is 10).
   - The **upper band** is determined by adding a multiple of the ATR to the average price ((high + low) / 2).
   - The **lower band** is calculated by subtracting the ATR multiple from the average price.
   - The multiple used (default is 3) can be adjusted to fit different market conditions.

2. **Trend Direction**:
   - **Trend Bands**: The bands are adjusted based on previous values to ensure they only move in the direction of the trend.
   - **SuperTrend Calculation**: The SuperTrend value switches between the upper and lower bands based on the closing price. If the closing price is above the upper band, the SuperTrend follows the lower band and vice versa.
   - **Trend Direction**: A positive or negative direction is assigned based on the relationship between the current closing price and the SuperTrend value.

3. **Trend Confirmation**:
   - **Trend Band Configuration**: Depending on the selected mode (Strict, Quick, Quicker), the trend confirmation varies:
     - **Strict**: Uses the SuperTrend value for confirmation.
     - **Quick**: Uses adjusted upper/lower bands for faster trend identification.
     - **Quicker**: Uses basic bands for even quicker trend changes.
   - **Directional Check**: The trend direction is determined by comparing the trend bands over the past three bars and confirming with the current and previous closing prices.

4. **Trend Identification**:
   - **Uptrend**: Identified when the trend band is rising over the last three bars and the closing price is higher than both the open and the previous candle's close.
   - **Downtrend**: Identified when the trend band is falling over the last three bars and the closing price is lower than both the open and the previous candle's close.
   - **Sideways Trend**: Recognized when the trend band remains flat over the last three bars and is confirmed by the relationship between the current and previous closing prices.
   - **Trend Continuation**: If the trend from the previous bar persists, it is continued.

5. **Counter-Trend Momentum**:
   - **Counter-Trend Identification**: It calculates the average gap between the closing price and the SuperTrend over the current direction and compares it to a predefined threshold.
   - **Bearish Momentum**: Identified if the closing price, direction, and band movement indicate a possible downward reversal.
   - **Bullish Momentum**: Identified if the closing price, direction, and band movement indicate a possible upward reversal.

## Plotting in the Chart
- **Uptrend**: Filled with green when identified.
- **Downtrend**: Filled with red when identified.
- **Sideways Trend**: Filled with blue when identified.
- **Counter-Trend Momentum**: Displayed with blue arrows (triangles) above or below the bar, indicating potential bearish or bullish momentum, respectively.
