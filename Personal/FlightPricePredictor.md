# Flight Price Predictor

This project uses a Random Forest Regressor to predict flight prices based on various features from a flight dataset. The workflow includes data preprocessing, model training, evaluation, and visualization.

## Steps

### 1. Import Required Libraries

- pandas, numpy: Data handling and numerical operations
- scikit-learn: Model, preprocessing, evaluation, and visualization
- matplotlib: Plotting
- kagglehub: Dataset access

### 2. Load the Dataset

The dataset is loaded using kagglehub and pandas:

```python
df = pd.read_csv(kagglehub.dataset_download("rohitgrewal/airlines-flights-data")+"/airlines_flights_data.csv")
```

### 3. Data Preprocessing

- **One-hot encoding** is applied to categorical columns: `airline`, `source_city`, `destination_city`, `arrival_time`, `departure_time`, `class`, and `stops`.
- Unnecessary columns (like `flight`) are dropped.
- Rows with missing values and duplicates are removed.

### 4. Feature and Target Split

- Features (`X`) are all columns except `price`.
- Target (`y`) is the `price` column.
- Data is split into training and test sets.

### 5. Model Training

A Random Forest Regressor is trained on the training data:

python
model = RandomForestRegressor(random_state=42)
model.fit(X_train, y_train)


### 6. Visualize a Decision Tree

A single tree from the random forest is visualized (top 3 levels) to understand the model's decision process.

### 7. Model Evaluation

- The model is tested on the test set.
- Metrics: Mean Squared Error (MSE) and R² Score are printed.

### 8. Visualization of Predictions

A bar plot compares actual vs. predicted prices for a random sample of 20 test cases.

### 9. Test Case Details

A table displays the original feature values for each test sample in the bar plot, along with their actual and predicted prices.

## Notes

- All categorical features are encoded for model compatibility.
- The bar plot's sample indices are just positions in the displayed sample, not original row numbers.
- The table below the plot helps interpret what each sample index represents.

---

