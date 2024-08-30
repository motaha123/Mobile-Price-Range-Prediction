# Mobile-Price-Range-Prediction
This project aims to predict the price range of mobile phones based on various features such as battery power, RAM, internal memory, etc. The dataset consists of several mobile phone specifications and their corresponding price ranges, classified into four categories.

Dataset

Training Data: Contains mobile phone features and the respective price range.

Test Data: Used for evaluating the model's performance on unseen data.
Data Processing

Data Concatenation: The training and test datasets were combined for unified preprocessing.

Feature Engineering:
Features like battery_power, clock_speed, mobile_wt, and int_memory were categorized into ordinal values representing the quality of the feature (e.g., low, medium, high).
Numerical features such as px_height, px_width, and ram were normalized using TensorFlow's Normalization layer.
Handling Missing Values: Ensured no missing values in the target column (price_range).


Data Visualization
Distribution of price ranges was visualized using bar plots.
Histograms were generated for each feature to understand their distributions and any necessary transformations.

Model Architecture
A neural network model was built using TensorFlow and Keras. The architecture of the model is as follows:

Input Layer: Takes input features with the shape of (number of features,).
Hidden Layers:
First Hidden Layer: 64 neurons with ReLU activation.
Second Hidden Layer: 32 neurons with ReLU activation.
Output Layer: 4 neurons with Softmax activation for multi-class classification.


Training Process
Loss Function: Categorical Crossentropy.
Optimizer: Adam.
Metrics: Accuracy.
Early Stopping: Implemented to prevent overfitting, monitoring the validation loss with a patience of 10 epochs.
Model Evaluation
Test Loss and Accuracy: The model was evaluated on the test set, achieving satisfactory accuracy.
Learning Curves: Plots for training and validation accuracy/loss were generated to visualize the model's performance over epochs.
Results
The model was trained and evaluated, and the following metrics were obtained:

Test Loss (Categorical Crossentropy): e.g., 0.6543
Test Accuracy: e.g., 82.56%
Predictions
The trained model was used to predict the price ranges for the test set. The predictions were added to the DataFrame for further analysis.

