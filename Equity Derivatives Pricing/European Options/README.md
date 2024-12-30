### EuropeanOptions Class - Pricing European Options

The `EuropeanOptions` class provides a complete suite of tools for pricing European-style options using the Black-Scholes model and for calculating the associated Greeks. This class is essential for traders and analysts who need to understand and manage the sensitivities of their option portfolios.

#### Current Implementations :

1. **Standard European Call and Put Options:**
   - **Black-Scholes Call Option:** Prices a standard European call option using the Black-Scholes formula, which assumes the option can only be exercised at expiration.
   - **Black-Scholes Put Option:** Prices a standard European put option using the Black-Scholes formula.

2. **Greeks Calculation:**
   - **Delta (Call and Put):** Measures the sensitivity of the option's price to changes in the underlying asset's price.
   - **Gamma (Call and Put):** Represents the rate of change of Delta with respect to changes in the underlying asset's price.
   - **Dual Delta (Strike Call and Put):** Sensitivity of the option price to changes in the strike price, also known as the strike Delta.
   - **Dual Gamma (Strike Call and Put):** Second-order sensitivity of the option price with respect to changes in the strike price, also referred to as strike Gamma.
   - **Vega (Call and Put):** Measures the sensitivity of the option price to changes in the volatility of the underlying asset.
   - **Voma (Call and Put):** Sensitivity of Vega with respect to changes in the volatility itself.
   - **Theta (Call and Put):** Measures the sensitivity of the option price to the passage of time, reflecting time decay.
   - **Rho (Call and Put):** Sensitivity of the option price to changes in the risk-free interest rate.
   - **Psi (Call and Put):** Sensitivity of the option price to changes in the dividend yield of the underlying asset.

3. **Forward and Futures Pricing:**
   - **Black’s Model for Forwards (Call and Put):** Implements the Black model to price European call and put options on forward contracts.
   - **Delta for Futures:** Calculates the Delta of a futures contract, providing insight into how the futures price will respond to changes in the underlying asset's price.

#### Usage:
The `EuropeanOptions` class is implemented in Python, with well-documented methods for each option type and Greek. It is designed to be integrated into larger financial models, allowing users to price European options and calculate their Greeks quickly and accurately.

Whether you are a quantitative analyst, trader, or financial engineer, the `EuropeanOptions` class offers the essential tools needed for effective options pricing and risk management in European-style derivatives.
This description effectively outlines the features and functionalities of the `EuropeanOptions` class in your GitHub repository.
