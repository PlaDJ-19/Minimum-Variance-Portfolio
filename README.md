This project is a Python class that allows you to calculate the minimum variance portfolio with positive weights for a given list of crypto currencies, using the Yahoo Finance API. The class allows you to specify a start and end date for the historical prices of the crypto currencies, and returns a mapping from column names to weights for the optimal portfolio (+ expected daily return and standard deviation for each currency). The class also includes an additional feature that allows you to pass a target return value, and returns a portfolio with target return values with minimum variance if it is feasible.

The class Crypto has the following methods:

- __init__(self, tickers, start_date, end_date): Initialize the class with the tickers, start date and end date for the historical prices of the crypto currencies.
- initialize_close_prices(self): Get the close prices for each ticker, drop rows that contain missing values and convert the index to datetime objects with the desired format.
- get_close_prices(self): Returns the close prices dataframe
- minimum_variance_portfolio_with_positive_weights(self, target_return): Returns the optimal portfolio with minimum variance with positive weights. It includes an additional feature that allows you to pass a target return value, and returns a portfolio with target return values with minimum variance if it is feasible.

The module yfinance is used to get the historical prices of the crypto currencies and cvxopt is used to solve the optimization problem.

You will need to install yfinance and cvxopt before using this class. This can be done by running the following command:
- pip install yfinance cvxopt

