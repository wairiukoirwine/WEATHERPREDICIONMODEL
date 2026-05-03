# WEATHERPREDICIONMODEL
 Weather Rain Prediction — ML Project
A beginner machine learning project that predicts whether it will rain based on daily weather measurements from Seattle.

 Project Summary
ItemDetailsAlgorithmLogistic RegressionDatasetSeattle Weather (seattle-weather.csv)Records1,461 daysFeatures4 (precipitation, temp_max, temp_min, wind)TargetRain: Yes (1) or No (0)Accuracy~85%ToolsPython, pandas, scikit-learn, matplotlib, seaborn

 Project Files
weather-ml-project/
│
├── weather_ml_project.py       # Main Python script
├── seattle-weather.csv         # Dataset
├── README.md                   # This file
│
├── fig1_distributions.png      # Feature distribution charts
├── fig2_heatmap.png            # Correlation heatmap
├── fig3_confusion_matrix.png   # Confusion matrix
└── fig4_feature_importance.png # Feature importance chart

 Dataset
Source: Kaggle — Seattle Weather
Columns:
ColumnDescriptiondateDate of observationprecipitationRainfall in mmtemp_maxMaximum temperature (°C)temp_minMinimum temperature (°C)windWind speed (km/h)weatherWeather type (rain, sun, fog, drizzle, snow)
The weather column is converted into a binary target — 1 = Rain, 0 = Everything else.

 How to Run
Option 1 — Google Colab (Recommended)

Open colab.research.google.com
Create a new notebook
Upload seattle-weather.csv using the file upload cell
Paste and run each cell from weather_ml_project.py in order

Option 2 — VS Code / Local

Make sure Python is installed
Install dependencies:

bashpip install pandas scikit-learn matplotlib seaborn

Place seattle-weather.csv in the same folder as the script
Run:

bashpython weather_ml_project.py

⚙️ How the Model Works

Load the CSV file into a pandas DataFrame
Clean the data — convert weather labels to binary (Rain / No Rain)
Split data — 80% for training, 20% for testing
Scale features using StandardScaler so all variables are on the same scale
Train Logistic Regression on the training set
Predict on the test set
Evaluate using accuracy, confusion matrix, and classification report


 Results

Accuracy: ~85%
Strongest predictor: Precipitation
Model correctly classified roughly 85 out of every 100 test days


Possible Improvements

Use a larger dataset (e.g. Rain in Australia — 145,000 records)
Try Random Forest or XGBoost for higher accuracy
Add more features: humidity, pressure, cloud cover
Apply k-fold cross-validation for a more reliable accuracy estimate


 Limitations

Dataset is specific to Seattle — may not generalize to other climates
Only 4 features used — real weather systems are more complex
Logistic Regression assumes a linear decision boundary


Libraries Used

pandas — data loading and manipulation
scikit-learn — model training and evaluation
matplotlib — charts and visualizations
seaborn — correlation heatmap


👤 Author
DAI022 — Machine Learning Fundamentals Final Project
