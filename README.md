# Autonomous-Driving-Systems

This repository contains the work done on the Autonomous Driving Systems project, documented week-wise. This project aims to develop a simplified kinematic model for vehicle motion and explore various statistical methods for confidence interval estimation using bootstrapping.

## Project Structure

The repository is organized into week-wise folders, each containing the work done during that specific week.

### Week 1
- **Work Done:** Developed the kinematic bicycle model from scratch.
- **Folder:** [week1](Week_01)

### Week 2
- **Work Done:** Identified that the parameter of concern is the steering angle and modelled it accordingly.
- **Folder:** [week2](Week_02)

### Week 3
- **Work Done:** 
  - Removed the concept of steering angle and focused on the heading angle as the sole parameter for direction change.
  - Understood the coin toss experiment and created scratch models of bootstrapping for better understanding.
  - The new system equations for the model:
    ```
    x(t) = x(t-Δt) + v * cos(θ(t)) * Δt
    y(t) = y(t-Δt) + v * sin(θ(t)) * Δt
    θ(t) = θ(t-Δt) + Δθ(t)
    ```
  - Assumed Δθ(t) follows a Gaussian (0, 1) and Uniform(-pi/3, +pi/3) distribution [as 2 different cases] for the first iteration.
  - Modified the distribution of Δθ(t) based on its extracted value for subsequent time steps to find x(t) and y(t) distributions.
  - Simulated the coin toss experiment using a similar approach.
- **Folder:** [week3](Week_03)

### Week 4
- **Work Done:** Simulated Kernel Density Estimation (KDE) and compared the output with bootstrapping.
- **Folder:** [week4](Week_04)

### Week 5
- **Work Done:**
  - Compared KDE output with bootstrapping using the same dataset for initial heading angle change.
  - It's not necessary that the list to be sampled is of the same size as the original one during bootstrapping. The size of the list can be variable. In actuality, we are just trying to test the behaviour of bootstrapping, so the size of the newly sampled list can be variable.
- **Folder:** [week5](./Week_05)

### Week 6
- **Work Done:**
  - Documented the work done so far in LaTeX.
  - Created a timeline for events at each time step and listed all assumptions and initial conditions.
- **Folder:** [week6](./Week_06)

### Week 7
- **Work Done:** Focused on reading book content related to Confidence Intervals. [Ch- 12]
- **Folder:** N/A

### Weeks 8 & 9
- **Work Done:** Focused on reading book content related to Confidence Intervals. [Ch- 13, 14]
- **Folder:** N/A

### Weeks 10 & 11
- **Work Done:**
  - Aimed to find an appropriate confidence interval for the true mean of the underlying unknown distribution.
  - Discussed five different approaches for confidence interval estimation:
    1. Standard Normal
    2. Student-t Distribution
    3. Bootstrap-t Distribution
    4. Percentile Method
    5. BCA Method
  - Simulated approaches 1, 2, and 3.
  - General assumptions while coding:
    1. 1000 bootstrapped samples of the given dataset are created.
    2. Considering mean to be the statistic of interest.
- **Folder:** [week10](./week10)

## Guidance

This project has been guided by the book "An Introduction to the Bootstrap" by B. Efron.

## Installation

To set up the project and produce results, follow these steps:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/Aarya-Gupta/Autonomous-Driving-Systems.git
   cd Autonomous-Driving-Systems
   ```
2. **Create and Activate a Virtual Environment:**
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
   ```
