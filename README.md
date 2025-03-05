# NBA Player Salary and Points Predictions

## Author: Sammi Beard

## Overview
This project aims to predict NBA player salaries and points scored based on player statistics from the 2022 season. The dataset was sourced from Kaggle and includes various performance metrics such as field goal percentage, assists, steals, and rebounds. The goal is to assist team owners and coaches in making data-driven decisions regarding player acquisitions and salary negotiations.

## Dataset
The data was obtained from multiple Kaggle datasets:
- **NBA Player Salaries (2022-2025)**
- **NBA Player Stats (1950-2022)**

After cleaning and processing, the dataset includes attributes such as:
- Position, Age, Team
- Games Played, Games Started
- FG%, 3P%, 2P%, Free Throw%
- Offensive & Total Rebounds, Assists, Steals, Blocks, Turnovers, Personal Fouls
- Points and Salary (Target Variables)

## Data Cleaning & Preprocessing
- Dropped columns with little to no data.
- Renamed columns for better readability.
- Removed features with high correlation (>90%) to reduce redundancy.
- Filtered data to only include 2022 statistics to match salary information.
- Handled missing values by filling in median values for percentage-based statistics.
- Created dummy variables for categorical data (Position, Team).

## Exploratory Data Analysis (EDA)
Several visualizations were created to explore relationships between different player attributes and the target variables (Salary, Points). Key findings include:
- A weak correlation between Salary and Points.
- No significant correlation between Salary and FG%.
- Stronger trends when comparing Points to metrics like Games Played, Age, and Rebounds.

## Model Development
The dataset was split into training and testing sets, and multiple models were tested:

### Models Tested:
1. **Decision Tree Regressor**
   - Salary R²: 0.295
   - Points R²: 0.773
2. **Random Forest Regressor**
   - Salary R²: 0.705
   - Points R²: 0.918
3. **Multi-Output Regressor (Random Forest with Poisson Criterion)**
   - Salary R²: 0.716
   - Points R²: 0.945

The best-performing model was the **Multi-Output Regressor** using a Random Forest with Poisson criterion, showing high predictability for points and moderate predictability for salary.

## Key Insights
- Player salaries are harder to predict than points scored.
- The model can provide a ballpark salary estimate based on past performance but should be supplemented with additional factors such as injuries and team synergy.
- Further analysis on player chemistry and team dynamics could improve predictions for real-world applications.

## Future Work
- Incorporate injury history and collegiate statistics to improve rookie salary predictions.
- Analyze team synergy to assess how players perform in different lineups.
- Include demographic data (height, weight, nationality) to explore potential performance trends.
- Develop a dashboard for interactive analysis and visualization of player performance and salary trends.

## References
- Kaggle datasets: [NBA Player Salaries](https://www.kaggle.com/datasets/omarsobhy14/nba-players-salaries), [NBA Player Stats](https://www.kaggle.com/datasets/loganlauton/nba-players-and-team-data)
- Multi-Target Regression Model Guide: [Medium Article](https://medium.com/@tubelwj/developing-multi-class-regression-models-with-python-c8beca5dd482)

## Contact
For any questions or collaboration opportunities, please reach out to **Sammi Beard**.
