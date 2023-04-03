## Project: Estimation of wildfire using CNN

### Install

This project requires **Python** and the following Python libraries installed:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org/)
- [matplotlib](http://matplotlib.org/)
- [scikit-learn](http://scikit-learn.org/stable/)
- [tensorflow](https://www.tensorflow.org/)

You will also need to have software installed to run and execute a [Jupyter Notebook](http://jupyter.org/install.html).

If you do not have Python installed yet, it is highly recommended that you install the [Anaconda](https://www.anaconda.com/download/) distribution of Python, which already has the above packages and more included. 

This will open the Jupyter Notebook software and project file in your browser.

### DataSet

This dataset is public available for research. The details are described in [Cortez and Morais, 2007].(https://archive.ics.uci.edu/ml/datasets/forest+fires).

Title: Forest Fires

Sources
Created by: Paulo Cortez and An�bal Morais (Univ. Minho) @ 2007

Number of Instances: 517
Number of Attributes: 12 + output attribute

Attribute information:

- X - x-axis spatial coordinate within the Montesinho park map: 1 to 9
- Y - y-axis spatial coordinate within the Montesinho park map: 2 to 9
- month - month of the year: "jan" to "dec"
- day - day of the week: "mon" to "sun"
- FFMC - FFMC index from the FWI system: 18.7 to 96.20
- DMC - DMC index from the FWI system: 1.1 to 291.3
- DC - DC index from the FWI system: 7.9 to 860.6
- ISI - ISI index from the FWI system: 0.0 to 56.10
- temp - temperature in Celsius degrees: 2.2 to 33.30
- RH - relative humidity in %: 15.0 to 100
- wind - wind speed in km/h: 0.40 to 9.40
- rain - outside rain in mm/m2 : 0.0 to 6.4
- area - the burned area of the forest (in ha): 0.00 to 1090.84(this output variable is very skewed towards 0.0, thus it may make sense to model with the logarithm transform).
-Missing Attribute Values: None

### System Architecture

![image](https://user-images.githubusercontent.com/64827072/229441006-c94c3571-db69-480e-8c60-e57858b93a8a.png)


- *<b>Collecting the Raw Data:*</b> The first step involves collecting raw data from various sources, such as satellite and aerial imagery, weather data, and ground-based observations. The raw data will be in different formats and structures, so it needs to be collected, organized and integrated into a common database.
- *<b>Pre-processing the Data:*</b> The raw data will undergo various pre-processing steps to remove noise, filter out irrelevant information, and convert data into a common format. Pre-processing steps can include image resizing, colour correction, and normalization to ensure that the data is consistent and compatible with the CNN.
- *<b>Cleaning and Preparing the Data:*</b> The pre-processed data will be further cleaned and prepared by removing missing values and outliers, and transforming the data into the appropriate input format for the CNN. This step is critical for ensuring that the data is accurate, consistent, and representative of the underlying population.
- *<b>Splitting the Data into Training and Testing:*</b> The cleaned and prepared data will be divided into training and testing sets. The training set will be used to train the CNN, while the testing set will be used to evaluate the performance of the CNN.
- *<b>Applying the CNN:*</b> The CNN will be applied to the training data to learn the relationships between the input features and the output labels. The CNN architecture will consist of convolutional layers, pooling layers, and fully connected layers. The number of layers, filters, and activation functions will be optimized using hyperparameter tuning.
- *<b>Evaluating the Score:*</b> The performance of the CNN will be evaluated on the testing data using various metrics, such as accuracy, precision, recall, and F1 score. The evaluation metrics will provide insights into how well the CNN is performing and whether it is accurately predicting the behaviour of wildfires.


**Model Evaluation**
- R2 Score   - 0.02990449
- RMSE Value - 0.4924266

![image](https://user-images.githubusercontent.com/64827072/229441822-32ad5015-35d6-483f-85b4-98876bb37b6b.png)

![image](https://user-images.githubusercontent.com/64827072/229441953-ea2450ab-953d-4013-a891-712c86a7be1a.png)



