# R
Data Visualization and Model Evaluation Project: This project visualizes data and evaluates machine learning models using R. The focus is on linear regression, random forest, and neural network models. Various metrics are used for evaluation, including RMSE, MAE, and R-squared.

![1](https://github.com/user-attachments/assets/b521bdc0-e976-4b5b-82d8-ec8ccdd76ecd)
![2](https://github.com/user-attachments/assets/700d0ce0-49b9-4463-9ae6-ac64f9c21d2c)
![3](https://github.com/user-attachments/assets/2aace1f6-8401-4d28-bf4f-fa2c959938cd)
![4](https://github.com/user-attachments/assets/dbd4895c-1b50-46c0-94a8-801b28ed3c24)
![5](https://github.com/user-attachments/assets/7414784f-fbed-48cd-9726-ce670f11bc71)
![6](https://github.com/user-attachments/assets/d32bed28-d26c-4bfd-9d32-91e5986a9f74)
![7](https://github.com/user-attachments/assets/393fdbdf-53d0-449f-8781-4e9d4d98d8c9)
![8](https://github.com/user-attachments/assets/bbed76f7-9b90-4417-8482-9417a00ab2cc)
![9](https://github.com/user-attachments/assets/858740ff-af03-46f8-8413-4dc2c054dc63)

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
