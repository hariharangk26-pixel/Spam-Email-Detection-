# Spam Email Detection

A beginner-friendly cybersecurity and machine-learning mini project using Python, Flask, TF-IDF, and Multinomial Naive Bayes.

## Features
- Paste a message into a web form.
- Classify the message as `SPAM` or `HAM` (not spam).
- Display the model's predicted class probability.
- Simple responsive web interface.
- Optional training script for a labelled CSV dataset.

## Requirements
- Python 3.10 or newer
- pip

## Run locally
1. Download or clone this repository.
2. Open a terminal in the project folder.
3. Create and activate a virtual environment.

Windows:
```bash
python -m venv .venv
.venv\\Scripts\\activate
```

macOS/Linux:
```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install dependencies:
```bash
pip install -r requirements.txt
```

Start the application:
```bash
python app.py
```
Open `http://127.0.0.1:5000` in your browser.

The first run creates `spam_model.pkl` using a small built-in sample dataset.

## Optional: train with your own data
Create a CSV with columns `text,label`, where labels are `spam` or `ham`, and include many examples from both classes. Then run:
```bash
python train_model.py path/to/spam.csv
```

## Limitations
The built-in dataset is intentionally tiny and only demonstrates the workflow. Predictions are not reliable enough for real email filtering. For meaningful evaluation, use a reputable labelled dataset, test on held-out data, and report precision, recall, F1-score, and a confusion matrix. Do not paste confidential messages into the demo.
