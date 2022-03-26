# Anomaly-Detection

### Data Preparation

* Importing the dataset into pandas dataframe for feature processing and data cleaning.
* The data impurities was identified by using dtype() method, which initially printed all the feature as object. Hence the dataset may contained non-numeric value or null value which is to be handled.
* Non numeric data handling- For non numeric data used coerce() method to convert the explicitly change the non numeric type to float or int. Because searching through data frame for non numeric values was tedious.
* Null values handling- For Null values used fillna() method to fill the null value with nearest mean value(provided with range limit and period). Because null values can hamper the model learning process .
* Squeezing the data size- On observing the mean, median, top 25-50-75 %ile of minute basis data from describe() function, the data variance after transforming to per day dataset was negligible. Hence can be assured that data set on per day basis can be used for further analysis.

### Analysis Strategy

* Data feature selection - On observing the histogram of all the feature it’s found that some of the feature possessed same graphical structure, hence can be clubbed together as same feature. For instance the hist-plot of Inlet gas temp, Material temp and Outlet temp were similar, therefore were clubbed together as model learning feature. It’s also observed that the graph shows two spikes suggesting data inconsistency or we can say data is affected by some ambiguous data which need to handled. 
* Algorithm Used - k-nearest neighbors algorithm as it predicts a target variable using one or multiple independent variables.
* The decision for opting this algorithm was made based on observing the data variance and correlation, also on observing the data description using describe() function gave the idea about the data falling in top 25-50-75 %ile range.

### Insights

* Unsupervised Learning - On the context of unavailability of testing dataset and lack of knowledge about the working mechanism of Cyclone Preheater led to accept unsupervised learning approach. Moreover the dataset contained ambiguous data which can impute the model with false learning data and can lead to precision loss and inaccurate results.
* From the spikes in histogram graph insight about the data ranges drawn.
* Used Knn algorithm for this project since the dataset being contaminated with anomaly it can’t be trained using supervised techniques hence using a variable independent algorithm make sense.
* Why this algorithm - This algorithm uses unsupervised technique where it tries to group data points by evaluating the similarity, since on visualizing the histogram spots two spikes where data tends to accumulated and using this algorithm can be best way we can deal with such data set knowing there isn’t any test data set where we can verify the accuracy of the model.
* The abnormal periods are showed in the graphical output attached in the code with .pynb file.


