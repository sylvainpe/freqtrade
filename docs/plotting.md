# Plotting
This page explains how to plot prices, indicator, profits.

## Table of Contents
- [Plot price and indicators](#plot-price-and-indicators)
- [Plot profit](#plot-profit)

## Plot price and indicators
Usage for the price plotter:
script/plot_dataframe.py [-h] [-p pair]

Example
```
python script/plot_dataframe.py -p BTC_ETH,BTC_LTC
```

The -p pair argument, can be used to specify what
pair you would like to plot.


## Plot profit

The profit plotter show a picture with three plots:
1) Average closing price for all pairs
2) The summarized profit made by backtesting.
   Note that this is not the real-world profit, but
   more of an estimate.
3) Each pair individually profit

The first graph is good to get a grip of how the overall market
progresses.

The second graph will show how you algorithm works or doesnt.
Perhaps you want an algorithm that steadily makes small profits,
or one that acts less seldom, but makes big swings.

The third graph can be useful to spot outliers, events in pairs
that makes profit spikes.

Usage for the profit plotter:
script/plot_profit.py [-h] [-p pair] [--datadir directory] [--ticker_interval num]

The -p pair argument, can be used to plot a single pair

Example
```
python python scripts/plot_profit.py --datadir ../freqtrade/freqtrade/tests/testdata-20171221/ -p BTC_LTC
```
