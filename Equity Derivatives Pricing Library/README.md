### Black-Scholes Derivatives Pricing Library

This Python library is dedicated to the pricing of various financial derivatives using the Black-Scholes model. We have implemented comprehensive tools for pricing standard derivatives, calculating the Greeks, and extending the framework to handle exotic options and foreign exchange (FX) derivatives.

#### Key Features:

1. **Pricing of Standard Derivatives:**
   - We have implemented the Black-Scholes model to price classic financial derivatives, including European call and put options. This foundational pricing model serves as the basis for more complex derivative pricing.

2. **Computation of Greeks:**
   - The library includes detailed calculations for the Greeks, which are essential for risk management and sensitivity analysis. We provide a linear definition and mathematical explanation of each Greek:
     - **Delta:** Measures the sensitivity of the option price to changes in the underlying asset's price.
     - **Gamma:** Represents the rate of change of Delta with respect to changes in the underlying asset's price.
     - **Dual Delta:** Sensitivity of the option price to changes in the strike price for call and put options.
     - **Dual Gamma:** Second-order sensitivity of the option price with respect to the strike price.
     - **Vega:** Measures the sensitivity of the option price to changes in the volatility of the underlying asset.
     - **Vuma:** Sensitivity of Vega with respect to the underlying asset's price.
     - **Theta:** Represents the sensitivity of the option price to the passage of time (time decay).
     - **Rho:** Sensitivity of the option price to changes in the risk-free interest rate.
     - **Psi:** Sensitivity of the option price to changes in the dividend yield.

3. **Forward and Futures Pricing:**
   - We have implemented the Black-Scholes formulas for pricing options on forwards and futures. This includes the calculation of Delta for call options under forward and futures contracts.

4. **Pricing of Exotic Options:**
   - The library extends the Black-Scholes framework to price a variety of exotic options, including:
     - **Power Options:** Options where the payoff depends on a power of the underlying asset's price.
     - **Asset-or-Nothing Options:** Options that pay the asset if it ends in the money.
     - **Cash-or-Nothing Options:** Options that pay a fixed amount of cash if the option ends in the money.
     - **Digital Options (Call and Put):** Options that pay a fixed amount if the underlying asset is above (or below) a certain level at expiration.
   - We also provide an introduction to the pricing of barrier options, including:
     - **Regular Down-and-In Call (DIC):** A call option that comes into existence only if the underlying asset price hits a predetermined barrier level from above.
     - **Regular Down-and-Out Call (DOC):** A call option that ceases to exist if the underlying asset price hits a predetermined barrier level from above.
     - **Binary Down-and-In Call (DIC):** A binary call option that becomes active when the underlying asset price hits a barrier level.

5. **FX Options Pricing:**
   - The library includes tools for pricing FX options, incorporating the complexities of foreign and domestic currencies:
     - **Foreign Equity Call Strike in Foreign Currency:** A call option on foreign equity with the strike price also in foreign currency.
     - **Foreign Equity Call Strike in Domestic Currency (COMPO):** A call option on foreign equity where the strike price is in domestic currency.
     - **Fixed Foreign Equity Rate Call (QUANTO):** A call option with a fixed exchange rate, protecting against currency fluctuations.
     - **Equity-Linked Foreign Exchange Call (FX Option Denoted in Domestic Currency):** An option combining features of equity and FX markets, denominated in domestic currency.

This library is an essential tool for financial engineers, quantitative analysts, and traders looking to apply the Black-Scholes model across a wide array of derivatives, from standard options to more complex exotic and FX options.
