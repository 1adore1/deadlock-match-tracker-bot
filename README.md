# Deadlock Match Tracker Bot

## Description
Deadlock Match Tracker Bot is a Telegram bot designed to track and analyze matches in the game Deadlock for top 250 players of the leaderboard. It collects match data, processes it, and provides insights using a trained machine learning model.

## Features
- Fetch and store match data
- Process and clean match results
- Train a machine learning model for match predictions
- Provide match analysis via a Telegram bot

## Machine Learning Model
- Used **LightGBM** for match prediction
- Achieved **ROC AUC = 0.71**
- Used **Optuna** for hyperparameter tuning

## Project Structure
```
deadlock-match-tracker-bot/
│── 📂 assets/               # Media files
│   │── img.jpg             # Example image
│── 📂 data/                 # Datasets used in the project
│   │── clean_data.csv       # Processed match data
│   │── match_results.csv    # Raw match results
│── 📂 models/               # Trained machine learning models
│   │── model.joblib         # Serialized model file
│── 📂 notebooks/            # Jupyter notebooks for data processing and model training
│   │── fetch_data.ipynb     # Notebook for data collection
│   │── process_data.ipynb   # Notebook for data preprocessing
│   │── train_data.ipynb     # Notebook for model training
│── 📂 src/                  # Source code of the project
│   │── tg_bot.py            # Telegram bot implementation
│   │── tools.py             # Utility functions
│── requirements.txt         # List of dependencies
```

## Installation
1. Clone the repository:
   ```
   git clone https://github.com/1adore1/deadlock-match-tracker-bot.git
   ```
2. Navigate to the project directory:
   ```
   cd deadlock-match-tracker-bot
   ```
3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

## Usage
1. Run the Telegram bot:
   ```
   python src/tg_bot.py
   ```
2. Interact with the bot via Telegram to get match analytics and predictions.
