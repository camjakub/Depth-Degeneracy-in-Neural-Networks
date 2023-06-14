# Depth Degeneracy in Neural Networks
This repository contains the code used to produce the main figures in two papers I have worked on during my Master's degree. My research involves studying the "large depth degeneracy phenomenon" in neural networks, where inputs tend to get more correlated as they treavel through the layers of an initialized network. Networks which exhibit this type of degeneracy may have a hard time distinguishing between inputs, which can lead to poor training performance.

## Angle_Evolution
This folder contains a Google Colab notebook which produces the plots in Figure 1 of _Depth Degeneracy in Neural Networks: Vanishing Angles in Fully Connected ReLU Networks on Initialization_ (Cameron Jakub and Mihai Nica, 2023a), which can be found at the following [link](https://arxiv.org/abs/2302.09712). This paper was submitted to the Journal of Machine Learning Research. Figure 1 from our paper is shown below.

| ![Figure_1](Angle_Evolution/Figure_1.png) |
| :--: | 
| Figure 1: We feed 2 inputs with initial angle $\theta^0 = 0.1$ into 5000 Monte Carlo samples of independently initialized networks with network width $n_\ell = 256$ for all layers. Left: Using the Monte Carlo samples, we plot the empirical mean and standard deviation of $\ln(\sin^2(\theta^\ell))$ at each layer. We compare this to both the infinite width update rule and our prediction using Approximation 1 for the mean of $\ln(\sin^2(\theta^\ell))$. Our prediction for the standard deviation in each layer using Approximation 2 is also plotted as the shaded area. In contrast to our prediction, the infinite width rule predicts 0 variance in all layers. Right:  We plot histograms of our simulations as well as our predicted probability density function using Approximation 2 from (10) at Layer 1 (top) and Layer 30 (bottom). The predicted and empirical distribution are statistically indistinguishable according to a Kolmogorov-Smirnov test, with $p$ values $0.987 > 0.05$ (top) and $0.186  > 0.05$ (bottom). |

## Training_Performance


### References
Cameron Jakub and Mihai Nica. Depth degeneracy in neural networks: Vanishing angles in
fully connected ReLU networks on initialization, 2023a. URL https://arxiv.org/abs/2302.09712

Cameron Jakub and Mihai Nica. Network degeneracy as an indicator of training performance: Comparing finite and infinite width angle predictions, 2023b. URL https://arxiv.org/abs/2306.01513


