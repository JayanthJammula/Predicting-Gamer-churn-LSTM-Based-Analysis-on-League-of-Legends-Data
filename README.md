# League of Legends Player Churn Prediction 🚀

This project builds a pipeline to predict player churn in Riot Games' *League of Legends* using match data collected through the Riot API. The pipeline includes data retrieval, cleaning, feature extraction, and predictive modeling with deep learning.

---

## 📁 Project Structure

```text
.
├── Riot_API_Data_Retrieving.py       # Retrieves match data using the Riot API
├── clean.py                          # Cleans and formats raw match data
├── feature_extraction.py            # Extracts player-level features from match data
├── model.py                         # Performs EDA, statistical analysis, and trains LSTM model
├── player_features_manual_x.csv     # Final processed dataset for modeling
├── requirements.txt                 # Python dependencies
└── README.md                        # Project instructions and overview

```

## Workflow

1. **Riot API Data Collection**  
   Run `Riot_API_Data_Retrieving.py` to fetch match data starting from a seed PUUID.  
   This script:
   - Crawls matches from a seed player.
   - Gathers metadata for each match and participant.
   - Saves the result as `.json` and `.csv`.

2. **Data Cleaning**  
   Run `clean.py` to:
   - Convert timestamps to human-readable format.
   - Save the cleaned data as `updated_participants_with_match_data.csv`.

3. **Feature Extraction**  
   Run `feature_extraction.py` to:
   - Derive churn labels and player-level features.
   - Output a clean CSV: `player_features_manual_x.csv`.

4. **Modeling & Analysis**  
   Run `model.py` to:
   - Perform exploratory data analysis (EDA) and statistical analysis.
   - Train and evaluate a Bidirectional LSTM model for churn prediction.
   - Report performance metrics with confidence intervals.

---

## Installation

Ensure you have Python 3.8+ installed. Then install the required dependencies:
pandas, numpy

1. matplotlib, seaborn

2. scikit-learn

3. tensorflow

4. requests


