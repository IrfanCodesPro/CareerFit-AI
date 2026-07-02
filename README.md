# CareerFit AI

AI-powered career guidance system that uses Natural Language Processing (NLP) and a Random Forest classifier to analyze student skills, interests, and academic profiles, and recommend personalized career paths.

## Overview

CareerFit AI helps students and early-career professionals make data-driven decisions about their career direction. It parses free-text and structured profile data (skills, interests, academic background), extracts meaningful features using NLP techniques, and feeds them into a trained Random Forest model to predict the most suitable career paths.

This project was developed as part of ongoing research on AI-driven career guidance and is referenced in an IEEE RAASC co-authored publication.

## Features

- **Profile Parsing** – Extracts structured information (skills, interests, academic scores) from user input using NLP
- **Feature Engineering** – Converts textual and categorical data into model-ready features (TF-IDF / encoding)
- **Career Prediction** – Random Forest classifier trained on labeled career-outcome data to recommend suitable paths
- **Explainable Output** – Surfaces top contributing features behind each recommendation
- **Extensible Dataset** – Easily retrainable as new career/skill data becomes available

## Tech Stack

- **Language:** Python
- **ML/NLP:** scikit-learn (Random Forest), NLTK / spaCy (text preprocessing)
- **Data Handling:** pandas, NumPy
- **Model Persistence:** joblib / pickle
- **(Optional) Interface:** Flask / Streamlit for demo UI

## Project Structure

```
CareerFit-AI/
├── data/                  # Training and sample datasets
├── src/
│   ├── preprocessing.py   # NLP text cleaning & feature extraction
│   ├── train_model.py     # Model training script
│   ├── predict.py         # Inference / prediction script
│   └── utils.py           # Helper functions
├── models/                 # Saved trained models
├── notebooks/               # EDA and experimentation notebooks
├── requirements.txt
└── README.md
```

## Installation

```bash
git clone https://github.com/IrfanCodesPro/CareerFit-AI.git
cd CareerFit-AI
pip install -r requirements.txt
```

## Usage

**Train the model:**
```bash
python src/train_model.py
```

**Run a prediction:**
```bash
python src/predict.py --skills "Python, Data Analysis" --interests "AI, Problem Solving" --cgpa 8.2
```

**Sample Output:**
```
Recommended Career Path: Data Scientist
Confidence: 87%
Top Contributing Features: Python proficiency, Analytical interest, Academic performance
```

## Model Details

- **Algorithm:** Random Forest Classifier
- **Preprocessing:** Text vectorization (TF-IDF) for skill/interest fields, label encoding for categorical academic data
- **Evaluation Metrics:** Accuracy, Precision, Recall, F1-score (see `notebooks/` for evaluation results)

## Future Improvements

- Expand dataset for better generalization across career domains
- Add bias/fairness auditing across demographic and academic subgroups
- Deploy as a web app with real-time recommendations
- Integrate with resume parsing for end-to-end profile analysis

## Author

**Irfan S**
Software & AI/ML Lead, Unified Automations & Tech Solutions (UATS)
[GitHub](https://github.com/IrfanCodesPro) · [Portfolio](https://irfanportfolio.pythonanywhere.com)

## License

This project is licensed under the MIT License.
