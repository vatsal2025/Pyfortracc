# PyForTraCC Enhanced: Tracking & Forecasting Atmospheric Systems
📖 Overview

This repository contains an enhanced implementation of PyForTraCC with:

✅ Support for NetCDF/HDF5 input files (not available in the original PyForTraCC).

✅ A physics-aware machine learning forecasting module (Wide & Deep hybrid model).

✅ End-to-end pipeline for tracking, analyzing, and forecasting convective cloud clusters.

It is designed for meteorologists, researchers, and data scientists working with satellite data who want both tracking and short-term forecasting capabilities.

✨ Key Features

Extended Data Input

Direct support for NetCDF & HDF5 datasets.

Automated variable detection (temperature, latitude, longitude).

Tracking

Improved PyForTraCC-based detection of convective systems.

Handles splits, merges, growth, decay, and dissipation.

Outputs system lifecycles, trajectories, and movement vectors.

Forecasting (Newly Added)

Physics-aware Wide & Deep ML architecture.

Forecasts brightness temperature evolution.

Constrained by physical laws → realistic predictions.

Visualization

System trajectory animations.

Diagnostic plots: size evolution, intensity changes, movement dynamics.

Statistical summaries (DuckDB-based).

📂 Repository Structure
├── Pyfortracc_Tracking_&_Enhanced_Forecasting.ipynb   # Main notebook
├── data/                                             # Place NetCDF/HDF5 input files here
├── output/                                           # Tracking and forecast outputs
├── requirements.txt                                  # Dependencies
└── README.md                                         # Project documentation

⚙️ Installation

Clone this repo

git clone https://github.com/yourusername/pyfortracc-enhanced.git
cd pyfortracc-enhanced


Install dependencies

pip install -r requirements.txt


Run Jupyter Notebook / Colab
Open the main notebook:

jupyter notebook Pyfortracc_Tracking_&_Enhanced_Forecasting.ipynb

▶️ Usage
1. Upload NetCDF/HDF5 Files

Place your .nc or .hdf5 files in the data/ folder.

The notebook automatically detects variables (temperature, lat, lon).

2. Configure Parameters

Set thresholds:

Warm cloud = 235K

Cold cloud = 200K

Adjust cluster size filtering if needed.

3. Run Tracking

Detects cloud systems across time steps.

Outputs lifecycle statistics, trajectories, and movement vectors.

4. Forecasting (New)

Uses physics-aware Wide & Deep ML model.

Produces short-term temperature forecasts.

Ensures outputs remain meteorologically realistic.

📊 Results (Example)

Tracking: Successfully identified both short-lived convective events and long-lived mesoscale systems.

Forecasting: Achieved 2–4K RMSE with <5% physical violations (temperature outside 150–350K).

Visualization: Generated animations and diagnostic plots for lifecycle analysis.

📦 Requirements

Main dependencies:

pyfortracc (core algorithm)

xarray, numpy, pandas (data handling)

matplotlib, ipywidgets (visualization/UI)

duckdb (tracking result queries)

torch, lightgbm (forecasting models)

Install all with:

pip install -r requirements.txt

🚀 Your Contributions vs Original PyForTraCC

🔹 Original PyForTraCC: Limited to specific formats, tracking-only.

🔹 This Repo:

Added NetCDF/HDF5 input compatibility.

Added physics-aware ML forecasting.

Built an end-to-end workflow (tracking → analysis → forecasting → visualization).

📌 Future Work

Extend forecasts to spatial fields (not just point-based).

Add uncertainty quantification in forecasts.

Optimize for real-time streaming satellite data.

🤝 Acknowledgements

Original FORTRACC methodology.

PyForTraCC library.

Open-source ML & meteorological data analysis community.

📜 License

MIT License.
