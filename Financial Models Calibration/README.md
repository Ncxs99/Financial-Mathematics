**Financial Models Calibration**  

This repository is dedicated to exploring the calibration of financial and volatility models, with a focus on using advanced optimization techniques. The goal is to develop a robust framework for fitting these models to data, making them more applicable for real-world financial analysis and risk management.  

### Current Progress  
At this stage, we have successfully calibrated the Ornstein-Uhlenbeck (OU) model using three distinct approaches:  
1. **Stochastic Optimization**: Leveraging the Autograd functionality in PyTorch, we implemented a stochastic optimization routine to fine-tune the parameters of the OU model. This approach highlights the potential of modern machine learning libraries in the realm of financial modeling.  
2. **Ordinary Least Squares (OLS)**: A classic and widely-used statistical method, OLS provides a straightforward and efficient way to estimate the model parameters by minimizing the residual sum of squares.  
3. **Maximum Likelihood Estimation (MLE)**: As one of the most rigorous and theoretically sound methods, MLE was applied to derive parameter estimates by maximizing the likelihood function, ensuring an optimal fit to the data.  

### Future Plans  
This is just the beginning. The repository will be continuously expanded to include calibrations of other financial models, such as stochastic volatility models, jump-diffusion models, and potentially machine learning-inspired approaches. We also aim to benchmark the performance of different methods across these models to provide insights into their relative strengths and weaknesses.  

Whether you're a financial engineer, a data scientist, or simply someone interested in the intersection of finance and optimization, we hope this project serves as a valuable resource. Contributions and feedback are welcome as we continue to build out this repository!  
