# Exam Score Predictor

A machine learning project that predicts a student's exam score from their study habits using **linear regression**.

## Features used
| Feature | Meaning |
|---|---|
| hours_studied | Study hours per day |
| attendance | Class attendance % |
| previous_score | Score in the last exam |
| sleep_hours | Average sleep per night |

## Setup and run
```bash
pip install -r requirements.txt
python generate_data.py      # creates students.csv (synthetic data)
python train.py              # trains the model, prints metrics, saves results.png
python predict.py --hours 6 --attendance 90 --previous 70 --sleep 7
```

## Results
The training script prints R2 and mean absolute error on unseen test data, and shows which factors add the most marks. See `results.png` for actual vs predicted scores.

## Using real data
The dataset is synthetic so the project runs anywhere. To use a real one (for example a Kaggle student performance dataset), save it as `students.csv` with the same column names, or edit `FEATURES` in `train.py`.

## What I learned
- Train/test splitting and why it matters
- Evaluating regression with R2 and MAE
- Reading model coefficients to understand which factors matter
- Saving and reloading a trained model

## Ideas to extend
- Compare with Random Forest or Ridge regression
- Add a Streamlit web interface
- Add feature scaling and cross-validation
