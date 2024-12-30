### FXOptions Class - Pricing Foreign Exchange Derivatives

The `FXOptions` class is designed to provide robust and flexible tools for pricing a variety of foreign exchange (FX) derivatives. This class is essential for financial professionals looking to accurately price complex options that involve foreign and domestic currency interactions.

#### Current Implementation :

1. **Foreign Equity Call Option Priced in Foreign Currency:**
   - This method prices a call option on foreign equity, where both the underlying asset and the strike price are denominated in foreign currency. It is ideal for scenarios where the investor is operating entirely within a foreign market.

2. **Foreign Equity Call Option Priced in Domestic Currency (COMPO):**
   - The `COMPO` method calculates the price of a call option on foreign equity with the strike price denominated in domestic currency. This option type is particularly useful for investors seeking exposure to foreign equities while mitigating currency risk.

3. **Fixed Foreign Equity Rate Call Option (QUANTO):**
   - The `QUANTO` method provides pricing for call options that offer protection against currency fluctuations by fixing the exchange rate. This type of option allows the holder to participate in the movement of the foreign equity market without worrying about adverse currency movements.

4. **Equity-Linked Foreign Exchange Call Option (FX Option Denoted in Domestic Currency):**
   - This method prices an FX option that combines features of equity options and foreign exchange derivatives. The option is denominated in domestic currency, providing a linkage between the performance of a foreign equity and the FX market. This type of option is especially valuable for investors looking to hedge or speculate on both equity and currency movements.

#### Usage:
The `FXOptions` class is implemented in Python and is designed to integrate seamlessly into larger financial modeling frameworks. It is equipped with clear and well-documented methods, allowing users to easily price these FX derivatives and analyze their sensitivities under different market conditions.

Whether you are a quantitative analyst, trader, or financial engineer, the `FXOptions` class offers a comprehensive set of tools to meet your FX derivatives pricing needs.

---

This description should clearly communicate the purpose and functionality of the `FXOptions` class in your GitHub repository.
