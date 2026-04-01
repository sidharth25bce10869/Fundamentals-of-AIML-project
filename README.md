# Sea Waves Predictor using Intelligent Agent

## Project Overview
This project is a Sea Waves Predictor that estimates wave characteristics using environmental parameters such as wind speed, duration, fetch, sea depth, tides, and ocean currents.

It is based on the concept of an Intelligent Agent which:
- Takes input from the environment
- Processes it using mathematical models
- Produces wave predictions and graphs

## Objectives
- To design an intelligent agent-based system for wave prediction
- To simulate real-world ocean conditions
- To apply a simple machine learning-inspired correction factor

## Methodology

### Agent-Based Approach
The system is implemented using a WaveAgent class which performs:
- Perception: Takes user input
- Computation: Calculates wave height
- Action: Displays results and graph

### Input Parameters
- Wind Speed (m/s)
- Wind Duration (hours)
- Fetch (km)
- Sea Depth (m)
- Tide Level (m)
- Current Speed (m/s)

### Wave Height Calculation
Base formula:
Hs = V^2 / g

Where:
V = Wind Speed
g = 9.81 m/s^2

Final wave height is calculated by applying correction factors:
- Duration factor
- Fetch factor
- Depth factor
- Tide factor
- Current factor

### Machine Learning Correction
Hs(corrected) = 0.85 * Hs

### Wave Range Estimation
Maximum Wave Height = 1.86 * Hs
Minimum Wave Height = 0.3 * Hs

### Probability Distribution
P = 1 - e^(-(H/Hs)^2)

## Technologies Used
- Python
- NumPy
- Matplotlib

## How to Run

1. Install required libraries:
pip install numpy matplotlib

2. Run the program:
python Sea_Waves_Predictor.py

3. Enter input values when prompted

## Output
- Significant Wave Height (Hs)
- Maximum and Minimum Wave Heights
- Wave Height vs Probability graph

## Applications
- Marine navigation
- Coastal engineering
- Weather forecasting
- Ocean research

## Advantages
- Simple and easy to use
- Uses multiple environmental factors
- Provides graphical output

## Limitations
- Uses simplified formulas
- ML correction is not based on real training
- Depends on user input accuracy

## Future Enhancements
- Real-time weather data integration
- Advanced machine learning models
- GUI interface
- More accurate ocean simulation

## Conclusion
This project demonstrates how intelligent agents can be used in environmental modeling to predict sea wave behavior effectively.
