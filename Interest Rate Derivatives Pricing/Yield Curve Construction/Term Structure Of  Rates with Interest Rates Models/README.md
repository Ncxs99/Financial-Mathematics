
  
### Implement Interest Rate Models: Derivation of Rates, Forward Rates, and Discount Factors

---

In this section, we derive and implement the various key rates, including **spot rates**, **forward rates**, and **discount factors**, based on well-known interest rate models. These models—**Nelson-Siegel**, **Nelson-Siegel-Svensson**, **Cox-Ingersoll-Ross (CIR)**, and **Vasicek**—are commonly used in financial markets to model the term structure of interest rates. 
Below is a breakdown of how we derive and calculate these key metrics using each model:

### **1. Nelson-Siegel Model**:

The **Nelson-Siegel model** is a popular parametric model used to fit the yield curve. The model expresses the yield at time \( t \) as a function of three parameters:
- $\beta_0 $: Long-term rate (asymptotic value)
- \( \beta_1 \): Slope of the yield curve
- \( \beta_2 \): Curvature
- \( \lambda \): Time to mean reversion (decay factor)

The formula for the yield \( r(t) \) under the Nelson-Siegel model is:

\[
r(t) = \beta_0 + \beta_1 \left( \frac{1 - e^{-t/\lambda}}{t/\lambda} \right) + \beta_2 \left( \frac{1 - e^{-t/\lambda}}{t/\lambda} - e^{-t/\lambda} \right)
\]

- **Discount Factor** \( d(t) \): The discount factor can be derived by reversing the yield curve formula, using the exponential form of the yield.
  
- **Forward Rate** \( f(t1, t2) \): The forward rate between two times \( t1 \) and \( t2 \) can be computed from the discount factors at those points as:

\[
f(t1, t2) = \frac{\log(d(t1)) - \log(d(t2))}{t2 - t1}
\]

### **2. Nelson-Siegel-Svensson Model**:

The **Nelson-Siegel-Svensson (NSS)** model extends the Nelson-Siegel model by adding two additional parameters, making it more flexible. This model includes the following parameters:
- \( \beta_0, \beta_1, \beta_2, \beta_3 \): The first four parameters controlling the shape of the curve.
- \( \tau_1, \tau_2 \): The decay factors, controlling the speed of mean reversion for the curves.

The formula for the yield at time \( t \) is:

\[
r(t) = \beta_0 + \beta_1 \left( \frac{1 - e^{-t/\tau_1}}{t/\tau_1} \right) + \beta_2 \left( \frac{1 - e^{-t/\tau_1}}{t/\tau_1} - e^{-t/\tau_1} \right) + \beta_3 \left( \frac{1 - e^{-t/\tau_2}}{t/\tau_2} - e^{-t/\tau_2} \right)
\]

Similar to the Nelson-Siegel model, we can derive **discount factors** and **forward rates** from this model using the same principles.

### **3. Cox-Ingersoll-Ross (CIR) Model**:

The **Cox-Ingersoll-Ross (CIR)** model is a mean-reverting process where the short-term interest rate follows an Ornstein-Uhlenbeck process. The model is described by the SDE:

\[
dr(t) = \kappa (\theta - r(t)) dt + \sigma \sqrt{r(t)} dW(t)
\]

Where:
- \( r(t) \): The short-term interest rate
- \( \kappa \): The speed of mean reversion
- \( \theta \): The long-run mean level
- \( \sigma \): The volatility of the interest rate

The **discount factor** \( d(t) \) under the CIR model is computed as:

\[
d(t) = \exp \left( - A(t) - B(t) r(0) \right)
\]

Where \( A(t) \) and \( B(t) \) are functions of the parameters \( \kappa \), \( \theta \), \( \sigma \), and the initial rate \( r(0) \). These functions are derived from solving the CIR SDE analytically.

- **Forward Rate** \( f(t1, t2) \) is derived similarly to other models, based on the discount factors at times \( t1 \) and \( t2 \).

### **4. Vasicek Model**:

The **Vasicek model** is another mean-reverting process often used to model the evolution of interest rates. The rate follows the process:

\[
dr(t) = a(b - r(t)) dt + \sigma dW(t)
\]

Where:
- \( r(t) \): The short-term interest rate
- \( a \): The speed of mean reversion
- \( b \): The long-term mean level
- \( \sigma \): The volatility of the interest rate

The **discount factor** \( d(t) \) in the Vasicek model is given by:

\[
d(t) = A \exp(-B r_0)
\]

Where \( A \) and \( B \) are derived from the parameters \( a \), \( b \), \( \sigma \), and the initial rate \( r_0 \). These expressions for \( A \) and \( B \) are crucial to the discount factor's computation.

The **forward rate** \( f(t1, t2) \) can be derived using the same principles from the discount factors at the two points.

---

### **Conclusion**:

In this implementation, we've provided functions to calculate:
- **Yield** \( r(t) \) for each model based on the respective parameters.
- **Discount Factor** \( d(t) \) derived from the yields.
- **Forward Rate** \( f(t1, t2) \) calculated from the discount factors between two times \( t1 \) and \( t2 \).

The goal is to create a flexible term structure that can accommodate various interest rate models (Nelson-Siegel, Svensson, CIR, and Vasicek) for efficient pricing of bonds, options, and other financial instruments, as well as for risk management and portfolio optimization.

---

**Next Steps**:  
- Add additional interest rate models like **Hull-White** or **Black-Karasinski**.
- Further tests with real market data to ensure accuracy and robustness of the models.
- Expand the implementation to handle **interpolation** and **extrapolation** for missing time points.

---

**Files Changed**:
- `term_structure_models.py` – Added methods for calculating rates, discount factors, and forward rates.
- `README.md` – Updated with explanations of the models and usage examples.

---

Let me know if you need further details or additional explanations on any of the models!
