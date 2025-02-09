**American Options**  

This repository is dedicated to the in-depth study of American options, focusing on both theoretical proofs and practical pricing methodologies. American options differ from their European counterparts due to the flexibility they offer in early exercise, making their valuation more complex and requiring specialized techniques.  

### **In This Repository, we will find**  

1. **Mathematical Proofs and Theoretical Foundations**  
   - We present and rigorously demonstrate the most common proofs related to American options. These include fundamental properties such as the early exercise premium and relationships between American and European options.  
   - We also explore conditions under which early exercise is optimal, providing insights into the factors influencing American option behavior.  

2. **Pricing Methods for American Options**  
   - Given the lack of a closed-form analytical solution for most American options, we will implement and compare various pricing approaches, including:  
     - **Binomial Trees**: A discrete-time approach that models stock price movements and determines optimal exercise policies at each step.  
     - **Monte Carlo Simulation**: While traditionally more suited for European options, we examine techniques such as Least Squares Monte Carlo (LSM) for approximating American option values.  
     - **Linear Programming & Dynamic Programming**: Alternative approaches for efficiently computing option prices and exercise boundaries.  
     - **Analytical Approximations**: Discussion of common heuristics and semi-analytical methods that provide fast and reasonably accurate pricing estimates.  

3. **Comparative Analysis & Performance Considerations**  
   - We analyze the trade-offs between different pricing methods, considering accuracy, computational efficiency, and convergence properties.  
   - Special attention is given to high-dimensional options and scenarios where standard techniques may fail or require modifications.  
