# DynamicBT: A wrapper for Backtesting.py

This wrapper is an enhancement of the Python library ``backtesting.py``, which is very popular for backtesting of trading strategies.

***Currently part of [backtesting_ms](https://github.com/MathematicusLucian/backtesting_ms). Will extract and deploy to PyPi as a library***

Issues addressed:
- ``backtesting.py`` relies on hardcoding of strategy configuration, such as upper and lower bands, and also the optimisation criteria, etc., meaning much code has to be written to define strategies.
- The default strategies, and many circulated online, are not going to find alpha (an opportunity to exploit market inefficiency); because they are utilised by too many traders. 

Solution:
- The wrapper assembles strategy details according to content of either a config file, or a database. (WIP: This can then be edited via a UI.)
- There is a factory to fetch the strategy class.
- Walkforward testing of all strategies.
- Strategies, with optimisation functionality, are required that compare data sources of world events, including news events and social media sentiment, to market movements to find patterns that reflect correlation. [market_sentiment_ms](https://github.com/MathematicusLucian/market_sentiment_ms)
- Optimsiation can be ehanced with machine learning [stonk-value-forecasting-model](https://github.com/MathematicusLucian/stonk-value-forecasting-model)