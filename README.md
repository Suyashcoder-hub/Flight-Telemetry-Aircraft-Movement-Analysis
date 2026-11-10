# Flight Telemetry & Aircraft Movement Analysis

## About the Project

This project is focused on analyzing aircraft surveillance data to understand aircraft movement and flight behaviour using Python.

I started this project to explore how real-world flight data can be processed, cleaned and analyzed to extract useful information. The dataset contains details such as aircraft location, altitude, speed, vertical rate, flight status and aircraft identifiers.

The main objective is to understand the data, identify quality issues, perform exploratory analysis and discover patterns related to aircraft movement.

## Objectives

- Understand the structure and characteristics of aircraft surveillance data.
- Identify missing values, duplicates and inconsistent records.
- Clean and validate flight-related measurements.
- Analyze aircraft speed, altitude and vertical movement.
- Study the geographical distribution of aircraft.
- Classify aircraft based on their flight phase.
- Apply basic data filtering and smoothing techniques.
- Extract meaningful insights through data visualization.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- Jupyter Notebook

## Dataset Overview

The project uses an OpenSky-style aircraft surveillance dataset containing approximately 7,500 records and 16 columns.

Some of the important attributes include:

| Column | Description |
|---|---|
| icao24 | Unique aircraft identifier |
| callsign | Aircraft callsign |
| origin_country | Country associated with the aircraft |
| latitude | Aircraft latitude |
| longitude | Aircraft longitude |
| baro_altitude | Barometric altitude |
| geo_altitude | Geometric altitude |
| velocity | Aircraft speed in m/s |
| vertical_rate | Rate of climb or descent |
| on_ground | Ground or airborne status |
| true_track | Aircraft direction |

## Project Workflow

### 1. Data Understanding

Started by loading the dataset into Pandas and examining its structure, dimensions, data types and statistical summary. Also checked missing values and duplicate records to understand the overall quality of the data.

### 2. Data Cleaning and Preprocessing

Worked on preparing the raw dataset for analysis by handling duplicate records, standardizing values, converting timestamps and checking the validity of geographical coordinates and flight measurements.

### 3. Feature Engineering

Created additional features to make the data easier to interpret, including:

- Speed conversion from m/s to km/h.
- Altitude conversion from metres to feet.
- Vertical rate conversion from m/s to feet per minute.
- Flight-phase classification based on ground status and vertical rate.

### 4. Exploratory Data Analysis

Explored different aspects of aircraft movement through statistical analysis and visualizations.

The analysis includes:

- Airborne and ground aircraft distribution.
- Country-wise aircraft distribution.
- Aircraft speed and altitude patterns.
- Climbing and descending behaviour.
- Geographical distribution of aircraft positions.

### 5. Data Filtering and Movement Analysis

Explored basic filtering techniques to identify invalid measurements and improve data consistency. Also experimented with moving-average smoothing for sequential aircraft observations and calculated geographical distances between consecutive positions.

## Initial Observations

During the initial examination of the dataset, I found:

- Approximately 7,561 aircraft records.
- 93 distinct origin countries.
- 6,864 airborne records and 697 ground records.
- A considerable number of missing values in the squawk column.
- Some missing altitude and vertical-rate measurements.

These observations helped identify the areas that needed further investigation during data cleaning and analysis.

## Project Structure

```text
Flight_Telemetry_Analytics/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   └── Flight_Telemetry_Analysis.ipynb
│
├── reports/
│
├── README.md
└── requirements.txt
```

## How to Run

Clone the repository:

```bash
git clone YOUR_REPOSITORY_URL
```

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn plotly
```

Open Jupyter Notebook:

```bash
jupyter notebook
```

Open the analysis notebook and run the cells sequentially.

Make sure the dataset is placed inside the `data/raw/` directory.

## Limitations

The dataset contains aircraft state-vector information rather than raw radar signals or direct GPS/IMU sensor readings.

The available observations are also limited, with only a small number of aircraft having repeated records. This limits the scope of continuous trajectory tracking and meaningful filtering validation.

## Future Scope

I would like to extend this project by working with larger historical flight datasets, studying continuous aircraft trajectories, exploring Kalman filtering and analyzing actual GPS and IMU sensor data.

## Author

**Suyash Dwivedi**

B.Tech CSE – Artificial Intelligence and Data Science

Interested in Data Analytics, Python and real-world applications of data science.
