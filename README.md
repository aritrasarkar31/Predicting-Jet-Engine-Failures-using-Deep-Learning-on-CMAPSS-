Predictive Maintenance on Jet Engines (CMAPSS)
This project uses the NASA CMAPSS FD001 dataset to predict the Remaining Useful Life (RUL) of turbofan engines using an LSTM deep learning model.

🚀 Objective
Predict when an engine will fail so that maintenance can be scheduled proactively. This reduces downtime, increases safety, and saves operational costs.

📊 Dataset
Source: NASA CMAPSS (FD001)

Each row represents one time-step for an engine.

Features include:

Operational settings

21 sensor readings

Engine ID and cycle

🧠 Model Overview
Model: LSTM Regressor

Input: Sequence of 30 time steps of sensor data

Output: Predicted Remaining Useful Life (RUL)

Loss Function: Mean Squared Error (MSE)

Evaluation Metric: Root Mean Squared Error (RMSE)

🔧 Features
Sequence windowing for LSTM

Sensor filtering (remove low-variance signals)

Training & validation loop

RUL prediction

Alert system based on a defined RUL threshold

📈 Results
Engine ID	Predicted RUL	Actual RUL	Maintenance Alert
1	18.2	20	YES
2	60.1	65	NO

⚠️ Alert Logic
Any engine with Predicted RUL < 20 cycles is flagged for maintenance.

📂 File Structure
notebooks/turbofancmapss.ipynb: Full implementation

data/: Place raw FD001.txt dataset here

models/: Optional folder to store trained models
