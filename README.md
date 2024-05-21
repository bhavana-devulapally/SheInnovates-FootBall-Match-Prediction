# SheInnovates-FootBall-Match-Prediction
This project uses a Random Forest algorithm to predict football match outcomes based on historical data. It includes data preprocessing, feature engineering, model training, and evaluation. Part of the "She Innovates" initiative to promote women's involvement in tech and sports analytics.

### She Innovates EPL Match Predictor

This project was developed for the She Innovates hackathon and uses a Random Forest machine learning model to predict the outcomes of English Premier League (EPL) matches based on historical data.

## Project Overview

The project involves the following steps:

1. **Data Preparation**:
    - The dataset used is `matches.csv`, containing over a thousand rows, each representing an EPL match.
    - Missing data was investigated and cleaned to ensure completeness for two seasons.

2. **Data Cleaning**:
    - Conversion of non-numeric data to numeric formats.
    - Handling missing values and converting date columns to the correct datetime format.

3. **Feature Engineering**:
    - Creation of new predictors such as `venue_code`, `opp_code`, `hour`, and `day_code`.
    - Conversion of categorical data to numerical codes.

4. **Model Training**:
    - The Random Forest classifier was chosen for its ability to handle non-linear relationships.
    - Data was split into training and test sets, ensuring chronological order to simulate real-world predictions.

5. **Model Evaluation**:
    - Initial evaluation showed the model predicted losses more accurately than wins.
    - Visualization of actual vs. predicted values was performed.

6. **Improving Model Precision**:
    - Rolling averages of team performance over the last three matches were computed and added as predictors.
    - The model was retrained using these new predictors, resulting in improved precision.

## Installation

To get started with this project, clone the repository and install the necessary dependencies:
```bash
git clone https://github.com/yourusername/she-innovates-epl-predictor.git
cd she-innovates-epl-predictor
pip install -r requirements.txt
```

## Usage

After installing the dependencies, you can run the main script to train the model and make predictions:
```bash
python main.py
```

## Key Components

- **Data Preprocessing**: Handling missing data and converting data types.
- **Feature Engineering**: Creating new features to improve model accuracy.
- **Model Training and Evaluation**: Training the Random Forest model and evaluating its performance.
- **Improvement with Rolling Averages**: Enhancing model precision with rolling averages of past performance.





