# Cryptocurrency Price Prediction Using Machine Learning

This project focuses on predicting the closing prices of the BTC/USDT cryptocurrency pair using machine learning techniques. It involves data preprocessing, feature extraction, model training, and visualization of the results. Additionally, it includes pattern recognition in candlestick charts to provide more insightful predictions.

## Table of Contents

- [Project Overview](#project-overview)
- [Data Description](#data-description)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Model Training](#model-training)
- [Prediction and Evaluation](#prediction-and-evaluation)
- [Visualization](#visualization)
- [How to Run](#how-to-run)
- [Dataset Links](#dataset-links)
- [Contributors](#contributors)
- [License](#license)

## Project Overview

The goal of this project is to predict the next closing price of the BTC/USDT pair on Binance using historical minute-by-minute data. The project also identifies specific candlestick patterns like Hammer, Doji, and Engulfing patterns to generate buy/sell signals, making the prediction model more robust.

## Data Description

The project uses minute-level data from the Binance BTC/USDT trading pair. The datasets include the following features:
- `date`: The timestamp of the data.
- `open`: Opening price of the minute.
- `high`: Highest price of the minute.
- `low`: Lowest price of the minute.
- `close`: Closing price of the minute.
- `Volume BTC`: Volume in BTC traded during the minute.
- `Volume USDT`: Volume in USDT traded during the minute.
- `tradecount`: Number of trades executed during the minute.

## Exploratory Data Analysis (EDA)

Before model training, an extensive EDA is conducted to understand the data better. Key steps include:
- **Data Cleaning:** Conversion of date strings to datetime objects and handling missing data.
- **Statistical Summary:** Summary statistics of the numerical columns.
- **Visualization:** Distribution plots of the closing prices, volumes, and a correlation heatmap of the key features.

### Sample Visualizations:
![image](https://github.com/user-attachments/assets/d5a8194b-2867-49a8-ad7e-8dbc36f832bf)

## Model Training

The model used for price prediction is a **Random Forest Regressor**. The features include:
- OHLCV data: `open`, `high`, `low`, `close`, `Volume BTC`, `Volume USDT`.
- Candlestick patterns: `hammer`, `doji`, `shooting_star`, `bullish_engulfing`, `bearish_engulfing`.
- Trend indicator: A column indicating the trend of the market.

### Hyperparameter Tuning:
Cross-validation is performed with a parameter grid to fine-tune the model's performance.

## Prediction and Evaluation

After training the model, predictions are made on the test set. The model's performance is evaluated using metrics like **Mean Squared Error (MSE)**, **Root Mean Squared Error (RMSE)**, **Mean Absolute Error (MAE)**, and **R-Squared (R2)**.

### Sample Prediction Visualizations:

1. **Scatter Plot of Actual vs. Predicted Prices**
   ![image](https://github.com/user-attachments/assets/1856925f-7212-4cc3-b2c0-ba2361469313)


2. **Line Plot of Actual and Predicted Prices**
   ![image](https://github.com/user-attachments/assets/a2492598-2eb8-4f6a-aa36-b60b6c6d80aa)

## Visualization

To provide more context to the predictions, the project includes visualizations of candlestick charts with annotated patterns and predictions:
- **Candlestick Chart with Predicted Close Prices**: Shows the actual and predicted close prices on the candlestick chart.
- **Candlestick Chart with Pattern Annotations**: Visualizes specific patterns like Hammer, Doji, etc., and their corresponding buy/sell signals.

### Sample Chart Visualizations:

1. **Candlestick Chart with Predicted Prices**
   ![image](https://github.com/user-attachments/assets/9528f812-6274-406d-8128-8232dc216049)

2. **Candlestick Chart with Patterns**
   ![image](https://github.com/user-attachments/assets/b5969963-41d9-4559-8636-09f42144265c)

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your_username/crypto-price-prediction.git
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter notebook or Python script for EDA, model training, and evaluation.

## Dataset Links

The datasets used in this project can be downloaded from the following links:
- [Binance BTC/USDT Minute Data](https://drive.google.com/file/d/1zk9lE8-ibklI0IbGLesbYeOJNZ_Jqxl-/view?usp=sharing)
- [Additional Data](https://drive.google.com/file/d/1LuRqfPRPdOkO0ljqKuwc01D8tag2ng_B/view?usp=sharing)

## Contributors

- [Your Name](https://github.com/your_username)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Replace the placeholder paths for images with the actual paths to your visualizations once they are uploaded to the repository.
