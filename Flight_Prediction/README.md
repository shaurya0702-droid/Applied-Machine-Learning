# ✈️ Flight Delay Predictor

A machine learning project that predicts whether a flight will be delayed by more than 15 minutes using historical US flight data.

The model is trained using airline, airport, departure time, distance, and date-related features.

Dataset used:
US DOT Flight Delays 2015 (Kaggle)

---

# Model Performance

| Metric | Score |
|---|---|
| ROC-AUC | 0.703 |
| F1 Score | 0.380 |

The dataset is imbalanced because most flights are on time, so F1-score and ROC-AUC were used instead of accuracy.

---

# Features Used

| Feature | Meaning |
|---|---|
| AIRLINE | Airline code |
| ORIGIN_AIRPORT | Source airport |
| DESTINATION_AIRPORT | Destination airport |
| HOUR | Departure hour |
| MONTH | Month number |
| DAY_OF_WEEK | Day number |
| DISTANCE | Flight distance |

---

# Data Cleaning

The dataset was cleaned by:

- Removing cancelled flights
- Removing missing values
- Removing duplicate rows
- Keeping valid airport codes only
- Removing invalid departure times
- Removing unrealistic delay values

---

# Technologies Used

- Python
- pandas
- scikit-learn
- LightGBM
- matplotlib

---

# Project Workflow

1. Load dataset
2. Clean data
3. Create features
4. Train LightGBM model
5. Evaluate using F1-score and ROC-AUC
6. Predict flight delays

---

# Run the Project

Install dependencies:

```bash
pip install -r requirements.txt
```

Download the dataset from Kaggle and place:

```bash
data/flights.csv
```

Run the notebook:

```bash
jupyter notebook flight_delay_predictor.ipynb
```

---

# Project Structure

```text
flight-delay-predictor/
│
├── flight_delay_predictor.ipynb
├── requirements.txt
├── README.md
└── data/
    └── flights.csv
```

---

# License

MIT