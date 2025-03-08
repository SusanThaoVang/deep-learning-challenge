Background
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received access to a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special considerations for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

Compiling, Training, and Evaluating the Model

Model Structure

First Attempt:
The first attempt used the Starter_Code_M1.ipynb file, which included a neural network with two hidden layers. Since 2-4 layers are ideal for neural network models (NNMs), the first hidden node had 86 neurons (2-3 times the number of input features, which is 43), while the second hidden node had 43 neurons. The model was trained for 100 epochs using the reLU activation function (which is ideal for positive, nonlinear input data) and the sigmoid function (which normalizes values between 0 and 1, suitable for binary classification).

Second Attempt:
In the AlphabetSoupCharity_Optimization_Model2.ipynb file, the neural network used three hidden layers with 129, 86, and 43 neurons, trained for 150 epochs. The reLU activation and sigmoid functions were used.

Third Attempt:
The third model, from the AlphabetSoupCharity_Optimization_Model3.ipynb file, used four hidden layers with 172, 129, 86, and 43 neurons, trained for 200 epochs. The reLU activation and sigmoid functions were employed again.

Model Accuracy

The first model achieved an accuracy score of 72.49%.
The second model, with increased neurons and layers, achieved an accuracy score of 72.59%.
The third model, with more epochs, achieved an accuracy score of 72.47%.
Despite the adjustments, none of these models reached the target performance of 75%.
Steps to Increase Model Performance

In the second attempt, a third hidden reLU layer was added, and the number of training epochs was increased from 100 to 150 to provide more data to each neuron and improve the chances of reaching optimal weights.
In the third attempt, the model’s neurons, layers, and epochs were adjusted further. A fourth hidden reLU layer was added, and the number of epochs was increased to 200. The neuron counts were changed from 129, 86, and 43 to 172, 129, 86, and 43. These changes were aimed at speeding up the model, reducing loss, and considering more interactions between variables.
Summary:

Model Overview:
The deep learning model aimed to predict whether a company would be classified as successful or not based on features of their application. The highest accuracy score achieved across the three models was 72.59%, with a loss of 59.2%. Since these results did not meet the required threshold of 75%, further adjustments to hyperparameters are necessary to improve the binary classifier's reliability.

Additional Model Recommendation:
Another potential solution is to use a Perceptron model or a linear binary classifier. The Perceptron mimics a biological neuron by receiving input, weighting it, and producing a clear output. This method could effectively separate and classify the data into two groups: successful and not successful.
