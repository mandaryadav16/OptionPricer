# Option Pricing Models

## Introduction
This repository contains a simple web app for calculating European option prices using three different methods:

1. Black-Scholes model
2. Monte Carlo simulation
3. Binomial model

The app is implemented in Python 3.9 and uses the Streamlit library for visualization.

## Option Pricing Methods

### 1. Black-Scholes Model
A mathematical model used to calculate the theoretical price of European-style options, based on factors like current stock price, strike price, time to expiration, risk-free rate, and volatility.

### 2. Monte Carlo Simulation
A probabilistic method that uses random sampling to estimate option prices by simulating multiple possible price paths of the underlying asset.

### 3. Binomial Model
A discrete-time model that represents the evolution of the underlying asset's price as a binomial tree, allowing for the calculation of option prices at different time steps.

## Features

- Fetches latest stock price data from Yahoo Finance API using pandas-datareader
- Caches data using requests-cache to avoid duplicate API calls
- Allows users to input various parameters:
  - Strike price
  - Risk-free rate (%)
  - Sigma (Volatility) (%)
  - Exercise date
- Calculates option prices based on user inputs
- Provides a user-friendly interface for testing different scenarios
