# Aviation Accident Analysis

## Overview
This project analyzes aviation accident data to investigate factors associated with passenger injuries and aircraft destruction. The analysis focuses on comparing small and large aircraft across different manufacturers, aircraft types, weather conditions, and engine types.

The goal of the project is to identify patterns related to aircraft safety and determine which factors are associated with lower fatal/serious injury rates.

---

## Dataset
The dataset used in this project is the NTSB Aviation Accident Database (`AviationData.csv`).

The dataset contains information including:
- Aircraft make and model
- Aircraft category
- Engine type
- Number of engines
- Weather conditions
- Flight phase
- Passenger injuries
- Aircraft damage severity

---

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Data Cleaning
The following preprocessing steps were performed:
- Removed rows with invalid passenger counts
- Filled missing injury values with 0
- Filtered groups with fewer than 10 accident records
- Created injury fraction metrics:

```python
Injury Fraction =
(Fatal Injuries + Serious Injuries)
/
Number of Passengers
```

- Created aircraft destruction indicators based on the `Aircraft.damage` column

---

## Analysis Performed

### 1. Aircraft Make Analysis
- Compared small vs large aircraft manufacturers
- Calculated mean fatal/serious injury fractions
- Identified the safest manufacturers based on injury outcomes
- Evaluated aircraft destruction rates

### 2. Plane Type Analysis
- Compared injury distributions across aircraft types
- Used violin plots and strip plots to visualize injury distributions

### 3. Weather Condition Analysis
- Compared accident severity under:
  - VMC (Visual Meteorological Conditions)
  - IMC (Instrument Meteorological Conditions)
  - UNK (Unknown)
- Evaluated both injury rates and aircraft destruction rates

### 4. Engine Type Analysis
- Investigated how engine type affects:
  - Passenger injury severity
  - Aircraft destruction probability

---

## Key Findings
- Large aircraft generally showed lower injury fractions and tighter injury distributions.
- Poor weather conditions (IMC) were associated with higher injury severity and aircraft destruction rates.
- Certain aircraft makes consistently showed lower injury fractions and lower destruction rates.
- Some engine types displayed higher variability and more severe accident outcomes.

---

## Visualizations
The project includes:
- Horizontal bar plots
- Violin plots
- Strip plots

These visualizations were used to compare injury severity and destruction rates across different aviation factors.

---

## How to Run
1. Clone/download the repository
2. Install required libraries:

```bash
pip install pandas matplotlib seaborn numpy
```

3. Open the Jupyter Notebook:

```bash
jupyter notebook
```

4. Run all cells in order

---

## Future Improvements
Possible extensions for future work:
- Add predictive modeling
- Analyze flight phase impacts
- Investigate geographic trends
- Include time-series accident trends
- Build interactive dashboards
