### Customer churn prediction

### 1. Data Cleaning and Preparation

- Dropped customerID column: This was necessary as it doesn't contribute to the model.
- Handled missing values: You identified and filtered out rows with missing TotalCharges, which is a critical step.
- Converted TotalCharges to numeric: You correctly converted the column from object to float64.
- Replaced categorical values: You replaced categorical values like 'Yes'/'No' with 1/0, which is important for model training.
- Created dummy variables: You used pd.get_dummies to handle categorical features like InternetService, Contract, and PaymentMethod.

### 2. Data Visualization

- You visualized the distribution of tenure and MonthlyCharges based on the Churn status. This is a good approach to identify potential patterns.

### 3. Model Building

####  I.  Model Architecture
  - Layers:
    - Input Layer: A Dense layer with 26 units and ReLU activation. This layer expects input data with 26 features.
    - Hidden Layer: A Dense layer with 15 units and ReLU activation. This layer learns complex patterns from the data.
    - Output Layer: A Dense layer with 1 unit and sigmoid activation. This layer outputs probabilities for the binary classification task.
      python

####  II.  Compilation
  - Optimizer: Adam, which adapts the learning rate during training.
  - Loss Function: Binary Crossentropy, suitable for binary classification tasks.
  - Metrics: Accuracy, to evaluate the performance of the model.
  python

####  III.  Training
  - Epochs: 100 epochs were used for training the model.
  - Training Data: The model was trained on X_train and y_train.
    python

####  IV.  Evaluation
  - Test Data: The model was evaluated on X_test and y_test, achieving an accuracy of approximately 0.777 and a loss of 0.463.

    

