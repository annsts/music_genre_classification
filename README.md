# Music Genre Classification

## Overview
This project involves building a classification model to predict the genre of a song based on its features.

## Process
### Data Preprocessing
- Removed rows with missing `instance_id`, `artist_name`, and `track_name`.
- Replaced missing values in `duration_ms` and `tempo` with medians.
- One-hot encoded the `key` column; label encoded the `mode` and `music_genre` columns.
- Standardized numerical features.

### Train/Test Split
- Split dataset: 500 songs per genre for the test set, remaining for training.

### Dimensionality Reduction and Visualization
- Used t-SNE and UMAP for visualization.
- Applied HDBSCAN for clustering analysis.

### Model Training
- Added cluster labels as features.
- Used XGBoost for classification.
- Evaluated with ROC AUC and accuracy metrics.

## Results
- Mean ROC AUC: 0.9345 (test set).
- Accuracy: 64.59% (training), 58.82% (test).
- Observed overfitting; suggested cross-validation, regularization, and further feature engineering.

## Conclusion
- Feature engineering and data preprocessing were crucial.
- Visualized audio features highlighted the complexity of genre classification.
- Further improvements needed for practical application.

For a detailed description, refer to [report.pdf](report.pdf).