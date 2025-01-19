# Pandas_Hotel_analytics
This project focuses on analyzing hotel booking data using pandas. It provides insights into key metrics such as occupancy percentages, booking trends, and room category performance. The project is designed to help hotel management make data-driven decisions to optimize operations and revenue.
Features

## Data Cleaning and Preparation

- Handled missing values and duplicates.

- Standardized column names for consistency.

- Converted data types where necessary (e.g., dates and percentages).

## Data Analysis

- Aggregated metrics like occupancy percentage (occ_pct) by day type, room category, and booking platform.

- Identified high-performing room categories.

- Compared weekday and weekend performance.

## Visualization

- Generated charts and graphs to visualize booking trends.

- Highlighted differences in occupancy percentages for weekdays vs. weekends.

## Custom Filtering and Aggregation

- Applied conditional logic to filter and compare aggregated results.

- Used group-by operations to analyze data at different levels.

# Setup Instructions

## Prerequisites

- Python 3.8+

- pandas

- matplotlib (optional for visualization)

- seaborn (optional for visualization)

# Installation

## Clone the repository:

git clone https://github.com/yourusername/hotel-analytics.git
cd hotel-analytics

## Install dependencies:

pip install -r requirements.txt

## Run the Jupyter Notebook or Python script:

jupyter notebook hotel_analytics.ipynb
 Or
python hotel_analytics.py

# Usage

## Key Operations

## Aggregate and Analyze:
Use groupby operations to calculate metrics like occupancy percentage by various dimensions (e.g., day_type, room_category).

## Apply Conditional Logic:
Compare metrics such as weekend vs. weekday performance using pandas filtering.

## Visualize Trends:
Create plots to display trends and key insights, helping stakeholders understand data visually.

# Example Code Snippets

## Aggregate Occupancy Percentage by Room Category

import pandas as pd

# Group by room category and calculate the mean occupancy percentage
df_agg = df.groupby('room_category')['occ_pct'].mean()
print(df_agg)

# Aggregate by day type
aggregated = df.groupby('day_type')['occ_pct'].sum()

# Extract and compare
weekend_sum = aggregated.get('weekend', 0)
weekday_sum = aggregated.get('weekday', 0)

if weekend_sum > weekday_sum:
    print(f"Weekend has higher occupancy: {weekend_sum}")
elif weekday_sum > weekend_sum:
    print(f"Weekday has higher occupancy: {weekday_sum}")
else:
    print("Both have the same occupancy")

# Folder Structure
hotel-analytics/
|— data/               # Contains sample CSV files for analysis
|— notebooks/          # Jupyter notebooks with step-by-step analysis
|— scripts/            # Python scripts for automated execution
|— visuals/            # Saved visualizations (e.g., PNG, JPEG)
|— README.md          # Project documentation (this file)


