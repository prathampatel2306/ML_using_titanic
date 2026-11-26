# ML_using_titanic
# Titanic Survival: Baseline (Level 1)

## Project
The project is to make a model worth trusting on the prediction of Titanic survivors. This is the starting phase: a clear baseline for comparison with further improved models.

## Dependencies
- scikit-learn: `pip install scikit-learn`
- pandas: `pip install pandas`

## How to run
1. Download `train.csv` from the Kaggle "Titanic - Machine Learning from Disaster" competition page.
2. Place it in: The same folder as the notebook(type the path the notebook reads)
3. Open and run the notebook.

## Data
The data is `train.csv` from the Kaggle "Titanic - Machine Learning from Disaster" competition. It is not included in this repository because the competition rules don't allow redistributing the data.

## Baseline result
The DummyClassifier with `most_frequent` scores 61.45% accuracy on the test set. It predicts non-survivor (0) for every passenger, so the score equals the share of non-survivors in the test set. This is the score future models must beat to be considered useful.

## Decisions
- **most_frequent:** It predicts the majority class from the training labels, so it's the simplest possible guess to compare against.
- **Stratified 80/20 split:** It keeps the survival ratio the same in train and test, so the test score reflects the real class balance.
- **Accuracy as the headline metric:** The brief asks for one accuracy number, and this baseline only needs to show how many predictions are correct.

## Limits
This baseline ignores all features, so it doesn't show how a real model would use passenger information to predict survival. Its score also depends on the class balance of this dataset.
