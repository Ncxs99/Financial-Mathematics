### Exotics Class - Pricing Exotic Options

The `Exotics` class is designed to provide comprehensive tools for pricing a variety of exotic options. These options, which feature non-standard payoff structures, are often used in complex trading strategies and require sophisticated pricing techniques.

#### Key Features:

1. **Power Option Call:**
   - This method prices a call option where the payoff depends on a power of the underlying asset's price. Power options amplify the potential returns (and risks), making them suitable for investors with a specific view on volatility and asset movements.

2. **Power Option Put:**
   - Similar to the Power Call, this method calculates the price of a put option where the payoff is based on a power of the underlying asset's price. It provides a leveraged way to bet on significant downward movements in the asset's value.

3. **Asset-or-Nothing Call:**
   - The `Asset-or-Nothing Call` method prices an option that pays the full value of the underlying asset if it ends in the money. This all-or-nothing approach is useful in binary-like scenarios where the investor expects a decisive movement in the asset price.

4. **Asset-or-Nothing Put:**
   - This method calculates the price of a put option that pays the asset's full value if it ends in the money. It offers a unique payout structure that can be advantageous in specific market conditions where sharp declines are expected.

5. **Digital Call:**
   - The `Digital Call` method prices an option that pays a fixed amount if the underlying asset's price exceeds a certain level at expiration. This binary option is ideal for scenarios where the investor has a strong directional view on the asset but wants a straightforward, fixed payout.

6. **Digital Put:**
   - Similar to the Digital Call, this method prices a put option that pays a fixed amount if the underlying asset's price falls below a certain level at expiration. Digital Puts are often used in strategies where a clear downside protection with a known payout is desired.

7. **Capped Call Option**

8. **Corridor Call Options**

#### Usage:
The `Exotics` class is implemented in Python and integrates smoothly with broader financial analysis and trading systems. It includes detailed documentation and intuitive methods for each exotic option type, making it easy for users to apply these models in real-world trading or risk management scenarios.

Whether you are an options trader, quantitative analyst, or financial engineer, the `Exotics` class provides a versatile and powerful set of tools for pricing and analyzing exotic options.
This description should effectively highlight the purpose and functionality of the `Exotics` class in your GitHub repository.
