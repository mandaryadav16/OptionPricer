#Option Pricer

##Overview
This project features a user-friendly web application designed to calculate European option prices using three widely recognized quantitative finance methods:

Black-Scholes Model

Monte Carlo Simulation

Binomial Model

The application is developed in Python 3.9 and leverages the Streamlit library for an interactive and intuitive web interface, making it accessible even to those new to option pricing.

##Option Pricing Methods Explained
###1. Black-Scholes Model
The Black-Scholes model is a foundational mathematical framework in financial engineering that provides a closed-form analytical solution for pricing European-style call and put options. It calculates the theoretical option price based on key input parameters including:

Current price of the underlying asset

Option strike price

Time remaining until option expiration

Risk-free interest rate

Volatility (standard deviation of the asset’s returns)

This model assumes continuous trading, no arbitrage, and lognormally distributed asset prices.

###2. Monte Carlo Simulation
Monte Carlo simulation is a powerful numerical technique that estimates the value of an option by simulating thousands (or millions) of potential future paths for the underlying asset price, based on stochastic processes. It works by:

Generating random samples of possible price paths following a geometric Brownian motion or other stochastic processes

Calculating the payoff of the option at maturity for each simulated path

Averaging the discounted payoffs to estimate the option’s fair value

This method is particularly useful for pricing complex derivatives where closed-form solutions are not available.

###3. Binomial Model
The Binomial model provides a flexible, discrete-time approach to option pricing by representing the possible price changes of the underlying asset as a recombining binomial tree. The process involves:

Dividing the time to expiration into discrete intervals

Modeling the asset price at each node as either an upward or downward move by a specific factor

Computing the option value recursively from expiration back to the present, using risk-neutral probabilities

This model is intuitive and can be extended to American options and other derivatives.

##Application Features
###Real-Time Data Integration
Automatically fetches the latest stock prices and historical data from the Yahoo Finance API using the pandas-datareader library to ensure option prices are calculated with up-to-date market information.

###Efficient Data Handling
Implements caching via the requests-cache library to reduce redundant API calls and improve performance during repeated queries.

###Customizable Inputs
Users can interactively enter key parameters for option pricing, including:

Strike Price

Risk-Free Interest Rate (annualized, in %)

Volatility (annualized standard deviation, in %)

Option Expiration Date

###Multiple Pricing Methods
Supports calculation of European option prices via the three methods above, allowing users to compare outputs and understand differences in modeling approaches.

###Intuitive Visualization
Displays pricing results clearly through Streamlit’s clean interface, supporting easy experimentation with various scenarios and parameters to deepen understanding of option pricing dynamics.

