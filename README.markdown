# FetalAI: Using Machine Learning to Predict and Monitor Fetal Health

## Overview
This project uses machine learning to predict fetal health (normal, suspect, or pathological) based on a dataset of fetal health metrics. It includes data preparation, exploratory data analysis (EDA), model training, hyperparameter tuning, and deployment via a Flask web app.

## Project Structure
- `data/fetal_health.csv`: Dataset (place it in the `data` folder).
- `train_model.py`: Script for data preparation, EDA, training, and saving the model.
- `app.py`: Flask app for model deployment.
- `requirements.txt`: List of required Python packages.
- `README.md`: This file.

## Setup Instructions
1. **Clone the Repository or Create the Directory Structure**
   - Create a `FetalAI` directory.
   - Create a `data` subfolder and place `fetal_health.csv` inside it.

2. **Install Dependencies**
   - Run the following command in the `FetalAI` directory:
     ```
     pip install -r requirements.txt
     ```

3. **Train the Model**
   - Run the training script:
     ```
     python train_model.py
     ```
   - This will perform EDA, train models, tune the best one (XGBoost), and save the model (`fetalai_model.pkl`) and scaler (`scaler.pkl`).
   - EDA plots will be saved as PNG files in the project directory.

4. **Run the Flask App**
   - Start the Flask app:
     ```
     python app.py
     ```
   - The app will be available at `http://127.0.0.1:5000`.

5. **Test the App**
   - Use a tool like Postman or a Python script to send a POST request to `http://127.0.0.1:5000/predict`.
   - Example Python script (`test.py`):
     ```python
     import requests

     sample_input = {
         "baseline value": 120.0,
         "accelerations": 0.0,
         "fetal_movement": 0.0,
         "uterine_contractions": 0.0,
         "light_decelerations": 0.0,
         "severe_decelerations": 0.0,
         "prolongued_decelerations": 0.0,
         "abnormal_short_term_variability": 73.0,
         "mean_value_of_short_term_variability": 0.5,
         "percentage_of_time_with_abnormal_long_term_variability": 43.0,
         "mean_value_of_long_term_variability": 2.4,
         "histogram_width": 64.0,
         "histogram_min": 62.0,
         "histogram_max": 126.0,
         "histogram_number_of_peaks": 2.0,
         "histogram_number_of_zeroes": 0.0,
         "histogram_mode": 120.0,
         "histogram_mean": 137.0,
         "histogram_median": 121.0,
         "histogram_variance": 73.0,
         "histogram_tendency": 1.0
     }

     response = requests.post('http://127.0.0.1:5000/predict', json=sample_input)
     print(response.json())
     ```
   - Expected output: `{'fetal_health': 2}` (suspect).

## Notes
- Ensure `fetal_health.csv` is in the `data` folder before running `train_model.py`.
- The project was set up on June 10, 2025, at 12:08 PM IST.
- If you encounter issues, ensure all dependencies are installed and the dataset matches the expected format (21 features + `fetal_health` target).