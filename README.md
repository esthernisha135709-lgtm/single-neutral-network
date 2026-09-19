# single-neutral-network
Climate Energy Consumption Prediction 🌍⚡
This project builds a Feedforward Neural Network (FNN) using TensorFlow/Keras to predict energy consumption based on climate and temporal features. It demonstrates data preprocessing, feature engineering, model training, evaluation, and performance visualization.

📂 Dataset
File: climate_energy.csv

Contains:

timestamp (date & time)

location (categorical)

climate features (temperature, humidity, etc.)

energy_consumption (target variable)

🔧 Steps in the Workflow
1. Import Libraries
pandas, numpy, scikit-learn

tensorflow/keras

matplotlib

2. Load Dataset
python
df = pd.read_csv("/content/climate_energy.csv")
print(df.head())
3. Feature Engineering
Convert timestamp → numerical features (hour, day, month)

Encode categorical location using LabelEncoder

Drop original timestamp

4. Data Preprocessing
Split into features (X) and target (y)

Normalize features with StandardScaler

Train-test split (80/20)

5. Model Architecture
Input layer: Dense(16, relu)

Hidden layer: Dense(8, relu)

Output layer: Dense(1)

6. Compile & Train
Optimizer: Adam

Loss: Mean Squared Error

Metric: Mean Absolute Error

Train for 100 epochs, batch size 16

7. Evaluation
Test Loss & MAE

Predictions on test set

Performance metrics:

Mean Squared Error (MSE)

Root Mean Squared Error (RMSE)

Mean Absolute Error (MAE)

R² Score

📊 Example Output
text
Test Loss : 0.0123
Test MAE  : 0.089
Mean Squared Error: 0.0123
Root Mean Squared Error: 0.111
Mean Absolute Error: 0.089
R2 Score: 0.92
🚀 How to Run
Clone the repo:

bash
git clone https://github.com/yourusername/climate-energy-prediction.git
cd climate-energy-prediction
Install dependencies:

bash
pip install -r requirements.txt
Run the notebook or script:

bash
python energy_model.py
📌 Requirements
Python 3.8+

pandas, numpy, scikit-learn

tensorflow, keras

matplotlib

📈 Future Improvements
Add more climate features (wind speed, rainfall, etc.)

Try advanced models (LSTM, GRU for time series)

Hyperparameter tuning

Deploy as a web app with Flask/Streamlit
