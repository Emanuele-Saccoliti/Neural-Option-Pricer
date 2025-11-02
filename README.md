# Repository Description

This project explores the use of feed-forward Artificial Neural Network (ANN) to learn the pricing map of European call options in the Black–Scholes framework, replacing the analytical formula with a data-driven surrogate model.

While the Black–Scholes price is known in closed form, this experiment serves as a benchmark to evaluate the capability of neural networks to approximate financial pricing functions, offering a foundation for more sophisticated models where closed-form solutions are not available (e.g., rough volatility models).


# 🔍 Key Objectives
* Construct a synthetic dataset of option prices from the Black–Scholes model
* Train a neural network to approximate the pricing map
* Evaluate interpolation vs. extrapolation performance
* Test fundamental arbitrage-free properties (e.g., homogeneity, monotonicity)


# 📌 Key Takeaways
* Neural networks can accurately learn the pricing function within the training domain
* Structural option pricing properties are not guaranteed without constraints
* Demonstrates the importance of incorporating financial structure & no-arb conditions


# ⚠️ Key Challenges
* Recovering structural properties of option prices: Ensuring the network learns financial structure, not just numerical fitting.
* Avoiding arbitrage violations: NN trained purely on MSE can violate no-arbitrage constraints like Call spread arbitrage (monotonicity), Butterfly arbitrage (convexity), Calendar arbitrage.
* Extrapolation instability: The model performs well in-domain but fails outside the training region.
