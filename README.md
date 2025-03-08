# deep-learning-challenge

OVERVIEW OF ANALYSIS

The purpose of this analysis is to develop a deep learning model using TensorFlow to predict the success of charitable organizations applying for funding from Alphabet Soup. The goal is to classify applications as successful or unsuccessful based on various financial and categorical factors. The model's performance is evaluated based on its predictive accuracy, with the target of achieving an accuracy above 75%.

RESULTS

Data Preprocessing

Target Variable:

IS_SUCCESSFUL (Binary classification: 1 for successful funding, 0 for unsuccessful)

Feature Variables:

APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT

These categorical features were transformed using one-hot encoding.

Variables Removed:

EIN and NAME were dropped as they are identifiers and do not contribute to predictive analysis.

Compiling, Training, and Evaluating the Model

Neural Network Architecture:

Input layer with 44 features (after one-hot encoding)

Three hidden layers:

First layer: 128 neurons, ReLU activation

Second layer: 64 neurons, ReLU activation

Third layer: 32 neurons, ReLU activation

Dropout layer with a dropout rate of 0.2 to prevent overfitting

Output layer: 1 neuron with sigmoid activation (for binary classification)

Model Performance:

The initial model achieved an accuracy of approximately 72%.

After optimization (increasing neurons, adding a dropout layer, adjusting epochs), the accuracy improved but did not consistently exceed 75%.

Steps Taken to Improve Performance:

Increased the number of neurons in hidden layers

Added an additional hidden layer

Implemented dropout to prevent overfitting

Increased the number of training epochs to 100

Experimented with different activation functions (ReLU and tanh)

SUMMARY

The deep learning model developed for Alphabet Soup was able to classify funding applications with a reasonable accuracy of ~72-74%, but did not consistently surpass the 75% threshold. The optimization attempts improved performance slightly, but diminishing returns were observed.

Alternative Approaches

A different model could be used to solve this classification problem, such as:

Random Forest Classifier: A tree-based model that handles categorical features well and is less sensitive to scaling.

Gradient Boosting (XGBoost): A boosting algorithm that often outperforms neural networks on structured data.

Logistic Regression: A simpler model that could be used as a baseline for comparison.