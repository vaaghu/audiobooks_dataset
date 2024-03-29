<h2>Introduction</h2>

The audiobook dataset contains information about audiobook customers over a two-year period. The purpose of this data science project is to analyze the dataset and develop a model to predict whether or not a customer will make a purchase after two years.</br>
</br></br>
<h2>Data Description</h2>

The dataset contains 10 columns:</br>

ID: ID of each customer.</br>
Book length (mins)_overall: The overall purchased length of books.</br>
Book length (mins)_avg: The average purchased length of books.</br>
Price_overall: The total price paid by the customer.</br>
Price_avg: The average price paid by the customer.</br>
IsReview: A boolean value indicating whether or not the customer has left a review.</br>
Review: The rating given by the customer on a scale of 0 to 10.</br>
Minutes listened: The total minutes the customer listened to audiobooks.</br>
Completion: The percentage of total minutes listened to total purchased minutes.</br>
Support requested: The number of times a customer requested support.</br>
Time length: The time period between the last visit and the purchase date.</br>
Target: Whether or not the customer made a purchase after two years.</br>
</br></br>
<h2>Exploratory Data Analysis</h2>

The dataset was analyzed by performing the following steps:

Book Length: Over 97% of customers on average bought audiobooks of length less than 2500 minutes, with the 100th percentile being 7000 minutes. The average length of audiobooks purchased by each customer was 1678.6 minutes, with a standard deviation of 654.8 minutes.</br>

Price: Over 97% of customers on average bought audiobooks of price less than $10, with the 100th percentile being $140. The average price paid by each customer was $7.54, with a standard deviation of $5.56.</br>

Book Completion: More than 60% of customers didn't even start their audiobook even once. The mean book completion rate was 0.1256, with a standard deviation of 0.2412.</br>

Repeat Purchases: More than 84% of customers didn't buy the same audiobook again.</br>
</br></br>
<h2>Data Pre-processing</h2>

The dataset was pre-processed by performing the following steps:</br>

Balancing Priors: The target variable was imbalanced, so the data was balanced by removing some rows with target value 0.</br>
Standardizing Data: The unscaled inputs were standardized using the preprocessing module from the scikit-learn library.</br>
Shuffling Data: The shuffled_indices function from numpy.random module was used to shuffle the data.</br>
Splitting Data into Train, Validation, Test: The data was split into three sets, 80% for training, 20% for validation, and 10% for testing. </br>
The np.savez function was used to save each set in a separate file.</br>
</br></br>
<h2>Model Development</h2>

The pre-processed data was used to train a model to predict the target variable using TensorFlow. The model was developed using a sequential neural network with three dense layers. </br>
The loss function used was binary cross-entropy, and the optimizer used was Adam. The accuracy metric was used to evaluate the model.</br>
</br></br>
<h2>Results</h2>

The model was evaluated on the test set, and the following results were obtained:</br>

Test loss = 0.240</br>
Test accuracy = 0.910</br>
</br></br>
<h2>Conclusion</h2>

In conclusion, the audiobook dataset was analyzed and pre-processed by balancing priors, standardizing data, shuffling data, and splitting data into train, validation, and test sets. A sequential neural network model was developed using TensorFlow, and the model was evaluated on the test set. The model achieved a test accuracy of 0.910, which indicates that it is a good
