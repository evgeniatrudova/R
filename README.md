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

# Model Training

## Linear Regression
Three linear regression models are built to predict the response variable using LogP, TopoPSA, and MW.

## Random Forest
A random forest model is trained to predict the response variable.

## Neural Network
A neural network model is trained and evaluated.

## Evaluation Metrics
- **Root Mean Squared Error (RMSE)**: A metric that penalizes larger errors more than smaller ones.
- **Mean Absolute Error (MAE)**: A metric that checks for prediction errors.
- **R-squared (R2)**: Indicates the proportion of variance explained by the model.

## Results
The results are visualized using ggplot2, showing scatter plots with regression lines. The evaluation metrics are displayed as subtitles on the plots.

### Example of Linear Regression Plot
```r
ggplot(plot_data_LogP, aes(x = XLogP, y = response)) +
  geom_point() +
  geom_line(aes(y = predictions), color = "blue", size = 1) +
  labs(
    x = "XLogP",
    y = "Response",
    title = "Linear Regression: Response vs. XLogP",
    subtitle = metrics_text
  ) +
  theme_minimal() +
  theme(
    plot.subtitle = element_text(size = 10, hjust = 0.5)
  )
