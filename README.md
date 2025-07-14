# 🏠 India House Price Prediction

A machine learning web application built with Streamlit that predicts house prices in India based on various property features.

## 🌐 Live Demo
**Try the app online:** [https://india-house-price-predictor.streamlit.app](https://india-house-price-predictor.streamlit.app)

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Model Information](#model-information)
- [File Structure](#file-structure)
- [Screenshots](#screenshots)
- [Contributing](#contributing)

## 🎯 Overview

This project uses a Linear Regression model to predict house prices based on key property features such as:
- Number of bedrooms
- Number of bathrooms
- Living area (square feet)
- Number of nearby schools
- Distance from the airport

The application provides an intuitive web interface where users can input property details and get instant price predictions.

## ✨ Features

- **Interactive Web Interface**: Easy-to-use Streamlit web application
- **Data Upload**: Support for custom CSV datasets or use default dataset
- **Real-time Predictions**: Instant house price predictions based on input features
- **Data Visualization**: View dataset statistics and feature ranges
- **Input Validation**: Smart validation to prevent unrealistic predictions
- **Responsive Design**: Clean, modern UI with organized layout
- **Error Handling**: Comprehensive error handling for negative predictions

## 📊 Dataset

The project uses the `IndiaHousePrice.csv` dataset containing 14,621 house records with the following features:

| Feature | Description | Range |
|---------|-------------|-------|
| Number of bedrooms | Count of bedrooms in the house | 1-10 |
| Number of bathrooms | Count of bathrooms in the house | 1-10 |
| Living area sqft | Living area in square feet | 500-10,000 |
| Number of schools nearby | Count of schools in vicinity | 0-10 |
| Distance from the airport | Distance in kilometers | 1-200 |
| Price | House price in Indian Rupees (INR) | Target variable |

## 🚀 Installation

### Prerequisites
- Python 3.7 or higher
- pip package manager

### Step 1: Clone or Download
Download the project files to your local machine.

### Step 2: Install Dependencies
```bash
pip install -r requirements.txt
```

The required packages are:
- `pandas` - Data manipulation and analysis
- `scikit-learn` - Machine learning library
- `streamlit` - Web application framework

### Step 3: Run the Application

**Option 1: Using the batch file (Windows)**
```bash
run_app.bat
```

**Option 2: Using command line**
```bash
streamlit run IndiaHousePrice.py
```

**Option 3: Using Python directly**
```bash
python -m streamlit run IndiaHousePrice.py
```

## 💻 Usage

1. **Start the Application**: Run the application using one of the methods above
2. **Access the Web Interface**: Open your browser and go to `http://localhost:8501`
3. **Upload Data (Optional)**: Upload your own CSV file or use the default dataset
4. **View Dataset**: Explore the dataset preview and statistics
5. **Make Predictions**: 
   - Enter property features in the input fields
   - Click "Predict Price" to get the estimated house price
   - View the prediction with appropriate validation messages

### Input Guidelines
- **Bedrooms**: 1-10 (realistic range)
- **Bathrooms**: 1-10 (realistic range)
- **Living Area**: 500-10,000 sqft (minimum 500 sqft recommended)
- **Schools Nearby**: 0-10 schools
- **Airport Distance**: 1-200 km

## 🤖 Model Information

### Algorithm
- **Model Type**: Linear Regression
- **Training Split**: 80% training, 20% testing
- **Random State**: 2529 (for reproducible results)

### Performance Metrics
- **Mean Squared Error (MSE)**: Displayed in the application
- **Prediction Range**: ₹100,000 - ₹2,000,000+ (typical range)

### Model Features
- **Feature Scaling**: Not applied (Linear Regression can handle the current feature scales)
- **Feature Selection**: Uses all 5 available features
- **Validation**: Includes negative prediction detection and handling

## 📁 File Structure

```
ybi project-2/
├── IndiaHousePrice.py      # Main Streamlit application
├── IndiaHousePrice.csv     # Dataset file
├── requirements.txt        # Python dependencies
├── run_app.bat            # Windows batch file for easy startup
└── README.md              # Project documentation
```

## 🖼️ Screenshots

The application includes:
- **File Upload Section**: Drag and drop CSV files
- **Dataset Preview**: First 5 rows of the dataset
- **Statistics Panel**: Expandable section with feature ranges
- **Prediction Interface**: Two-column layout for input fields
- **Results Display**: Color-coded prediction results with validation

## 🔧 Troubleshooting

### Common Issues

1. **Negative Price Predictions**
   - **Cause**: Input values outside training data range
   - **Solution**: Use realistic values within suggested ranges

2. **File Not Found Error**
   - **Cause**: `IndiaHousePrice.csv` not in project folder
   - **Solution**: Ensure CSV file is in the same directory as the Python script

3. **Module Import Errors**
   - **Cause**: Missing dependencies
   - **Solution**: Run `pip install -r requirements.txt`

### Tips for Best Results
- Use property features within the statistical ranges shown in the app
- Ensure living area is at least 500 sqft
- Keep distance from airport reasonable (1-200 km)
- Use integer values for bedrooms, bathrooms, and schools

## 🤝 Contributing

Contributions are welcome! Here are some ways you can improve the project:

1. **Model Improvements**:
   - Try different algorithms (Random Forest, XGBoost, etc.)
   - Add feature engineering
   - Implement cross-validation

2. **UI/UX Enhancements**:
   - Add data visualization charts
   - Implement model comparison
   - Add prediction confidence intervals

3. **Data Enhancements**:
   - Include more features (location, house age, etc.)
   - Add data preprocessing
   - Implement outlier detection

## 📄 License

This project is open source and available under the MIT License.

## 👤 Author

**Nikhil Negi**
- Skills learned through YBI Foundation 45-Days Internship Program

## 🙏 Acknowledgments

- YBI Foundation for the live skill learning classes
- Streamlit team for the amazing web framework
- Scikit-learn contributors for the machine learning tools

---

**Happy House Price Predicting! 🏡**
