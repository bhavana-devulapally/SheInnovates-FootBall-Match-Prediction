# SheInnovates-FootBall-Match-Prediction
This project was developed for the SheInnovates Hackathon and uses a Random Forest machine learning model to predict the outcomes of English Premier League (EPL) matches based on historical data. The end-to-end pipeline includes data scraping, cleaning, feature engineering, model training, evaluation, and improvement. This project was develped as a part of the "She Innovates" Hackathon.

### She Innovates EPL Match Predictor

This project was developed for the She Innovates hackathon and uses a Random Forest machine learning model to predict the outcomes of English Premier League (EPL) matches based on historical data.

## Project Overview
The objective of this project was to predict match outcomes by building a machine learning model trained on multi-season EPL data. The project pipeline follows these major steps:

1. **Data Collection (Web Scraping)**:
Before model building, I implemented a web scraping pipeline using Python, leveraging the requests library to make HTTP calls and BeautifulSoup to parse the HTML pages of EPL match data across seasons. I extracted relevant match details such as date, teams, venue, and results, and structured the raw HTML into a pandas DataFrame. This automated pipeline ensured access to up-to-date and comprehensive match history from various online sources.

2. **Data Preparation**:
    - The dataset used is `matches.csv`, containing over a thousand rows, each representing an EPL match.
    - Missing data was investigated and cleaned to ensure completeness for two seasons.

3. **Data Cleaning**:
    - Conversion of non-numeric data to numeric formats.
    - Handling missing values and converting date columns to the correct datetime format.

4. **Feature Engineering**:
    - Creation of new predictors such as `venue_code`, `opp_code`, `hour`, and `day_code`.
    - Conversion of categorical data to numerical codes.

5. **Model Training**:
    - The Random Forest classifier was chosen for its ability to handle non-linear relationships.
    - Data was split into training and test sets, ensuring chronological order to simulate real-world predictions.

6. **Model Evaluation**:
    - Initial evaluation showed the model predicted losses more accurately than wins.
    - Visualization of actual vs. predicted values was performed.

7. **Improving Model Precision**:
    - Rolling averages of team performance over the last three matches were computed and added as predictors.
    - The model was retrained using these new predictors, resulting in improved precision.

8. **Performance Enhancement** : 
   - Introduced rolling performance metrics as additional features.
   - Retrained the model with enhanced feature set, leading to improved precision and generalization.


## Key Technologies Used
 - Languages/Libraries: Python, pandas, NumPy, scikit-learn, BeautifulSoup, requests
 - ML Techniques: Random Forest, feature engineering, rolling averages, model evaluation
 - Data Engineering: Web scraping, data wrangling, categorical encoding


## Installation

To get started with this project, clone the repository by the commad given below:
```bash
git clone https://github.com/yourusername/SheInnovates-FootBall-Match-Prediction.git

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





