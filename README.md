# Derivative Pricing Models

This repository contains a Jupyter Notebook (`Derivative pricing.ipynb`) that implements fundamental mathematical models for pricing financial derivatives, specifically European Call and Put options. 

## Features

*   **N-Period Binomial Option Pricing Model:** 
    *   Calculates premiums for European Call and Put options using discrete-time binomial lattices.
    *   Implements up/down factors and risk-neutral probabilities.
*   **Black-Scholes (BS) Model:** 
    *   Prices European Call and Put options using the continuous-time Black-Scholes formula.
    *   Includes functions to calculate total contract cash costs.
*   **Asset Price Path Simulation:** 
    *   Utilizes stochastic simulations and lognormal distributions to model future asset prices ($S_T$) and visualize expected distributions.

## Mathematical Models Implemented

### Black-Scholes Formula
The continuous-time pricing for a European Call option is calculated as:
$$C = S_0 \Phi(d_1) - K e^{-rT} \Phi(d_2)$$

Where:
$$d_1 = \frac{\ln(S_0 / K) + (r + \frac{\sigma^2}{2})T}{\sigma \sqrt{T}}$$
$$d_2 = d_1 - \sigma \sqrt{T}$$

### N-Period Binomial Model
The discrete-time pricing for an N-period European Call option is calculated as:
$$V_0 = \frac{1}{(1+r)^N} \sum_{k=0}^{N} \binom{N}{k} \max(S_0 u^k d^{N-k} - K, 0) \tilde{p}^k (1-\tilde{p})^{N-k}$$

## Libraries Used

*   `numpy`: Numerical computing, random sampling, and array operations.
*   `scipy.stats`: Statistical functions (e.g., standard normal CDF for Black-Scholes).
*   `matplotlib.pyplot`: Visualizing sample means and lognormal price distributions.
*   `math`: Combinatorics and exact mathematical operations for the binomial model.

## Usage

1. Clone this repository to your local machine:
   ```bash
   git clone <your-repository-url>
