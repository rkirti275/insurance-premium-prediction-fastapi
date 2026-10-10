# Insurance Premium Prediction API

A Machine Learning-powered REST API built using **Python and FastAPI** to predict insurance premiums based on user-related features such as BMI, age group, lifestyle risk, city tier, income, and occupation.

## Project Overview

This project integrates a Machine Learning model with FastAPI to provide insurance premium predictions through REST API endpoints. It uses Pydantic schemas for request validation and provides interactive API documentation using Swagger UI.

## Features

- Insurance premium prediction through a REST API
- Input validation using Pydantic
- Machine Learning model integration
- Health check endpoint to monitor API and model status
- Interactive API documentation with Swagger UI
- Docker configuration for containerization

## Tech Stack

- **Programming Language:** Python
- **Backend Framework:** FastAPI
- **ASGI Server:** Uvicorn
- **Data Validation:** Pydantic
- **Machine Learning:** Scikit-learn
- **Data Processing:** NumPy, Pandas
- **Containerization:** Docker

## Project Structure

```text
insurance-premium-prediction-fastapi/
├── app.py
├── config/
├── model/
│   └── predict.py
├── schema/
│   ├── user_input.py
│   └── prediction_response.py
├── requirements.txt
├── Dockerfile
└── README.md
```

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/rkirti275/insurance-premium-prediction-fastapi.git
```

### 2. Navigate to the project directory

```bash
cd insurance-premium-prediction-fastapi
```

### 3. Create a virtual environment

```bash
python -m venv venv
```

### 4. Activate the virtual environment

**Windows PowerShell:**

```powershell
.\venv\Scripts\Activate.ps1
```

### 5. Install dependencies

```bash
python -m pip install -r requirements.txt
```

### 6. Start the FastAPI server

```bash
python -m uvicorn app:app --reload
```

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/` | Returns the API welcome message |
| GET | `/health` | Checks API and model status |
| POST | `/predict` | Generates an insurance premium prediction |
| GET | `/docs` | Opens interactive API documentation |

## API Documentation

After starting the server, open:

**Swagger UI:** http://127.0.0.1:8000/docs

**Health Check:** http://127.0.0.1:8000/health

Use Swagger UI to provide input data, execute requests, and inspect API responses.

## Input Features

The prediction endpoint accepts the following features:

- `bmi`
- `age_group`
- `lifestyle_risk`
- `city_tier`
- `income_lpa`
- `occupation`

Refer to `schema/user_input.py` for the expected data types and allowed values.

## Learning Outcomes

- Building REST APIs using FastAPI
- Integrating Machine Learning models into backend applications
- Validating input data using Pydantic
- Testing API endpoints using Swagger UI
- Organizing a Python project into modular components

## Future Improvements

- Develop a user-friendly web frontend
- Deploy the API to a cloud hosting platform
- Add automated testing
- Improve error handling and monitoring

## Author

**Kirti Ratnawat**

GitHub: [@rkirti275](https://github.com/rkirti275)

---

*This project is developed for learning and demonstrating Machine Learning model integration with FastAPI.*
