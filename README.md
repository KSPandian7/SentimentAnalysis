# Sentiment Analysis Web Application

This project is a Sentiment Analysis web application built using Flask. The application allows users to upload CSV files containing text data or input text manually to predict the sentiment of the content (positive or negative). The prediction results can be downloaded in CSV format, and the sentiment distribution is visualized through a pie chart.

## Table of Contents
• Project Overview<br>
• Features<br>
• Setup Instructions<br>
• How to Use<br>
• File Structure<br>
• Key Components<br>
• Model and Preprocessing<br>
• Acknowledgments<br>

## Project Overview
This Sentiment Analysis project classifies textual data as either positive or negative using a machine learning model. The application processes input data (individual text or bulk CSV files) and provides predictions. It employs natural language processing (NLP) techniques for text preprocessing and machine learning for sentiment prediction.

### The project utilizes:

• Flask for building the web interface and handling user requests.<br>
• NLTK and scikit-learn for text processing and sentiment classification.<br>
• matplotlib for visualizing sentiment distribution.<br>

### Features

• Single Text Prediction: Input a single text string to predict its sentiment.<br>
• Bulk CSV Prediction: Upload a CSV file containing sentences, and the application will return a downloadable CSV file with sentiment predictions.<br>
• Sentiment Visualization: Visualize the sentiment distribution of text data with a pie chart.<br>
• Error Handling: Displays meaningful error messages for invalid inputs.<br>

### Setup Instructions

#### Prerequisites

Ensure you have the following installed on your machine:

• Python 3.7+<br>
• Flask<br>
• Pandas<br>
• Matplotlib<br>
• Scikit-learn<br>
• NLTK<br>
• XGBoost (or another pre-trained sentiment analysis model)<br>
• Jupyter Notebook (if running the .ipynb file)<br>

### Installation

#### Clone this repository to your local machine:
```bash
git clone <repository-url>
```

#### Navigate to the project directory:
```bash
cd sentiment-analysis-web-app
```

#### Install the required dependencies:
```bash
pip install -r requirements.txt
```

#### Download NLTK stopwords:
```bash
import nltk
nltk.download('stopwords')
```

Place your trained model files (model_xgb.pkl, scaler.pkl, countVectorizer.pkl) in the Models/ directory.

#### Run the Flask application:
```bash
python app.py
```

Open your browser and navigate to bash http://127.0.0.1:5000/ to access the web interface.

### How to Use
#### Single Text Prediction
• Enter text directly into the input field on the homepage.
• Click the Predict button to see the sentiment (positive/negative) for the text.
• The prediction will be displayed on the right side of the screen.

#### Bulk CSV Prediction
• Upload a CSV file with a column named Sentence that contains the text data.
• The application will process the file and provide the sentiment predictions as a downloadable CSV file.
• Additionally, a pie chart will be displayed to show the sentiment distribution.

#### Output
• Single Prediction: Displays the sentiment for the input text.
• Bulk Prediction: A CSV file is generated and made available for download.
• Visualization: A pie chart showing the sentiment distribution of the uploaded CSV file.

#### File Structure
```bash
sentiment-analysis-web-app/
│
├── app.py                   # Main Flask application file
├── templates/
│   └── index.html            # HTML template for the front-end interface
├── Models/
│   ├── model_xgb.pkl         # Pre-trained sentiment analysis model
│   ├── scaler.pkl            # Scaler for data normalization
│   └── countVectorizer.pkl   # CountVectorizer for text vectorization
├── static/
│   └── style.css             # (Optional) Static files like CSS or JavaScript
├── main.ipynb                # Jupyter notebook for sentiment analysis
├── requirements.txt          # Required dependencies
└── README.md                 # Project documentation
```
Flask for web development.
NLTK for natural language processing.
Scikit-learn for machine learning preprocessing.
XGBoost for the classification model.
