# 🏠 House Price Prediction & Recommendation System

A Machine Learning-powered web application that predicts house prices and recommends suitable properties based on user preferences. The system combines Random Forest Regression, Cosine Similarity, Constraint-Based Filtering, Affordability Analysis, and Accessibility Scoring to provide personalized property recommendations.

---

## Features

### House Price Prediction
- Predicts house prices using Random Forest Regression
- Generates estimated property value based on user inputs
- Provides price range for better decision-making

### Smart Property Recommendation
- Recommends properties matching user preferences
- Uses Cosine Similarity for content-based matching
- Applies constraint-based filtering using:
  - City
  - Budget
  - BHK
  - Area

### Hybrid Ranking System
Properties are ranked using:
- Similarity Score
- Affordability Score
- Accessibility Score
- Exact BHK Match Bonus

### Interactive Web Interface
- Built with Flask
- Responsive UI
- Property details popup
- Sorting and filtering options

---

## Technologies Used

### Backend
- Python
- Flask

### Machine Learning
- Scikit-learn
- Random Forest Regression
- Cosine Similarity

### Data Processing
- Pandas
- NumPy

### Frontend
- HTML
- CSS
- JavaScript

### Model Storage
- Joblib

---

## Project Structure

```text
House-Price-Prediction-Recommendation-System/
│
├── app/
│   ├── routes.py
│   ├── prediction.py
│   ├── recommendation.py
│   ├── utils.py
│   └── __init__.py
│
├── data/
│   └── combined_final_dataset.csv
│
├── models/
│   ├── random_forest_model.pkl
│   ├── scaler.pkl
│   └── features.pkl
│
├── templates/
│   ├── index.html
│   ├── results.html
│   └── base.html
│
├── static/
│   ├── style.css
│   └── script.js
│
├── notebook/
│   └── model_training.ipynb
│
├── run.py
├── requirements.txt
└── README.md
```

---

## How It Works

### Step 1: User Input
User enters:
- City
- BHK
- Bathrooms
- Balconies
- Area
- Property Age
- Amenities
- Budget

### Step 2: Price Prediction
The trained Random Forest model predicts the expected house price.

### Step 3: Property Filtering
Properties are filtered using:
- City
- Area Range
- BHK Range
- Budget

### Step 4: Similarity Calculation
Cosine Similarity compares user preferences with property features.

### Step 5: Hybrid Scoring
Final recommendation score is calculated using:
- Similarity
- Affordability
- Accessibility

### Step 6: Recommendation Output
Top-ranked properties are displayed to the user.

---

## Installation

### Clone Repository

```bash
git clone https://github.com/SamyakkSingh/Smart-Home-Finder
```

### Navigate to Project Folder

```bash
cd House-Price-Prediction-Recommendation-System
```

### Create Virtual Environment

```bash
python -m venv venv
```

### Activate Virtual Environment

Windows:

```bash
venv\Scripts\activate
```

Linux/Mac:

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run Application

```bash
python run.py
```

---

## Machine Learning Model

### Model Used
**Random Forest Regression**

### Why Random Forest?
- Handles non-linear relationships
- High prediction accuracy
- Reduces overfitting
- Works well with multiple features

### Input Features
- BHK
- Bathrooms
- Balconies
- Carpet Area
- Amenities Count
- Property Age
- Latitude
- Longitude
- Accessibility Score

---

## Recommendation Logic

```text
User Input
     ↓
Constraint-Based Filtering
     ↓
Cosine Similarity
     ↓
Affordability Calculation
     ↓
Accessibility Calculation
     ↓
Hybrid Score Generation
     ↓
Top Property Recommendations
```

---

## Future Enhancements

- Real-time property data integration
- Property comparison feature
- Map-based property search
- Deep Learning models
- Mobile application support

