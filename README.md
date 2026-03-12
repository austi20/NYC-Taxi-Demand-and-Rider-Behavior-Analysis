# NYC Taxi Demand and Rider Behavior Analysis

This repository presents an exploratory and modeling-based analysis of New York City yellow taxi trips using a January 2023 trip sample and the NYC taxi zone lookup table. The project combines descriptive analysis, route visualization, and baseline predictive modeling to study how trip timing, distance, location, fare structure, and passenger behavior relate to taxi demand, fare amounts, trip duration, and tipping outcomes.

The work originated as a course project, but this repository has been revised to read as a portfolio-quality case study with clearer setup instructions, tighter scope, and more explicit discussion of methodological limits.

## Project Overview

The central question is:

How do rider behavior patterns across time, location, and trip characteristics relate to taxi demand, trip duration, fares, and tipping outcomes in New York City?

The analysis is organized into five components:

1. Origin-destination route exploration with network visualizations
2. Time-of-day and day-of-week demand analysis
3. Tip likelihood classification
4. Fare amount regression
5. Trip duration regression

## Dataset

This repository uses two files stored at the project root:

- `taxi.csv`: January 2023 NYC yellow taxi trip sample used across the notebooks
- `taxi_zones.csv`: taxi zone lookup table for interpreting pickup and dropoff location IDs

Important scope note:

- The notebook explicitly filters the trip data to January 1 through January 14, 2023.
- Results should therefore be interpreted as a short-window case study, not a full-year or citywide annual trend analysis.
- `taxi.csv` is tracked with Git LFS because of its size.

If the large dataset does not appear after cloning, run:

```bash
git lfs install
git lfs pull
```

## Methods Used

- Data cleaning with `pandas`
- Descriptive demand analysis by hour, day, and weekday/weekend split
- Directed network graphs for popular origin-destination routes
- Ordinary least squares regression for fare modeling
- Linear regression for trip-duration modeling
- Logistic regression with ROC analysis for tip classification
- Visualization with `matplotlib` and `seaborn`

## Key Findings

- Trip demand varies meaningfully by hour of day and by weekday versus weekend periods within the January 1-14 window.
- The most common routes cluster around a relatively small set of zone pairs, which makes the route network highly concentrated rather than evenly distributed across the city.
- Fare amount is strongly associated with trip distance in this sample, and the fare regression achieves a relatively high in-sample fit.
- Trip duration is moderately predictable from a small set of trip-level features, with distance contributing the strongest linear signal among the variables used.
- Tip prediction is weak with the current feature set. The notebook's baseline logistic regression performs only slightly above chance, which suggests that tipping behavior is not well captured by distance, fare amount, and passenger count alone.

## Limitations

- The analysis window covers only January 1-14, 2023, so it cannot capture broader seasonal demand patterns.
- The notebooks use a shortened working sample rather than the complete TLC trip record universe, which limits generalizability.
- Several models use simple linear specifications and minimally engineered features, so the results are better interpreted as baseline explanatory models than production-grade predictive systems.
- Categorical variables such as payment type and location IDs are treated simplistically in parts of the analysis, which can distort interpretation when those variables are encoded as ordinary numeric values.
- Reported findings should be read as evidence from this sample and this time window, not as definitive claims about all NYC taxi behavior.

## Repository Structure

```text
.
|-- README.md
|-- SETUP.md
|-- requirements.txt
|-- ProjectGroup4Final.ipynb
|-- Project_parts_125.ipynb
|-- Project_part_3.ipynb
|-- ProjectDiscussionAndPlanning.md
|-- Group 4 Project Report.pdf
|-- taxi.csv
`-- taxi_zones.csv
```

Notebook roles:

- `ProjectGroup4Final.ipynb`: recommended notebook for review; contains the integrated final analysis
- `Project_parts_125.ipynb`: earlier project stage covering sections 1, 2, 4, and 5
- `Project_part_3.ipynb`: earlier project stage focused on section 3 plus shared preprocessing

## How to Run the Project

1. Clone the repository.
2. Make sure Git LFS is installed, then pull the large dataset if needed.
3. Create a Python virtual environment.
4. Install dependencies with `pip install -r requirements.txt`.
5. Open `ProjectGroup4Final.ipynb` in JupyterLab or Jupyter Notebook.
6. Run the notebook from top to bottom from the repository root so file paths resolve correctly.

For additional setup details, see `SETUP.md`.

## Reproducibility Notes

- The notebooks expect both CSV files to remain in the repository root.
- Generated charts are mostly displayed inline rather than saved to a structured output directory.
- Some notebook outputs are verbose because the original project preserved intermediate displays for class submission purposes.

## Recommended Next Improvements

- Encode categorical predictors properly for predictive modeling
- Add holdout metrics such as RMSE, MAE, precision, recall, F1, and confusion matrices directly in the notebook narrative
- Separate exploratory analysis from predictive modeling into cleaner notebook sections
- Move reusable preprocessing into Python modules for easier reruns and testing

## Authors

Original project contributors:

- Rafin Ahon
- Rashik Alahi
- Gunnar Austin
- Connor Curtis
- Emily Evans
