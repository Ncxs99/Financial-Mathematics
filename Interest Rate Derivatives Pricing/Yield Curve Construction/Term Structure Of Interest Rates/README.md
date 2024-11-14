# TermStructureClassInterpolated: A Flexible Term Structure for Yield Curve Analysis

Welcome to **TermStructureClassInterpolated** — a highly adaptable and powerful class for modeling term structures in finance! This class is designed to provide exceptional flexibility by supporting both *flat* and *non-flat* term structures, allowing users to leverage a variety of yield curve scenarios with ease. Below, we walk through the core functionality and features that make this class an ideal tool for yield curve modeling and analysis.

---

### Overview

The `TermStructureClassInterpolated` class extends both `TermStructureClass` and `TermStructure`, inheriting essential yield and discount factor calculation methods. It introduces a specialized interpolation feature to estimate yields at arbitrary times and can seamlessly switch between flat and non-flat term structures, enabling dynamic modeling and forecasting.

### Key Features
- **Flexible Term Structure**: Supports both constant (flat) and variable (non-flat) term structures, providing options for different financial modeling needs.
- **Linear Interpolation**: Enables yield estimation at any time by interpolating between given points, ideal for creating a smooth yield curve.
- **Override Capability with Flat Rate**: Allows a flat rate to override interpolation, useful for quick calculations or when a flat term structure is assumed.
- **Customizable Observations**: Users can set custom times and yields for precise and tailored yield curve configurations.

### Class Initialization

```python
def __init__(self, times=None, yields=None, flat_rate=None)
```

The constructor accepts three optional parameters:
- `times`: A list of times for observed yields.
- `yields`: A list of yields corresponding to the times provided.
- `flat_rate`: An optional constant rate to use across all maturities. This will override any interpolation if provided.

> **Flexible Structure**: If `flat_rate` is defined, it will be used as the yield for any time `T`. If not, the class will interpolate based on `times` and `yields`.

### Method Highlights

#### `r(T)`: Yield at Time `T`
The `r` method is the central function for retrieving the yield at a specified time:
- If `flat_rate` is set, `r` will return this constant rate for all maturities.
- Otherwise, it employs `linear_interpolation` to estimate the yield at time `T`.

```python
def r(self, T)
```

#### `linear_interpolation(T, times, yields)`: Interpolate Yield at Time `T`
When a flat rate is not provided, `linear_interpolation` performs a linear interpolation to estimate yields. It iterates through `times` and calculates a yield for any `T` within the specified range. If `T` falls outside the bounds of `times`, an error is raised.

```python
def linear_interpolation(self, T, times, yields)
```

#### `clear()`: Clear Observations
The `clear` method removes all entries from the `times` and `yields` lists, providing a quick reset function.

```python
def clear(self)
```

#### `set_interpolated_observations(in_times, in_yields)`: Set Observations for Interpolation
To update the yield curve with new data, `set_interpolated_observations` accepts lists of `in_times` and `in_yields`, enforcing that both lists must have the same length.

```python
def set_interpolated_observations(self, in_times, in_yields)
```

### Example Usage

```python
# Initialize with custom observations and no flat rate
term_structure = TermStructureClassInterpolated(
    times=[1, 2, 3, 5, 10],
    yields=[0.02, 0.025, 0.03, 0.035, 0.04]
)

# Retrieve yield at an interpolated time
print(term_structure.r(4))  # Interpolates yield for time T=4

# Use a flat rate
term_structure_with_flat = TermStructureClassInterpolated(flat_rate=0.03)
print(term_structure_with_flat.r(4))  # Returns flat rate of 0.03 for all T
```

---

### Why Choose `TermStructureClassInterpolated`?
With its ability to handle both flat and interpolated structures, this class is ideal for users needing flexible and customizable yield calculations. Whether you are conducting financial research, building risk models, or analyzing investment scenarios, `TermStructureClassInterpolated` adapts to your requirements, making it a robust choice for any yield curve application.
