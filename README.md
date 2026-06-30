# NYC Taxi Trip Duration — Data Mining Project

A full data mining pipeline on the NYC Taxi Trip Duration dataset: data exploration, outlier removal, feature engineering (trip distance via haversine, time-based features), optional weather data integration, and modeling.

## Data

CSV files are **not included** in this repo (large Kaggle datasets). To run the notebook, download the following and place them in the project root (or update the paths in the notebook):

- `train.csv` — from the [Kaggle NYC Taxi Trip Duration competition](https://www.kaggle.com/c/nyc-taxi-trip-duration/data)
- `weather.csv` — NYC weather data for the same date range (temperature, precipitation, snowfall), merged in the optional weather-integration section

The notebook also produces intermediate files (`train2.csv`, `train2_with_weather.csv`) during preprocessing — these are also gitignored and regenerated when you run the relevant cells.

## Setup

```bash
pip install -r requirements.txt
jupyter notebook nyc_taxi_analysis.ipynb
```

## Pipeline overview

1. Data loading & exploration
2. Preprocessing & feature engineering (outlier removal, haversine distance, lat/long bounding box filtering)
3. Optional weather data integration
4. Time-based feature extraction (hour, day of week, etc.)
5. Modeling & evaluation
