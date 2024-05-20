# Kinematic Bicycle Model Trajectories

This repository contains Python code to simulate trajectories using a kinematic bicycle model. The model is implemented without slip angle consideration but can be implemented with slip angle, by swaping the function **kinematic_bicycle_model** to **kinematic_bicycle_model_w_slip** with an additional argument **lr** (distance of centre of mass from rear end) being added. Trajectories are generated for both simple and complex scenarios (No constraint on steering angle).

## Requirements

- Python 3.x
- Required Python libraries: `numpy`, `matplotlib`, `pandas`, `plotly`, `random`

## Overview

The code simulates trajectories of a vehicle using a kinematic bicycle model. Two versions of the model are provided:

1. **Simple Kinematic Bicycle Model**: This version considers a basic kinematic bicycle model in which trajectories are generated with random steering angles within a small predefined range.

2. **Complex Kinematic Bicycle Model**: This version extends the simple model by incorporating complex steering angles. Trajectories are generated with steering angles in a wider range, including the possibility of reversing the vehicle's direction.

## Code Structure

- `Kinematic_Bicycle_Model.py`: Contains the implementation of the kinematic bicycle model functions and plot some sample paths with varied parameters.
- `README.md`: This file, providing an overview of the repository and instructions for usage.

## Usage

1. Clone the repository:

    git clone https://github.com/Aarya-Gupta/Autonomous-Driving-Systems.git

2. Navigate to the repository directory:

    cd Autonomous-Driving-Systems

3. Run the `Kinematic_Bicycle_Model.py` script to generate and visualize trajectories:

    python Kinematic_Bicycle_Model.py

## Acknowledgments

- This code is based on the kinematic bicycle model concept widely used in vehicle dynamics simulation.
- Inspiration for the implementation and visualization techniques were drawn from various online resources and literature on vehicle dynamics.