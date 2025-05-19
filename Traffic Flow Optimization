import matplotlib.pyplot as plt
import numpy as np

# Traffic flow parameters
road1_traffic = 100  # vehicles per hour
road2_traffic = 150  # vehicles per hour
saturation_flow_rate = 1800  # vehicles per hour
cycle_length = 90  # seconds
green_time_road1 = 40  # seconds
green_time_road2 = cycle_length - green_time_road1  # Remaining time for Road 2

# Calculate the capacity of each road
capacity_road1 = (green_time_road1 / cycle_length) * saturation_flow_rate
capacity_road2 = (green_time_road2 / cycle_length) * saturation_flow_rate

# Calculate the degree of saturation for each road
degree_of_saturation_road1 = road1_traffic / capacity_road1
degree_of_saturation_road2 = road2_traffic / capacity_road2

# Print the results
print(f"Degree of saturation for Road 1: {degree_of_saturation_road1:.2f}")
print(f"Degree of saturation for Road 2: {degree_of_saturation_road2:.2f}")

# Plot the results
plt.bar(["Road 1", "Road 2"], [degree_of_saturation_road1, degree_of_saturation_road2])
plt.xlabel("Road")
plt.ylabel("Degree of Saturation")
plt.title("Traffic Flow Optimization")
plt.show()

# Optimize the green time for each road to minimize congestion
optimal_green_time_road1 = (road1_traffic / (road1_traffic + road2_traffic)) * cycle_length
optimal_green_time_road2 = cycle_length - optimal_green_time_road1

# Calculate the optimal degree of saturation for each road
optimal_capacity_road1 = (optimal_green_time_road1 / cycle_length) * saturation_flow_rate
optimal_capacity_road2 = (optimal_green_time_road2 / cycle_length) * saturation_flow_rate

optimal_degree_of_saturation_road1 = road1_traffic / optimal_capacity_road1
optimal_degree_of_saturation_road2 = road2_traffic / optimal_capacity_road2

# Print the optimal results
print(f"Optimal degree of saturation for Road 1: {optimal_degree_of_saturation_road1:.2f}")
print(f"Optimal degree of saturation for Road 2: {optimal_degree_of_saturation_road2:.2f}")

# Plot the optimal results
plt.bar(["Road 1", "Road 2"], [optimal_degree_of_saturation_road1, optimal_degree_of_saturation_road2])
plt.xlabel("Road")
plt.ylabel("Optimal Degree of Saturation")
plt.title("Optimal Traffic Flow")
plt.show()
