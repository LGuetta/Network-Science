# Airline Network Analysis

This project explores the structural and functional properties of the global airline network using the OpenFlights dataset. By applying network science principles, we uncover hidden patterns and provide insights into community structures, connectivity, and network resilience.

## Table of Contents
1. [Introduction](#introduction)
2. [Key Features](#key-features)
3. [Data Description](#data-description)
4. [Methods](#methods)
5. [Results](#results)
6. [Conclusion](#conclusion)
7. [How to Run the Code](#how-to-run-the-code)
8. [Contributors](#contributors)

---

## Introduction
Airline networks are critical to global connectivity, offering insights into regional interdependencies and operational efficiencies. This project applies structural and robustness analyses to identify key patterns and vulnerabilities within the network.

---

## Key Features
- **Structural Analysis**:
  - Degree distribution (\( \gamma = 1.85 \), \( k_x = 180 \)).
  - Clustering coefficients (global and local).
  - Small-world property (\( \langle l \rangle = 3.99 \)).
  - Community detection (Louvain algorithm, 18 geographic communities).
- **Robustness Analysis**:
  - Impact of targeted vs. random node removal.
  - Largest connected component resilience.
- **Centrality Metrics**:
  - Degree, betweenness, closeness, eigenvector, and PageRank centralities.

---

## Data Description
The dataset was sourced from [OpenFlights](https://openflights.org/), containing:
- **Airports**: 9,407 nodes with attributes (name, country, coordinates).
- **Routes**: 37,505 edges representing direct flight connections.

---

## Methods
1. **Data Cleaning**:
   - Removed missing/duplicate entries.
   - Validated routes and airport IDs.
2. **Network Construction**:
   - Single-layer directed graph.
   - Weighted edges (geographic distance).
3. **Community Detection**:
   - Louvain algorithm for modularity-based clustering.
   - Clique Percolation Method (CPM) for overlapping communities.
4. **Structural Metrics**:
   - Degree distribution, clustering coefficients, path lengths.
5. **Robustness Analysis**:
   - Simulated node removal strategies (high/low degree, random).

---

## Results
- **Structural Properties**:
  - Scale-free and small-world network characteristics.
  - Distinct geographic communities aligned with regional operations.
- **Centrality Insights**:
  - Amsterdam, Frankfurt, and Charles de Gaulle rank highest by eigenvector centrality.
- **Robustness**:
  - Hubs are critical for connectivity, with significant fragmentation under targeted attacks.

---

## Conclusion
The global airline network is efficient and modular, balancing connectivity with regional clusters. Future work could explore delay propagation and optimize infrastructure planning.

---

## How to Run the Code
1. Clone the repository:
   ```bash
   git clone https://github.com/LGuetta/airline-network-analysis.git
