# FIFA World Cup 2026 Prediction Model

## Overview

This project is a comprehensive simulation and prediction framework for the FIFA World Cup 2026. It is designed as a major engineering project in Python using Jupyter Notebooks. The model combines historical FIFA World Cup data with machine learning to predict match outcomes, simulate the tournament, and visualize predictions in charts suitable for academic or research purposes.

In the current simulation run, Senegal emerged as the predicted 2026 FIFA World Cup champion. This demonstrates the stochastic nature of football and the inherent unpredictability of the tournament when using probabilistic models.

## Project Structure

```
fifa_wc_prediction/
│
├── data/
│   ├── raw/                              # Raw FIFA World Cup historical match data (txt files)
│   └── processed/                        # Cleaned and feature-engineered CSV datasets
│       └── fifa_wc_features_enhanced.csv
│
├── notebooks/
│   ├── 01_data_parsing.ipynb             # Parsing historical FIFA match txt files
│   ├── 02_feature_engineering.ipynb      # Create features for ML model
│   ├── 03_model_training.ipynb           # Train Random Forest & evaluate predictive accuracy
│   ├── 04_initial_simulation.ipynb       # Initial predictions for sample matches
│   ├── 05_visualization.ipynb            # Generate charts and visualizations of match outcomes
│   └── 06_full_2026_simulation.ipynb     # Full tournament simulation & predicted champion
│
├── charts/                               # Auto-generated charts for match predictions & tournament
├── README.md                             # Project documentation
└── requirements.txt                      # Python dependencies
```

## Features

### 1. Historical Data Parsing

- Parses FIFA World Cup match results from 1930–2022 from raw .txt files
- Extracts match date, teams, scores, goal scorers, and other relevant metadata
- Combines all historical matches into a single master dataset for analysis

### 2. Feature Engineering

Generates numerical features for machine learning models:

- Team strength (historical performance)
- Recent form (last few matches)
- Head-to-head statistics
- Host advantage
- Stage of the tournament

Produces a clean CSV dataset ready for modeling.

### 3. Machine Learning Model

- Random Forest Classifier trained on historical match outcomes
- Target variable: match outcome (Home Win, Draw, Away Win)
- Accuracy approximately 46%, reflecting the inherent unpredictability of World Cup matches

### 4. Prediction & Simulation

Predicts individual match outcomes and associated probabilities. Simulates the entire 2026 FIFA World Cup tournament:

- Group stage
- Round of 16
- Quarterfinals
- Semifinals
- Final

Current simulation predicts Senegal as the champion, highlighting the stochastic nature of football prediction.

### 5. Visualization

- Pie charts for each match showing probability distribution of outcomes
- Bar chart showing probabilities across all group stage matches
- Knockout stage winner distribution chart
- All charts automatically saved in the `charts/` folder for research or reporting

## Installation

### Prerequisites

- Python 3.8 or higher
- Jupyter Notebook or JupyterLab

### Setup

1. Clone the repository:
```bash
git clone <repository-url>
cd fifa_wc_prediction
```

2. Install required dependencies:
```bash
pip install -r requirements.txt
```

3. Launch Jupyter Notebook:
```bash
jupyter notebook
```


## Model Performance

The Random Forest model achieves approximately 46% accuracy on historical World Cup matches. This relatively modest accuracy reflects several important factors:

- The inherent unpredictability of football matches
- The limited sample size of World Cup matches (held every 4 years)
- The impact of unpredictable factors such as injuries, weather, and referee decisions
- The tournament format, where a single match can eliminate strong teams

Despite these limitations, the model provides valuable probabilistic predictions that capture the competitive nature of the World Cup.

## Data Sources

Historical FIFA World Cup match data spanning from 1930 to 2022, including:

- Match results and scores
- Goal scorers and timing
- Tournament stages
- Host nations
- Team participation history

## Key Dependencies

- pandas - Data manipulation and analysis
- numpy - Numerical computing
- scikit-learn - Machine learning algorithms
- matplotlib - Data visualization
- seaborn - Statistical data visualization
- jupyter - Interactive computing environment
---

**Note:** This is a probabilistic model for research and educational purposes. Actual tournament outcomes will depend on numerous factors not captured in historical data. The prediction of Senegal as champion in the current simulation demonstrates the model's ability to identify competitive underdogs based on historical patterns, but should not be interpreted as a definitive forecast.
