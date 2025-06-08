# Prediction Modeling Notebook

This notebook performs predictive modeling to classify movies as "flops" or "non-flops" based on the enriched movie dataset created earlier in the project.

---

## Purpose

The goal of this notebook is to use machine learning classification techniques to predict whether a movie will be a flop, using features such as budget, user ratings, vote counts, release year, and genres. This helps validate and extend the "Flop Score" concept by building models that learn patterns from historical data.

---

## Notebook Outline and Explanation

### 1. Upload and Load Data

- The notebook begins by uploading the `enriched_worst_200_with_flop_score.csv` file.
- This dataset contains movie features enriched with financial data, ratings, genres, and the computed flop score.
- Loading this data is the foundation for training and testing the predictive models.

### 2. Define Target Variable

- We create a binary target variable `is_flop` based on a threshold flop score (e.g., movies with flop score > 50% are considered flops).
- This binarization allows us to formulate the prediction as a classification problem.

### 3. Feature Selection and Preprocessing

- We select key features that influence flop likelihood: budget, average vote rating, vote count, release year, and genres.
- The genres field is one-hot encoded for the top genres to handle categorical data.
- Missing values are dropped to ensure clean model inputs.

### 4. Train/Test Split

- The dataset is split into training (75%) and test (25%) subsets.
- Stratified splitting maintains the proportion of flop/non-flop classes across splits.

### 5. Train Classification Models

- Two models are trained:
  - **Logistic Regression:** a simple linear model that estimates probabilities.
  - **Random Forest Classifier:** an ensemble model capturing nonlinear relationships and interactions.
- Both models learn to predict `is_flop` from the feature set.

### 6. Model Evaluation

- We evaluate model performance using multiple metrics:
  - **Accuracy:** overall correctness of predictions.
  - **Precision:** correctness among predicted flops.
  - **Recall:** how many true flops were captured.
  - **F1 Score:** balance of precision and recall.
  - **ROC AUC:** ranking ability of the model.
- Confusion matrices visualize true positives, false positives, true negatives, and false negatives.

### 7. Feature Importance Analysis

- For Logistic Regression, we inspect feature coefficients to understand positive or negative impacts.
- For Random Forest, we examine feature importances indicating which features contribute most to predictions.
- These insights guide understanding of factors driving flop likelihood.

---

## Relevance to Overall Project

This notebook builds on the enriched movie dataset created in prior steps, transforming descriptive data into actionable predictive models. It demonstrates practical application of machine learning to evaluate the "flop score" concept, enabling future improvements such as:

- Refining the flop score calculation.
- Exploring additional data sources or features.
- Deploying the model for real-time flop prediction or recommendation systems.

---

## How to Use

1. Upload the `enriched_worst_200_with_flop_score.csv` file when prompted.
2. Run all notebook cells sequentially.
3. Review model metrics, confusion matrices, and feature importance plots.
4. Save or export any results and visualizations as needed.

---

Feel free to explore and build upon this modeling framework to deepen insights into movie performance prediction!
