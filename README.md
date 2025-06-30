## Fraud Detection Pipeline

This repository contains a multi-stage fraud detection pipeline implemented in Python. It leverages synthetic data to simulate a real-world scenario and includes the following components:

- **Data Ingestion**: Generate and load synthetic data mimicking PDF specifications.
- **Data Cleaning**: Remove columns with excessive missing values and drop redundant fields.
- **Feature Engineering**: Create new features, including flag aggregations, time-series summaries, and custom indicators.
- **Stage 1: High-Recall Filtering**: Train an XGBoost model to filter potential fraud cases with high recall.
- **Stage 2: Neural Network**: Build and evaluate a deep neural network on the filtered subset for refined predictions.
- **Ensemble with Uncertainty Handling**: Combine multiple classifiers (XGBoost, MLP, LGBM, CatBoost, Logistic Regression, ExtraTrees, RandomForest) and handle uncertain predictions.

---

### Table of Contents

1. [Installation](#installation)  
2. [Project Structure](#project-structure)  
3. [Usage](#usage)  
4. [Pipeline Overview](#pipeline-overview)  
   - [Data Ingestion](#data-ingestion)  
   - [Data Cleaning](#data-cleaning)  
   - [Feature Engineering](#feature-engineering)  
   - [Stage 1: High-Recall Filtering](#stage-1-high-recall-filtering)  
   - [Stage 2: Neural Network Training](#stage-2-neural-network-training)  
   - [Ensemble with Uncertainty Handling](#ensemble-with-uncertainty-handling)  
5. [Model Saving](#model-saving)  
6. [License](#license)  

---

### Installation

```bash
# Clone this repository
git clone https://github.com/yourusername/fraud-detection-pipeline.git
cd fraud-detection-pipeline

# Create and activate a virtual environment
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

Ensure you have Python 3.8+ installed. The requirements.txt includes:
pandas
numpy
scikit-learn
xgboost
lightgbm
catboost
tensorflow
joblib
