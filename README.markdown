# Fetal Health Prediction Project

Welcome to the Fetal Health Prediction Project. This web-based application leverages machine learning to predict fetal health status (Normal, Suspect, or Pathological) based on fetal heart rate parameters. this project offers a user-friendly interface with an orange theme and robust predictive capabilities.

## Project Overview

This project uses a Flask backend, HTML/CSS/JavaScript frontend with Tailwind CSS, and Scikit-learn for three machine learning models: Logistic Regression, K-Nearest Neighbors (KNN), and Random Forest. The application processes data from the `fetal_health.csv` dataset to provide accurate health predictions.

## Features

- **Model Selection**: Choose from Logistic Regression, KNN, or Random Forest.
- **Interactive UI**: Orange-themed interface with a two-column layout, tooltips, and dynamic loading.
- **Additional Endpoint**: `/health` route for system status.
- **Prediction Output**: Displays health status with a placeholder for confidence score.

## Project Structure

```
fetal-health/
├── app.py              # Flask application with prediction logic
├── requirements.txt    # Python dependencies
├── fetal_health.csv    # Dataset for training (not included, see below)
└── templates/
    ├── index.html      # Main page with orange two-column design
    └── output.html     # Prediction result template
├── Project Initiation and Planning Phase/
    └── project_initiation_and_planning.tex
├── Data Collection and Preprocessing Phase/
    └── data_collection_and_preprocessing.tex
├── Model Development Phase/
    └── model_development.tex
├── Model Optimization Phase/
    └── model_optimization.tex
├── Project Execution Files/
    └── project_execution_files.tex
```

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/hriturajnarvekar27/FetalAl.git
   cd fetal-health
   ```

2. **Install Dependencies**:
   Ensure Python 3.10+ is installed, then run:
   ```bash
   pip install -r requirements.txt
   ```

3. **Obtain the Dataset**:
   The `fetal_health.csv` file is not included due to size or sensitivity. Download it from [your source] and place it in the project root.

4. **Run the Application**:
   ```bash
   python app.py
   ```
   Open your browser at `http://127.0.0.1:5000/`.

## Usage

- Select a model from the dropdown on the homepage.
- Input fetal heart rate parameters in the provided fields.
- Click "Predict Health Status" to see the result.
- Use "Reset" to clear inputs or visit `/health` for system status.

## Documentation

This project includes detailed LaTeX documents for each development phase:
- **Project Initiation and Planning Phase**: Outlines objectives and planning.
- **Data Collection and Preprocessing Phase**: Details data sourcing and cleaning.
- **Model Development Phase**: Describes model implementation.
- **Model Optimization Phase**: Covers model tuning and improvement.
- **Project Execution Files**: Provides deployment and testing instructions.

Compile each `.tex` file using `latexmk -pdf` (e.g., `latexmk -pdf project_initiation_and_planning.tex`) to generate PDF reports.

## Technologies Used

- **Backend**: Flask, Python, Scikit-learn
- **Frontend**: HTML, Tailwind CSS, JavaScript
- **Design**: Poppins font, Font Awesome icons
- **Documentation**: LaTeX

## Contributing

Contributions are welcome! Fork the repository, make changes, and submit a pull request. Suggestions for UI enhancements or model improvements are encouraged.

This project is licensed under the MIT License. See the `LICENSE` file for details (create one if needed).

## Contact

For inquiries, contact Sakshi Patil at sakshi.patil@example.com.
