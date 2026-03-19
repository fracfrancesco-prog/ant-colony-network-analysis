# 🐜 Ant Colony Communication Network Analysis

Analysis of social interactions within an ant colony using graph theory and network analysis techniques.

## Overview

This project models the communication network of an ant colony over 3 days, where:
- **Nodes** represent individual ants
- **Edges** represent mandible contacts (the primary communication mechanism used by ants)
- Data was collected over 20-minute observation windows per day

The goal is to understand how information flows through the colony by analyzing the structure of the interaction network.

## Analysis

For each day (and for combined multi-day graphs), the project computes:

- **Degree Centrality** — how many ants each ant communicated with
- **Betweenness Centrality** — how important each ant was for information diffusion across the colony
- **Eigenvector Centrality** — whether each ant was connected to other influential ants (inspired by Google's PageRank algorithm)
- **Community Detection** — which groups of ants communicated prevalently with each other (Louvain method)
- **Bridge Detection** — which connections prevented the colony from splitting into isolated groups
- **Adjacency Matrix** — alternative visual representation of the graph

> **Note:** Closeness centrality was deliberately excluded, as average node proximity was not considered relevant for interpreting colony communication dynamics.

## Results

The analysis identifies, for each observation day:
- The most and least connected ants
- The key "bridge" ants whose removal would fragment the colony
- The main communication communities within the colony
- An overall importance ranking combining all three centrality measures

## Tech Stack

- **Python 3**
- **NetworkX** — graph construction and analysis
- **Matplotlib** — visualization

## Project Structure

```
ant-colony-network-analysis/
│
├── progetto.py        # Main analysis script
├── data/              # Edge list files (one per day)
│   ├── giorno_1.txt
│   ├── giorno_2.txt
│   └── giorno_3.txt
└── README.md
```

## How to Run

```bash
# Install dependencies
pip install networkx matplotlib

# Run the analysis
python progetto.py
```

The script will prompt you to select which days to analyze (individually or combined).

## Background

This project was developed as part of an **InfoMath** advanced coursework program, which covers topics including graph theory, linear algebra (matrices and eigenvectors), and data analysis with Python. The analysis was presented to researchers at the University of Modena and Reggio Emilia.

## Author

High school student — Liceo Scientifico Scienze Applicate, Italy (2025–26)
