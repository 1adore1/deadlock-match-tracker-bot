# Deadlock Match Tracker Bot

![Example](https://github.com/1adore1/deadlock-match-tracker-bot/raw/main/assets/img.jpg)

### Overview
A Telegram bot for tracking real-time Deadlock matches for top 250 players of the leaderboad. The bot fetches match data using the Deadlock API and predicts the likely match winner using a machine learning model.

### Features:
- Real-time tracking of Deadlock matches for top 250 players of the leaderboard.
- Predicts match winners using LightGBM.
- Achieves ROC-AUC at 71% in predicting match outcomes.
- Displays match details such as net worth, heroes, and match score.
- Allows users to refresh match details dynamically with a button click.

## Installation

**Requirements**:
- Python 3.10 or higher
- Required Python packages listed in `requirements.txt`

### Setup:
1. Clone the repository:
   ```
   git clone https://github.com/1adore1/deadlock-matches
   cd deadlock-matches
   ```
2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
3. Configure the bot token:
     Add your bot's API token in `config.py`:
     ```
     API_TOKEN = "your_bot_token_here"
     ```
4. Run the bot:
   ```
   python tg_bot.py
   ```

## Data Collecting:
**Deadlock API**
- Historical data (67k matches) was fetched from `https://analytics.deadlock-api.com/`.
- Total 250k rows match data, that were scrapped at different time.
- Information about each new match is fetched from `https://data.deadlock-api.com/`.

## Bot Commands

### `/start`
- Displays the bot's welcome message and shows a button to enter a Steam profile.

### `/check`
- Prompts the user to enter Steam profile URL to check active matches.

## How to Use

1. Start the bot with `/start`.
2. Use the `Check account (Top 250)` button or `/check` command to check for active games by entering a Steam account.
3. If a match is found, the bot will display detailed match data.
4. Use the `Refresh Match Info` button to update match details dynamically.

## Code Structure

- **`tg_bot.py`**: Main script for running the bot.
- **`tools.py`**: Contains utility functions for fetching and processing Steam and match data.
- **`config.py`**: Holds bot configuration, such as the API token of telegram bot.
- **`models/model.joblib`**: Pretrained lgb model for match predictions.
