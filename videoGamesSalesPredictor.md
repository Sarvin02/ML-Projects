# Video Games Sales Predictor

## Project Overview
This project aims to predict the global sales of video games based on various features such as platform, genre, publisher, and other attributes. The dataset used for this project is sourced from Kaggle and contains detailed information about video games.

## Objectives
1. Preprocess the dataset to handle missing values, duplicates, and categorical variables.
2. Build a Multi-Layer Perceptron (MLP) model to predict global sales.
3. Evaluate the model's performance using metrics like Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).
4. Provide insights into the predictions by mapping them back to the original features.

## Steps Involved
1. **Data Loading**: Download and load the dataset using KaggleHub.
2. **Data Preprocessing**:
   - Handle missing values and duplicates.
   - Perform one-hot encoding for categorical variables.
   - Drop unnecessary columns.
   - Scale numerical features and label encode categorical ones.
3. **Model Building**:
   - Create an MLP model with multiple dense layers.
   - Compile the model using Adam optimizer and MAE loss function.
   - Train the model on the preprocessed data.
4. **Model Evaluation**:
   - Evaluate the model on the test set.
   - Generate predictions and compare them with actual values.
5. **Insights**:
   - Map predictions back to the original features like genre, publisher, and platform.
   - Display predictions alongside actual sales for better interpretability.

## Key Features
- **Dataset**: Video Games Sales Dataset (2022 Updated with Extra Features).
- **Model**: Multi-Layer Perceptron (MLP).
- **Metrics**: MAE and RMSE.
- **Tools**: TensorFlow, Pandas, Scikit-learn.

## Results
The model predicts global sales with reasonable accuracy, providing insights into the factors influencing sales performance.

## Future Work
- Experiment with other machine learning models like Random Forest or Gradient Boosting.
- Incorporate additional features to improve prediction accuracy.
- Visualize the results using interactive plots for better understanding.

