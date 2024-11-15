### **TermStructureClassInterpolated: A Highly Flexible Term Structure Class for Yield Curve Analysis**

---
  
### Enhance Flexibility with Linear Interpolation for Yield, Discount Factor, and Forward Rate Calculations

---

Introducing the **TermStructureClassInterpolated** — a highly flexible class designed for dynamic modeling and analysis of interest rate term structures. This class combines the simplicity of linear interpolation with the power to calculate discount factors, forward rates, and interest rate yields at any time, providing users with robust tools for analyzing yield curves in various market conditions.

### **Key Features**:
- **Linear Interpolation**: The class supports **linear interpolation** for yield estimation, allowing us to easily calculate the yield at any given time \( T \) based on observed data points.
- **Discount Factor and Forward Rate Calculation**: In addition to yield curve estimation, the class enables the calculation of **discount factors** and **forward rates** at any time, derived from the interpolated yields.
- **Flat Term Structure Override**: For scenarios where a constant interest rate is needed across all maturities, the class allows users to manually set a **flat term structure**, overriding interpolation for faster and simpler calculations.
- **Customizable Observations**: The class supports custom **time** and **yield** observations, making it adaptable to different yield curve configurations and user preferences.

### **How It Works**:
- **Yield Calculation**: The `r(T)` method provides the yield at any given time \( T \), utilizing linear interpolation between provided time-yield points. If a flat rate is provided, the class returns this rate across all maturities.
- **Discount Factor**: With the interpolation of yields, discount factors can be derived for any given time period.
- **Forward Rate**: Similarly, forward rates between two given times can be computed using the relationship between discount factors at those points.

### **Next Steps**:
- We will be adding additional interpolation methods, such as **cubic splines**, to further enhance the flexibility of the term structure model.
- Future updates will include more complex methods for interest rate modeling, providing even greater flexibility and precision for financial calculations.

---

**Files Changed**:
- `term_structure_class_interpolated.py` – Implemented linear interpolation, discount factor, forward rate calculations, and flat rate override.
- `README.md` – Updated with explanations on how to use the class for interpolation, discount factor, and forward rate calculations.

---

**Why Choose `TermStructureClassInterpolated`**:
This class is a powerful and adaptable tool for anyone working with interest rate models. Whether you're analyzing financial markets, conducting risk assessments, or forecasting interest rates, the flexibility to manually set a flat term structure or use interpolation for precise estimations at arbitrary times makes **TermStructureClassInterpolated** a versatile solution. With plans to extend functionality to include **cubic splines** and other advanced techniques, this class will continue to evolve as a comprehensive tool for yield curve analysis.
