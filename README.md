# **Disaster Detection and Alert System**

This project implements a machine learning-based system for detecting natural disasters in real-time using satellite imagery and social media data. The system leverages Convolutional Neural Networks (CNNs) for image classification and Natural Language Processing (NLP) techniques for social media analysis. The model is deployed using a Flask API for real-time disaster alerts.

## **Project Overview**

This system is designed to:
- **Classify satellite images** to detect disasters such as wildfires, floods, and storms.
- **Analyze social media data** to detect disaster-related posts and provide timely alerts.
- **Serve predictions through an API** for easy integration into disaster response systems.

## **Table of Contents**

1. [Project Overview](#project-overview)
2. [Project Structure](#project-structure)
3. [Data](#data)
4. [Model Training](#model-training)
5. [API Setup](#api-setup)
6. [Requirements](#requirements)
7. [Usage](#usage)
8. [Contributing](#contributing)
9. [License](#license)

## **Project Structure**

disaster-detection-ml/ 
│ 
├── data/ # Datasets (raw and processed) 
│ ├── raw/ # Raw data (images, social media) 
│ └── processed/ # Cleaned and preprocessed data 
│ 
├── notebooks/ # Jupyter notebooks for experimentation 
│ └── disaster_detection.ipynb 
│ 
├── src/ # Source code (data processing, model, etc.) 
│ ├── data_preprocessing.py # Script to clean and preprocess data 
│ ├── model_training.py # Script to train models (CNN, NLP) 
│ └── inference.py # Script to run predictions 
│ 
├── models/ # Trained models 
│ └── disaster_model.h5 # Example CNN model 
│ 
├── api/ # Flask API for serving predictions 
│ ├── app.py # Flask application code 
│ └── requirements.txt # Dependencies for API 
│ 
├── tests/ # Unit tests for the project 
│ └── test_model.py # Example test case 
│ 
├── README.md # Project documentation 
├── requirements.txt # List of dependencies 
├── .gitignore # Files to ignore in version control 
└── LICENSE # License file (optional)

## **Data**

### Satellite Imagery
- **Source**: [Kaggle](https://www.kaggle.com/competitions/datasets)
- **Data Types**: Labeled images of disaster and non-disaster events.

### Social Media Data
- **Source**: Twitter API and [Tweepy](https://www.tweepy.org/)
- **Data Types**: Text posts with hashtags and geolocation data related to disasters.

## **Model Training**

### **Image Classification with CNN**
1. The CNN model is trained using satellite images labeled for disaster types such as floods, wildfires, and hurricanes.
2. The dataset is preprocessed (resized, normalized) before being fed into the CNN.

### **NLP for Social Media Data**
1. Text data from social media is cleaned using tokenization, stopword removal, and lemmatization.
2. The text is classified using a Naive Bayes classifier based on keywords and sentiment analysis.

## **API Setup**

The project includes a Flask API for serving real-time predictions from the trained models.

1. **Flask Setup**: The API allows users to send image or text data and receive disaster predictions in response.
2. To run the API locally, follow these steps:

```bash
# Navigate to the api directory
cd api

# Install required packages
pip install -r requirements.txt

# Start the Flask server
python app.py


