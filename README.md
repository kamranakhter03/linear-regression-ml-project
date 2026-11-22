# Linear Regression: Pune food delivery orders

A food delivery app in Pune shows every customer a delivery time when they place an order. Right now the app shows the same **"35 minutes"** for everyone, so people who live close get their food early, and people who live far get it late and leave angry reviews.

The operations team has the records of 200 past orders. They want a model that looks at a new order and says **how many minutes it will take**, so the app can show an honest time.

**Goal:** Predict delivery_minutes (a number) for a new order. Predicting a number is a regression problem, so we start with Linear Regression.

## What is inside

| File | What it is |
| --- | --- |
| [`linear_regression.ipynb`](linear_regression.ipynb) | The full notebook: data checks, training, testing and a prediction |
| [`data/deliveries.csv`](data/deliveries.csv) | 200 past orders, one row per order. |
| [`requirements.txt`](requirements.txt) | Python packages the notebook uses |

## The data

- `order_id`: Order number (just an id, not used by the model)
- `distance_km`: Distance from the restaurant to the customer
- `prep_minutes`: Minutes the restaurant took to pack the food
- `peak_hour`: Was it lunch or dinner rush? (Yes / No)
- `raining`: Was it raining? (Yes / No)
- `delivery_minutes`: What we want to predict: total minutes until delivery

## Run it yourself

```bash
pip install -r requirements.txt
jupyter notebook linear_regression.ipynb
```

Or open `linear_regression.ipynb` in Google Colab and upload the `data` folder next to it.

## What I learned

- Linear Regression predicts a number by fitting a straight line (or a flat plane, with many inputs).
- Always test on data the model has not seen: train_test_split.
- MAE tells the error in the same unit as the answer (minutes here), so anyone can understand it.
- Coefficients explain the model: each one says how much that input adds.
- Text columns must become numbers before training.

---

Built while learning Machine Learning on [JobPrax](https://www.jobprax.com/ml/linear-regression). The data is realistic practice data.
