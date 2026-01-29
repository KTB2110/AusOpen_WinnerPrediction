# Australian Open Winner Prediction

A machine learning project that predicts match outcomes and tournament brackets for the Australian Open tennis championship. This project was developed as an undergraduate capstone at Purdue University.

## Project Overview

This project uses historical player statistics and match data to predict the outcomes of Australian Open tennis matches. We implemented and compared multiple machine learning models to determine the most effective approach for tournament bracket prediction.

## Models Implemented

- Multi-Layer Perceptron (Neural Network)
- Support Vector Machines (Linear, Polynomial, and RBF kernels)
- Gradient Boosting
- Logistic Regression

## Data Sources

Player statistics and match outcomes were collected from:
- ATP Tour official statistics (atptour.com)
- Historical tennis match data (tennis-data.co.uk)

The dataset includes player performance metrics from 2014-2019, with features such as service statistics, return game performance, and head-to-head records.

## Project Structure

```
.
├── data/                          # Historical match and player statistics
├── multi_layer_perceptron/        # Neural network implementation
├── data_exploration.ipynb         # Exploratory data analysis
├── data_prep.py                   # Data preprocessing pipeline
├── main.py                        # Data collection script
├── linearSVM.py                   # Linear SVM implementation
├── polySVM.py                     # Polynomial SVM implementation
├── rbfSVM.py                      # RBF SVM implementation
├── GradientBoost.py               # Gradient boosting implementation
└── LogisticRegression.R           # Logistic regression implementation
```

## Setup

Install required dependencies:

```bash
pip install -r requirements.txt
```

## Usage

### Data Collection

To collect player statistics for a specific year:

```bash
python3 main.py --year 2018
```

This will scrape player statistics and save them to the data directory.

### Running the Neural Network Model

1. Ensure the required data files exist in the `data/` directory
2. Open `multi_layer_perceptron/neural_network.ipynb`
3. Verify the training and testing years are correctly specified
4. Run the notebook to generate predictions

### Running SVM Models

Execute the respective Python scripts:

```bash
python3 linearSVM.py
python3 polySVM.py
python3 rbfSVM.py
```

### Running Gradient Boosting

```bash
python3 GradientBoost.py
```

## Key Findings

The neural network model demonstrated the strongest performance in predicting match outcomes. Player service statistics and recent form proved to be the most predictive features across all models.

## Assumptions and Limitations

- Players with missing statistics are treated as walkovers
- The model is trained on hard court data specific to the Australian Open
- Predictions do not account for injuries or off-court factors

## Authors

- Aaditya Bhoota
- Krishna Tej Bhat
- Chintan Sawla
- Leyla Ciner
- Macie Wheeler
- Smruti Srinivasan
- Dhruv Marwa

Purdue University
