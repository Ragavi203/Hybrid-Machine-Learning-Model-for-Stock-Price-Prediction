# Hybrid Machine Learning Model for Stock Price Prediction

This project uses a hybrid approach combining Long Short-Term Memory (LSTM) networks and Linear Regression to predict future stock prices. The hybrid model leverages the strengths of both techniques to enhance prediction accuracy.

## Project Overview
- **Objective:** Predict future stock prices using a combination of LSTM and Linear Regression models.
- **Technologies:** Python, TensorFlow, Scikit-learn, Pandas, NumPy, Matplotlib
- **Models Used:** LSTM (for capturing sequential dependencies) and Linear Regression (for leveraging linear relationships).

## Dataset
The project uses a CSV file containing historical stock prices of Apple Inc. (`apple_stock_data.csv`). The data includes columns such as `Date`, `Close`, `Open`, `High`, `Low`, and `Volume`.

## Key Steps

### 1. Data Preprocessing
- Convert the `Date` column to datetime format and set it as the index.
- Normalize the `Close` price using `MinMaxScaler` to scale the data between 0 and 1.
- Create sequences of 60 days for the LSTM model.

### 2. Model Training
- **LSTM Model:**
  - Two LSTM layers with 50 units each.
  - One Dense output layer.
  - Trained with a mean squared error loss function and the Adam optimizer.

- **Linear Regression Model:**
  - Created using lagged features (`Lag_1`, `Lag_2`, `Lag_3`) to capture short-term dependencies.

### 3. Prediction and Future Forecasting
- Predict future prices using both models.
- Combine predictions with a weighted average to form hybrid predictions.

### 4. Visualization
- Plot the predicted prices from both models and the hybrid model for comparison.

## How to Use

### Prerequisites
- Python 3.x
- TensorFlow
- Scikit-learn
- Pandas
- NumPy
- Matplotlib

### Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/hybrid-stock-price-prediction.git
   ```
2. Navigate to the project directory:
   ```bash
   cd hybrid-stock-price-prediction
   ```
3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

### Running the Project
1. Ensure the dataset (`apple_stock_data.csv`) is in the project directory.
2. Run the main script:
   ```bash
   python main.py
   ```
3. The script will output future predictions and display plots comparing the predictions from the LSTM, Linear Regression, and Hybrid models.

## Results
The project generates a DataFrame containing future dates, and predictions from the LSTM model, Linear Regression model, and the Hybrid model. These predictions are visualized for easy comparison.

## Future Work
- Experiment with different sequence lengths for the LSTM model.
- Use additional features (like `Open`, `High`, `Low`, `Volume`) to improve prediction accuracy.
- Optimize the weights used in the hybrid model.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or suggestions.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.






https://colab.research.google.com/drive/175r0dqki1khrRr99fL-5eHGVdae6n2uC?usp=sharing
