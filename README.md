# 📈 Stock Price Prediction: Linear Regression vs Random Forest

This project compares the performance of **Linear Regression** and **Random Forest Regression** for predicting stock prices based on historical data. The trained Random Forest model is deployed on **Google Cloud Run**, and an API endpoint is available for real-time predictions.

---

## 🚀 Project Features

- 📊 Data Collection using `yfinance` and `yahoofinancials`
- 🔍 Data Visualization with `matplotlib`
- 🧠 Machine Learning models: `Linear Regression` and `Random Forest Regressor`
- ✅ Model comparison using R² score
- ☁️ **Model Deployment** on **Google Cloud Platform**
- 🌐 Simple frontend using React to interact with the API

---

## 📦 Repository Structure

```
.
├── rf.pkl                # Trained Random Forest model
├── main.py               # Flask app for model serving
├── requirements.txt      # Python dependencies
├── Dockerfile            # Docker image configuration
└── notebook           # Jupyter notebook for analysis and training
```

---

## 🌐 Live API Endpoint

The trained model is hosted on Google Cloud and accessible via:

🔗 **Base URL:**  
[https://stock-predictor-service-530633117369.us-central1.run.app](https://stock-predictor-service-530633117369.us-central1.run.app)

🧪 **Prediction Endpoint:**  
`POST /predict/predict`  
**URL:**  
[https://stock-predictor-service-530633117369.us-central1.run.app/predict/predict](https://stock-predictor-service-530633117369.us-central1.run.app/predict/predict)

---

## 📮 Example Usage

### ✅ Request Body
```json
{
  "features": [5.1, 3.5, 1.4, 0.2]
}
```

### 🔁 Sample Response
```json
{
  "prediction": [2.970800054073334]
}
```

---

## 🛠 Setup Locally

### Backend (Flask API)

```bash
git clone https://github.com/shemzegem200/Stock-Price-Prediction-LinearReg-Versus-RandomForest.git
cd Stock-Price-Prediction-LinearReg-Versus-RandomForest

# Create virtual environment
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt

# Run the API
python main.py
```

### Frontend (React)

```bash
cd frontend
yarn install
yarn start
```

---

## ☁️ Deployment (Google Cloud Run)

The model is containerized with Docker and deployed to Google Cloud Run.

```bash
gcloud builds submit --tag gcr.io/YOUR_PROJECT_ID/stock-predictor
gcloud run deploy stock-predictor-service \
  --image gcr.io/YOUR_PROJECT_ID/stock-predictor \
  --platform managed \
  --region us-central1 \
  --allow-unauthenticated
```

---

## 📌 Dependencies

- `Flask`
- `scikit-learn`
- `joblib`
- `numpy`
- `yfinance`, `yahoofinancials`
- `matplotlib`
- `flask-cors`
- `gunicorn`

---

## 🧠 Author

Made with ❤️ by [Shyam Varadharajan](mailto:shyamvaradharajan200@gmail.com)  
GitHub: [@shemzegem200](https://github.com/shemzegem200)

---
