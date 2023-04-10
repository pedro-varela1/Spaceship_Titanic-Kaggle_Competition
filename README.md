# Spaceship Titanic - Kaggle Competition

This Jupyter Notebook provides a solution to the Spaceship Titanic Kaggle Competition. It predicts whether a passenger was transported or not based on their characteristics. It uses TensorFlow and Keras libraries for machine learning.

## Libraries used

- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Seaborn

## Data Import
The first step is to import the data. The train and test datasets are imported using Pandas' read_csv() function.

## Data Analysis
The data is analyzed and visualized using various functions of Pandas and Seaborn libraries. The unique values of some features are shown using value_counts() function. The relationship between different features is shown using a pairplot from Seaborn.

## Feature Selection
The important features are selected for the model. These features are 'HomePlanet', 'CryoSleep', 'Cabin', 'Destination', 'VIP', 'Age', and 'Spend'. The 'Spend' feature is created by adding the RoomService, FoodCourt, Spa, VRDeck, and ShoppingMall columns.

## Data Preprocessing
The missing values are filled using the mean of the respective columns. The age and spend values are separated into 5 categories. The non-numerical values are converted to numerical values. The final train and test features and labels are created.

## Model Creation
A Sequential model is created with the following layers:

- Dense layer with 64 units and ReLU activation function
- Dropout layer with 0.2 rate
- Dense layer with 64 units and ReLU activation function
- Dropout layer with 0.2 rate
- Dense layer with 1 unit and sigmoid activation function

The optimizer used is Adam and binary cross-entropy is used as the loss function. The accuracy is used as the metric.

## Model Training
The model is trained with 100 epochs and a batch size of 32. The training data is split into 80:20 for training and validation data.

## Model Evaluation
The model is evaluated on the validation data using the evaluate function. The model is also evaluated on the test data and the predictions are saved in a CSV file.

## Conclusion
This Jupyter Notebook provides a complete solution to the Spaceship Titanic Kaggle Competition. It achieves an accuracy of 84% on the validation data and 78% on the test data.
