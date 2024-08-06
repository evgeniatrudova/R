# R
Data Visualization and Model Evaluation Project: This project visualizes data and evaluates machine learning models using R. The focus is on linear regression, random forest, and neural network models. Various metrics are used for evaluation, including RMSE, MAE, and R-squared.

# Data Visualization and Model Evaluation Project

## Libraries Used
- `ggplot2`: A flexible library commonly used to visualize data in R.
- `caret`: A library for training and evaluating machine learning models.
- `randomForest`: A library for implementing the random forest algorithm.
- `nnet`: A library for neural network models.

## Project Structure
- `data/`: Contains the dataset (`exam.Rdata`).
- `scripts/`: Contains the R scripts for data cleaning, training models, evaluating models, and visualizing results.

## Data Cleaning
The dataset is cleaned by removing columns with missing values and columns with variance below 0.5.

```r
dataset_clean <- dataset[ , colSums(is.na(dataset)) == 0]
dataset_clean <- dataset_clean[, apply(dataset_clean, 2, var) >= 0.5]

