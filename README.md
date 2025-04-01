# Water Potability Prediction API 🌊🚰

This FastAPI application predicts water potability based on various chemical properties. The model determines whether water is safe for consumption using a machine learning model trained on water quality data.

## 🚀 Features
- **FastAPI-based API** for quick and efficient predictions
- **Machine Learning model integration** (loaded from `model.pkl`)
- **Two endpoints:**
  - `/` → Welcome message
  - `/predict` (POST) → Accepts water quality parameters and predicts potability

## 🛠️ Installation & Setup
### Clone the repository:
```bash
git clone https://github.com/yourusername/water-potability-api.git
cd water-potability-api
```

### Install dependencies:
```bash
pip install fastapi pandas numpy pickle5 uvicorn
```

### Run the API locally:
```bash
uvicorn main:app --reload
```

## 📱 Deployment
This project can be deployed on **Render**, **Heroku**, or **Dockerized** for cloud deployment.

## 🏗️ API Usage
### 1️⃣ Home Route  
**GET /**  
Returns a welcome message.

### 2️⃣ Prediction Route  
**POST /predict**  

#### Request Body (JSON):
```json
{
  "ph": 7.1,
  "Hardness": 120.5,
  "Solids": 21000.0,
  "Chloramines": 7.5,
  "Sulfate": 350.2,
  "Conductivity": 400.0,
  "Organic_carbon": 10.2,
  "Trihalomethanes": 70.5,
  "Turbidity": 4.5
}
```

#### Response:
- **"Water is Consumable"** if potable
- **"Water is not Consumable"** otherwise

## 🐟 License
MIT License

