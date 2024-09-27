
# 🔥 Fire-Weather-Index (FWI) Prediction 

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/) [![Flask](https://img.shields.io/badge/Flask-%20v1.1.2-lightgrey.svg)](https://flask.palletsprojects.com/) ![AWS Elastic Beanstalk](https://img.shields.io/badge/Deployed_on-AWS_Elastic_Beanstalk-orange.svg) ![License](https://img.shields.io/badge/License-MIT-green.svg)

## 🚀 Introduction
The **Fire-Weather-Index (FWI) Prediction** project is an AI-powered solution designed to predict the risk of forest fires by calculating the Fire Weather Index (FWI). It leverages various meteorological factors like temperature, humidity, wind speed, and rain to offer real-time, data-driven predictions. 🔥

This project is deployed on **AWS Elastic Beanstalk** with a CI/CD pipeline using **AWS CodePipeline** for continuous integration. The machine learning model is served through a **Flask** web application, allowing users to input data and instantly get a prediction.

---

## 📦 Installation

### Prerequisites
Make sure you have the following installed:
- [Python 3.x](https://www.python.org/)
- [Flask](https://flask.palletsprojects.com/)
- [AWS CLI](https://aws.amazon.com/cli/) (for deployment)
  
### Steps to Set Up Locally

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/FWI-Prediction.git
   cd FWI-Prediction
   ```

2. **Install Required Libraries**
   Install the necessary Python libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. **Download or Train the Model**
   Ensure you have the pre-trained model files in the `/models` directory. If not, you can train your own by following the [Model Training](#model-training) section.

4. **Run the Application**
   Start the Flask web app:
   ```bash
   python app.py
   ```
   Open `http://localhost:5000` in your browser to access the application.

---

## 🛠️ Features

- **ML-Driven Predictions**: Utilizes a Ridge Regression model for accurate Fire Weather Index prediction.
- **Interactive Web Interface**: Easy-to-use UI where users can input weather data and receive instant predictions.
- **API Endpoint**: Programmatically access FWI predictions through a REST API.
- **Cloud Deployment**: Fully deployed on AWS Elastic Beanstalk with auto-deployment via AWS CodePipeline.

---

## 📊 Data Overview

The dataset used in this project is the **Algerian Forest Fires Dataset**, which includes meteorological information essential for calculating fire risks.

- **Key Features**:
  - 🌡️ **Temperature** (°C)
  - 💧 **Humidity** (%)
  - 🌬️ **Wind Speed** (km/h)
  - ☔ **Rainfall** (mm)
  - 🔥 **Fire Risk Classes** (binary: 0 = no fire, 1 = fire)

### Data Preprocessing
- **Dropping** unnecessary columns like day, month, and year.
- **Encoding** categorical data such as fire risk.
- **Feature Scaling**: Using `StandardScaler` to normalize the input features for better model performance.

---

## 💻 Methodology

1. **Data Cleaning**: Irrelevant columns removed and missing data handled.
2. **Feature Engineering**: Created and selected key features like FFMC, DMC, and ISI.
3. **Model Selection**:
   - Ridge Regression (final model)
   - Other models evaluated: Lasso, ElasticNet, Linear Regression
4. **Evaluation Metrics**:
   - **Mean Absolute Error (MAE)**
   - **R² Score**

**Key Libraries**:
- **scikit-learn**: Machine learning model
- **Flask**: Web framework
- **AWS Elastic Beanstalk**: Hosting platform

---

## 🎯 Usage

### Web Interface
1. Navigate to `http://fire-weather-index-fwi-predictio-env-2.eba-h2redfrz.eu-north-1.elasticbeanstalk.com/` in your browser.
2. Input the weather parameters in the form (e.g., Temperature, Wind Speed).
3. Hit **Predict** to get the Fire Weather Index (FWI).

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
