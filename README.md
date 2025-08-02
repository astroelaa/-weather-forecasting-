# -weather-forecasting-
# Weather Forecasting using Classical vs Quantum Machine Learning  
**Team 13 | Google Colab | Qiskit + scikit-learn**

## Overview
This project compares the performance of Classical Machine Learning (MLP Regressor) and Quantum Neural Networks (EstimatorQNN from Qiskit) in predicting average daily temperature using real-world weather data.

While classical models remain more accurate and faster, this work demonstrates the early feasibility of applying Quantum Machine Learning (QML) to practical regression problems, preparing for the future when quantum hardware scales.

---

## Project Structure


---

## Models Used

### Classical Model
- MLPRegressor from scikit-learn
- Hidden layer: 64 units
- Max iterations: 500
- Achieved MAE ≈ 1.5°C, R² ≈ 0.85

### Quantum Model
- EstimatorQNN using:
  - ZZFeatureMap (reps=3)
  - RealAmplitudes ansatz (reps=5)
  - Optimizer: COBYLA (500 iterations)
- Trained on small subsets (due to simulator limitations)
- Achieved MAE ≈ 3.0°C, R² ≈ 0.42

---

## Dataset Info

The features included:
- Wind speed, cloud cover, humidity, radiation
- Transformed features like sin_day, had_precipitation
- Target: temperature_2m_mean (°C)

Preprocessing steps:
- Z-score outlier removal
- Feature selection using F-regression
- Standard scaling
- Subsampling for the quantum model

---

## Results Summary

| Model    | MAE (°C) | RMSE (°C) | R² Score |
|----------|----------|-----------|----------|
| Classical | ~1.5     | ~2.0      | ~0.85    |
| Quantum   | ~3.0     | ~4.2      | ~0.42    |

Note: Quantum model was trained on only 500 samples due to simulator performance limits.

---

## Tech Stack
- Python (Google Colab)
- Qiskit & Qiskit Machine Learning
- scikit-learn
- NumPy, pandas, matplotlib

---

## How to Run

1. Clone the repository:
```bash
git clone https://github.com/your-username/weather-forecasting-qml.git
