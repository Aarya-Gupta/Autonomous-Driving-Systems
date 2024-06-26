import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import norm

# Define prior distribution (e.g., normal distribution)
prior_mu = 0
prior_sigma = 1
prior = norm(prior_mu, prior_sigma)

# Print prior distribution parameters
print(f"Prior distribution: mean = {prior_mu}, sigma = {prior_sigma}")

# Define a range of x values
x = np.linspace(-3, 3, 100)

# Compute and print the PDF values for the prior distribution
prior_pdf_values = prior.pdf(x)
print("Prior distribution PDF values:")
for value in prior_pdf_values:
    print(value, end = " ")
print("\n\n\n\n")
# Plot prior distribution
plt.plot(x, prior_pdf_values, label='Prior')
plt.legend()
plt.show()

# Collect data (e.g., observed mean and variance)
data_mu = 0.5
data_sigma = 0.1

# Update distribution using Bayes' theorem
posterior_mu = (prior_sigma**2 * data_mu + data_sigma**2 * prior_mu) / (prior_sigma**2 + data_sigma**2)
posterior_sigma = np.sqrt((prior_sigma**2 * data_sigma**2) / (prior_sigma**2 + data_sigma**2))
posterior = norm(posterior_mu, posterior_sigma)

# Print posterior distribution parameters
print(f"Posterior distribution: mean = {posterior_mu}, sigma = {posterior_sigma}")

# Compute and print the PDF values for the posterior distribution
posterior_pdf_values = posterior.pdf(x)
print("Posterior distribution PDF values:")
for value in posterior_pdf_values:
    print(value, end = " ")
print()
# Plot posterior distribution
plt.plot(x, posterior_pdf_values, label='Posterior')
plt.legend()
plt.show()
