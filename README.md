# Crime-Detection-using-Big-Data-Analysis

A comprehensive web application for crime analysis and prediction using machine learning.

## Overview

The Crime Detection System is a full-stack application designed to help law enforcement agencies and security professionals analyze crime patterns and predict potential criminal activities. The system uses machine learning algorithms to process crime data and provides visual representations of crime statistics and predictions.

## Features

- **Crime Prediction**: Predict potential criminal activities based on various factors such as time, location, and demographics.
- **Crime Heatmap**: Visualize crime hotspots and spatial distributions on an interactive map.
- **Statistical Analysis**: View and analyze crime trends and statistics with interactive charts.
- **User-friendly Interface**: Intuitive and responsive web interface for easy navigation and interaction.

## Technology Stack

### Frontend
- React.js
- Material-UI
- React Router
- Leaflet (for maps)
- Recharts (for data visualization)

### Backend
- Python Flask
- Flask-CORS
- Pandas for data processing
- Scikit-learn for machine learning
- **Dask & Dask-ML for scalable/big data processing and distributed ML**

## Project Structure

```
crime_detection_system/
├── backend/                # Flask backend
│   ├── app.py              # Main application file
│   ├── spark_processing.py # (Replaced by dask-based processing)
│   ├── predict_with_spark.py # (Replaced by dask-based prediction)
│   └── requirements.txt    # Python dependencies
├── data/                   # Crime datasets
│   └── crime_data.csv      # Generated crime data
├── frontend/               # React frontend
│   ├── public/             # Static files
│   └── src/                # React components and pages
│       ├── components/     # Reusable UI components
│       ├── pages/          # Application pages
│       ├── services/       # API services
│       └── utils/          # Utility functions
└── models/                 # Trained ML models
    └── dask_crime_model.pkl # Serialized Dask-ML model
```

## Setup and Installation

### Prerequisites
- Node.js and npm
- Python 3.7+
- pip

### Backend Setup
1. Navigate to the backend directory:
   ```
   cd crime_detection_system/backend
   ```

2. Create a virtual environment (recommended):
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

4. Start the backend server:
   ```
   python app.py
   ```
   The server will run on http://localhost:5000

### Frontend Setup
1. Navigate to the frontend directory:
   ```
   cd crime_detection_system/frontend
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Start the development server:
   ```
   npm start
   ```
   The frontend will be available at http://localhost:3000

## Usage

1. Open your browser and navigate to http://localhost:3000
2. Use the navigation sidebar to access different features:
   - Dashboard: Overview of the system and quick access to features
   - Prediction: Make crime predictions based on input parameters
   - Heatmap: View crime distribution on an interactive map
   - Statistics: Analyze crime trends and patterns
   - About: Information about the system and its features

## Machine Learning Model

The system uses a Random Forest Classifier (from Dask-ML) to predict crime types based on various features:
- Time of day
- Day of week
- Month
- Geographic location (latitude, longitude)
- Population density
- Proximity to police stations
- Historical crime rates

For demonstration purposes, the system generates synthetic crime data if no dataset is provided.

## Big Data Processing

- **Dask & Dask-ML** are used for scalable data processing and distributed machine learning, enabling the system to handle large datasets efficiently.

## License

This project is licensed under the MIT License.

## Acknowledgments

- This project is for educational and demonstration purposes only.
- The crime data used in this application is synthetic and does not represent actual crime statistics.
