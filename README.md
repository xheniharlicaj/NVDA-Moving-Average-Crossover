# NVDA-Moving-Average-Crossover
This Python script defines a class 'MovingAverageCrossover' that implements a Moving Average (MA) Crossover trading Strategy. 

We use historical price data from Yahoo Finance API, and simulate trading decisions based on exponential moving average (EMA) crossovers.

Parameters of the class include intial capital, stock symbol, start and end dates for data gathering, as well as short and long moving average periods.

On this case, we impement a trading strategy on the NVIDIA Corporation, which is the best-performing stock inb the S&P 500 in 2024. We use an initial capital of $100 and extract historical data from January 1st, 2010 to February 12th, 2024.

As for the short and long periods, we build an optimization function 'optimize_paramenters' to search for the optimal combination of short and long periods that yield the highest profit.

After we execute the script, we get the following output: Optimal parameters: Short Period = 20, Long Period = 54 Best Profit: 179.49%

We then plot an instance of the 'MovingAverageCrossover' class with initial capital of $100 and historical data timeline as above, as well as the most optimal short and long periods based on the output above.

'strategy = MovingAverageCrossover(100, 'NVDA', start_date, end_date, 20, 54)'

This will be used to conduct a simulation of the moving average crossover trading strategy for the NVIDIA stock within the given time frame.

The 'strategy.plot_signals()' function plots the stock price along with the short-term and long-term EMAs to visualize the moving average crossover signals.

The 'strategy.simulate()' function simulates the trading strategy based on the moving average crossover signals. It determines when to buy, sell, or hold positions according to the crossover signals.

The 'strategy.plot_equity()' function plots the equity curve, which represents the changes in capital over time as a result of executing the simulated trades. This curve helps visualize the performance of the trading strategy.

'print(strategy.equity)' prints the list of equity values at different points in time during the simulation.
