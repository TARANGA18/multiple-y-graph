import numpy as np
import matplotlib.pyplot as plt

# Data for the first set
x1 = np.array([0.5, 1, 1.5, 2, 2.5])
y_values1 = [
    [2.09, 1.99, 1.95, 1.81, 1.76],  # y1
    [2.12, 2.11, 2.08, 2.04, 2.03],  # y2
    [2.09, 2.08, 2.08, 2.08, 2.07]  # y3
]

# Data for the second set
x2 = np.array([0.843, 1.012, 1.976, 2.891, 3.961])
y2 = np.array([1.96, 1.93, 1.8, 1.64, 1.57])

# Plot the first set of data
plt.figure(figsize=(8, 5))
markers = ['o', 's', '^']  # Different bullet points for each material
colors = ['#6baed6', '#fd8d3c', '#74c476']  # Softer color palette
for i, y in enumerate(y_values1):
    # Fit a straight line
    slope, intercept = np.polyfit(x1, y, 1)
    material = ["Iron", "Aluminum", "Plexiglass"][i]
    print(f"Slope of {material} (Set 1): {slope:.4f}")

    # Plot data points and fitted line
    plt.plot(x1, y, markers[i], color=colors[i], label=f'{material}', markersize=5, linestyle='')
    plt.plot(x1, slope * x1 + intercept, '-', color=colors[i], linewidth=1)

# Fit a straight line for the second set of data
slope, intercept = np.polyfit(x2, y2, 1)
print(f"Slope of Lead (Set 2): {slope:.4f}")

# Plot data points and fitted line for the second set
plt.plot(x2, y2, 'd', color='#fdae6b', label='Lead', markersize=5, linestyle='')  # Softer diamond marker
plt.plot(x2, slope * x2 + intercept, '-', color='#fdae6b', linewidth=1)

# Graph formatting for minimalistic look
plt.xlabel("Distance x in cm", fontsize=12, labelpad=10)
plt.ylabel("log(N/min)", fontsize=12, labelpad=10)
plt.title("Linear Fits for Different Materials", fontsize=14, pad=15)
plt.legend(fontsize=10, frameon=False)
plt.grid(visible=True, linestyle='--', linewidth=0.5, alpha=0.5)
plt.xticks(fontsize=10)
plt.yticks(fontsize=10)
plt.tight_layout()
plt.savefig("minimalistic_graph.png", dpi=300, bbox_inches='tight')
plt.show()
