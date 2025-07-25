# Sector-wise-Stock-Market-Prediction

This project implements a machine learning system to forecast sector-based stock trends using historical data. It allows users to select a specific stock from various sectors, view its historical performance, analyze moving averages, and predict future prices using a RandomForestRegressor model.

## Features

* **Sector & Stock Selection:** Interactive command-line interface to choose from predefined sectors (Technology, Healthcare, Financial, Energy, Consumer Discretionary) and individual stocks within them.
* **Historical Data Download:** Fetches 5 years of historical stock data using the `yfinance` library.
* **Price Visualization:** Plots adjusted closing prices over time for selected stocks.
* **Technical Analysis:** Calculates and displays 20-day, 50-day, and 200-day Simple Moving Averages (SMA) for trend analysis.
* **Machine Learning Prediction:**
    * Utilizes a **RandomForestRegressor** for predicting future stock prices.
    * **Feature Engineering:** Incorporates moving averages (7-day, 21-day) and lagged prices as input features.
    * **Data Preprocessing:** Applies `StandardScaler` for feature scaling to normalize the input data.
    * **Train-Test Split:** Splits data into training and testing sets while preserving time series order (`shuffle=False`).
    * **Performance Metrics:** Evaluates the model using Mean Squared Error (MSE) and R-squared (R2) score.
    * **Prediction Visualization:** Plots actual versus predicted prices to visually assess model performance.

## Technologies Used

* **Python:** Programming language
* **Pandas:** Data manipulation and analysis
* **NumPy:** Numerical operations
* **Matplotlib:** Data visualization
* **yfinance:** Library for downloading financial market data from Yahoo! Finance
* **Scikit-learn (sklearn):** Machine learning library (for `RandomForestRegressor`, `train_test_split`, `mean_squared_error`, `r2_score`, `StandardScaler`)

## Project Structure

The project consists of a single Python script (`stock_prediction.py` or similar) that encapsulates all functionalities:


## How to Run

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/YourGitHubUsername/Sector-wise-Stock-Market-Prediction.git](https://github.com/YourGitHubUsername/Sector-wise-Stock-Market-Prediction.git)
    cd Sector-wise-Stock-Market-Prediction
    ```
2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: `venv\Scripts\activate`
    ```
3.  **Install dependencies:**
    ```bash
    pip install pandas matplotlib yfinance scikit-learn
    ```
4.  **Run the script:**
    ```bash
    python stock_prediction.py
    ```
    The script will then prompt you to select a sector and a stock, and choose an action (plot, analyze, predict).

