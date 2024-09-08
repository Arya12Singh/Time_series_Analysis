# Time Series Analysis of Google Stock Prices

## Overview

This project performs time series analysis on Google's stock price data, including various exploratory data analysis (EDA) techniques and visualizations. The analysis uses Python and focuses on common time series operations such as resampling, slicing, rolling statistics, and trend identification.

## Dataset

The dataset used for this analysis is **Google stock prices**, containing the following columns:
- `Date`: The date of the stock price record.
- `Open`: The stock's opening price on the given day.
- `High`: The highest price during the trading day.
- `Low`: The lowest price during the trading day.
- `Close`: The price at the end of the trading day.
- `Adj Close`: The adjusted closing price, accounting for splits and dividends.
- `Volume`: The number of shares traded on that day.

## Code Breakdown

### 1. Data Loading and Preparation
- The dataset is loaded using `pandas` and the `Date` column is converted to a datetime format.
- The `Date` column is set as the index for easier time series manipulation.

### 2. Time Series Operations
- **Fetching specific dates**: Retrieve stock prices for a specific date (`'2021-12-30'`).
- **Partial indexing**: Select data for a specific month or year using partial string indexing (e.g., `'2022-5'`).
- **New time-based columns**: Columns for month names, weekday names, and quarters are created to analyze trends.
  
### 3. Slicing and Filtering
- Slicing data for a range of dates (e.g., `'2022-01-07'` to `'2022-05-19'`).
- Fetching data for the same date across multiple years.

### 4. Visualization
- **Single column plotting**: The 'Close' prices are plotted over time.
- **Multiple columns**: A subset of columns ('Open', 'High', 'Low', 'Close') is visualized as subplots.
- **Monthly and Quarterly trends**: Grouped by month or quarter, and the mean 'Close' prices are plotted as bar charts.

### 5. Resampling
- **Upsampling**: Resampling to a higher frequency (12 hours) and using spline interpolation.
- **Downsampling**: Reducing the frequency to yearly data and calculating the mean for each year.

### 6. Rolling Mean and Shifting
- **Rolling mean**: A 3-day rolling mean is applied to the 'Close' prices to smooth fluctuations.
- **Shifting**: Shifts the 'Open' prices by 2 periods to create lag features.

## Visualizations

The notebook contains various visualizations, including:
- Time series line plots of stock prices.
- Bar plots of monthly and quarterly stock trends.
- Resampled data with interpolation and aggregation.




