# Stock Price Prediction using Deep Learning (LSTM)

This project aims to forecast the closing price of Tesla (TSLA) stock using historical data. A Long Short-Term Memory (LSTM) neural network, a type of recurrent neural network (RNN) well-suited for time-series data, is built and trained for this purpose.

## Project Objective

The goal is to develop a robust predictive model that can learn the complex patterns in historical stock prices and provide an accurate forecast for future prices. This project demonstrates skills in data cleaning, preprocessing, time-series analysis, and deep learning model implementation.

## Tech Stack

- **Language:** Python 3
- **Libraries:**
  - **Pandas:** For data loading, manipulation, and cleaning.
  - **Scikit-learn:** For data scaling (`MinMaxScaler`).
  - **TensorFlow & Keras:** For building and training the LSTM neural network.
  - **Matplotlib:** For data visualization.
  - **Jupyter Notebook:** For interactive development and code execution.

## Methodology

1.  **Data Loading and Cleaning:** The `TSLA_stock_data.csv` dataset is loaded. The date column is parsed correctly, and the 'Close' price column is sanitized to ensure it's a numeric type, handling any potential errors or missing values.
2.  **Data Preprocessing:** The 'Close' prices are scaled to a range between 0 and 1 using `MinMaxScaler`. This normalization step is crucial for the efficient training of neural networks.
3.  **Time-Series Sequencing:** The data is transformed into sequences. For this model, a sequence of 60 previous days' closing prices is used to predict the closing price of the 61st day.
4.  **Model Architecture:** A sequential LSTM model is constructed with two LSTM layers, Dropout layers to prevent overfitting, and Dense layers to produce the final output.
5.  **Training and Evaluation:** The model is trained on 80% of the historical data and then evaluated on the remaining 20%. The performance is measured using the Root Mean Squared Error (RMSE) metric.

## Results

The model demonstrates excellent performance on the test dataset, tracking the actual stock price with high accuracy.

-   **Root Mean Squared Error (RMSE):** 5.09
-   **Visual Representation:** The plot below shows a very close fit between the model's predictions and the actual stock prices.

*(Optional: Add the screenshot of your result plot here. You can do this by uploading the image to your repo and using the following markdown: `![Model Prediction Result](path/to/your/image.png)`)*

![Model Prediction Result](Screenshot%202025-05-30%20at%2011.54.07%E2%80%AFAM.png)


## How to Run

1.  Clone the repository:
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    ```
2.  Install the required dependencies:
    ```bash
    pip install pandas numpy scikit-learn tensorflow matplotlib jupyterlab
    ```
3.  Navigate to the project directory and launch Jupyter:
    ```bash
    jupyter lab
    ```
4.  Open and run the `.ipynb` notebook file to see the complete workflow and results.

## Disclaimer

This project is for educational purposes only and should not be considered financial advice. Stock market prediction is inherently complex and volatile.
