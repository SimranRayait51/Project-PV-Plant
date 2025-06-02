# PV Plant Performance Ratio (PR) and Global Horizontal Irradiance (GHI) Analysis

## Overview

This project processes and visualizes the daily Performance Ratio (PR) and Global Horizontal Irradiance (GHI) data of a photovoltaic (PV) plant. The goal is to analyze the plant's performance over time, comparing it against a dynamically calculated budget line and visualizing key trends.

## Dataset

The raw data consists of two parameters:

- **PR (Performance Ratio):** Tracks daily PV plant performance; higher values indicate better performance.
- **GHI (Global Horizontal Irradiance):** Tracks daily solar irradiation; higher values indicate sunnier days.

The data is organized by year-month and parameter in separate folders.

## Data Processing

- The script reads all CSV files from the `PR` and `GHI` directories.
- It merges the data into a single CSV file named `single_csv.csv` with columns: `Date`, `GHI`, and `PR`.
- The processed data contains 982 rows (daily records).
  
## Visualization

- The visualization script generates a scatter plot where:
  - The x-axis is the date.
  - The scatter points show daily PR values.
  - Points are color-coded based on GHI ranges:
    - < 2: Navy blue
    - 2 - 4: Light blue
    - 4 - 6: Orange
    - \> 6: Brown
  - A red line shows the 30-day moving average of PR.
  - A dark green budget line shows a decreasing target PR value annually (not hardcoded).
  - The plot also highlights points above the budget and shows average PR values for various recent periods.
