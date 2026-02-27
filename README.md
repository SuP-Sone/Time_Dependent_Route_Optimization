# Route Optimization with Time-Dependent Travel Times

This project contains a routing / scheduling optimization workflow implemented in a Jupyter notebook.

The notebook solves a **vehicle routing problem (VRP)** where travel times vary depending on conditions (time-dependent travel times). The pipeline includes:

- Data input and preprocessing
- Visualization
- Distance and travel-time matrix construction
- Optimization modeling (MILP workflow)
- Result evaluation and analysis

---

## Overview

Real-world routing problems rarely have constant travel times. Traffic, congestion, and time-of-day effects change the cost of moving between locations.

This notebook explores:

- Building routing graphs from geographic coordinates
- Estimating travel time and distance matrices
- Running optimization to find efficient vehicle routes
- Comparing estimated vs. true travel times
- Visualizing results

---

## Key Concepts

- **Vehicle Routing Problem (VRP)** – assigning routes to vehicles while minimizing cost or time.
- **Time-dependent travel times** – edge weights vary depending on departure time.
- **MILP (Mixed Integer Linear Programming)** – optimization framework used for route decisions.
- **Graph modeling** – routes represented using network graphs.

---

## Project Structure

```
Routing_Optimization.ipynb   # Main notebook (core workflow)
data/                        # Input datasets (CSV files)
```
> The notebook is designed to be run sequentially from top to bottom.

---

## Requirements

Install dependencies using the provided requirements file:

```bash
pip install -r requirements.txt
```
---

## API Setup 

Some steps use Google Maps for travel-time estimation.

1. Create a `.env` file in the project root:

```bash
GOOGLE_MAPS_API_KEY=your_api_key_here
```

2. Make sure the key has access to relevant APIs (Distance Matrix / Directions).

Or you can use the saved / manual graph and distance matrix.

---

## Inputs

Typical inputs include:

- Depot location (first entry)
- List of coordinates (latitude, longitude)
- Cost parameters (€/km, time value, etc.)
- Travel-speed datasets (mean vs. true values)

Example:

```python
coords_list = [
    "lat,lng",
    ...
]
```

---

## Outputs

The notebook generates:

- Route assignments
- Optimized schedules
- Travel-time comparisons
- Visual plots of routes and performance

---

## Notes

- The workflow mixes deterministic optimization with data-driven travel-time estimates.
- Performance depends heavily on input data quality.
- Large instances may require solver tuning or computational optimization.

---

## 👤 Author

Su Pyae Sone
