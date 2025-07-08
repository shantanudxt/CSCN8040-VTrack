# CSCN8040-VTrack Project

## Group Members
- Shantanu Dixit - 8965610
- Serageldin Monir Farid Abdelghaffar Abdelmoaty - 9052380
- Tai Siang Huang - 9006413
- Jaiminiben Natvarbhai Rathod - 8941937
- Mohammed Adeen Shaik - 8969152

## Project Overview
This repository contains the exploratory data analysis (EDA) and statistical evaluation for the V-Track project, focusing on optimizing traffic stop durations using AI-assisted tools, such as a proposed RAG-based system.

## Dataset
- **Source**: [Washington DC Stop Data](https://catalog.data.gov/dataset/stop-data-b6fdf)
- **Description**: Contains stop data from the Metropolitan Police Department (MPD) in Washington, D.C., covering vehicle, pedestrian, bicycle, and harbor stops from January 1, 2023, to June 30, 2024. Includes details like stop location, reason, duration, and outcomes (e.g., tickets, searches, arrests).

## Notebook
- View the detailed EDA: [V-Track EDA_Final.ipynb](https://github.com/shantanudxt/CSCN8040-VTrack/blob/main/notebooks/V-Track%20EDA_Final.ipynb)

## EDA Summary
- **Population**: Traffic stops recorded in Washington, D.C., anonymized case-by-case.
- **Independent Variables**: `STOP_TYPE`, `STOP_DISTRICT`, `DATETIME`, `STOP_LOCATION_BLOCK`
- **Dependent Variable**: `STOP_DURATION` (minutes)
- **Current Mean Duration**: ~8.9 minutes
- **Ideal Target**: < 10 minutes

### Key Insights
- Most stops are completed within 5–20 minutes.
- Ticket-only stops have lower durations.
- Weekdays, especially working hours, see more stops.
- `STOP_TYPE` and `STOP_DISTRICT` are key indicators of duration variation.
- `STOP_DURATION` exhibits a right-skewed distribution.

## Data Cleaning and Preprocessing
- Filtered data for `STOP_REASON_TICKET` containing "Observed moving violation".
- Standardized column names (e.g., `STOP_DURATION_MINS` to `STOP_DURATION`).
- Converted `DATETIME` to datetime object and extracted `HOUR` and `DAY_OF_WEEK`.
- Removed negative or zero `STOP_DURATION` values and those exceeding 24 hours (1440 minutes).
- Filled missing `STOP_DISTRICT` values with the median (3.0).
- Performed one-hot encoding for `TICKETS_ISSUED` and `WARNINGS_ISSUED`.

## Statistical Analysis
### Hypotheses
- **Null Hypothesis (H₀):** The selected columns has no significant effect on traffic stop duration.
- **Alternative Hypothesis (H₁):** The selected columns significantly effect on the average traffic stop processing time.

### Normality Test
- **Shapiro-Wilk Test**: Statistic = 0.3358, p-value = 0.0000
  - Data is not normally distributed; non-parametric tests are appropriate.

### Kruskal-Wallis Test Results
- **STOP_DISTRICT**: Statistic = 463.0993, p-value = 0.0000 → Significant effect.
- **TICKET_ Columns**: 77 significant effects (e.g., `TICKET_T637`, `TICKET_T639`), 63 non-significant.
- **WARNING_ Columns**: 33 significant effects (e.g., `WARNING_T184`, `WARNING_T200`), 148 non-significant.

### Evaluation
- Rejected H₀: `STOP_DISTRICT`, certain `TICKETS_ISSUED`, and `WARNINGS_ISSUED` columns significantly affect `STOP_DURATION`.

## Visualization
- Histograms and boxplots of `STOP_DURATION` by `STOP_TYPE` and `STOP_DISTRICT`.
- Countplot of stops by `DAY_OF_WEEK`.

## Next Steps
- Develop and test the RAG-based system to optimize traffic stop durations.
- Further analyze significant ticket and warning types for targeted improvements.
- Validate findings with additional data or real-time testing.

## Dependencies
- `pandas`
- `numpy`
- `seaborn`
- `matplotlib`
- `scipy`

Install dependencies in a virtual environment:

```bash
python -m venv venv
source ./venv/bin/activate  # For Windows, use: .\venv\Scripts\activate
pip install -r config/requirements.txt
