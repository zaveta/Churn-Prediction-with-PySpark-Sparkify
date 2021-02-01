# Churn Prediction with PySpark

### Motivation
Sparkify is a fake music streaming service invented by Udacity. Here users can listen to music for free (with ads between songs) or for a flat fee. Users can upgrade, downgrade, or cancel. My task is to predict the user who is going to leave in order to offer him a great discount before canceling the subscription.

I need to create a binary classifier based data thad Udacity provided. It's a large dataset of simulated Sparkify user activity logs. Due to the size of the dataset, the project  implemented using Apache Spark and Python API for Spark, PySpark.

The full Sparkify dataset is 12 GB. Due to its size, this could not be done locally, so an Elastic MapReduce (EMR) cluster was deployed to perform tasks in the AWS cloud.

#### Cluster configurations:
Release label: emr-5.30.1

Applications: Spark 2.4.5, Zeppelin 0.8.2

Instance type: m5.xlarge

Number of instances: 5 (1 master and 4 core nodes)

A post for this project is on [Medium](https://victorysharaf.medium.com/sparkify-churn-prediction-with-pyspark-on-big-data-c50157ee491c).

### Files Descriptions
* __Sparkify_small.ipynb__ includes data preparation, analysis, visualization, and machine learning models for small dataset
* __Sparkify_full.ipynb__ includes data preparation, analysis, visualization, and machine learning models for full dataset
 
### Libraries use
  * [pandas](https://github.com/pandas-dev/pandas)
  * [numpy](https://github.com/numpy/numpy)
  * [matplotlib](https://github.com/matplotlib/matplotlib)
  * [seaborn](https://github.com/mwaskom/seaborn)
  * [PySpark](https://spark.apache.org/docs/latest/api/python/index.html)
  
### Results
##### Baseline
Accuracy: 0.773
F-1 Score: 0.674
Total training time: 0.0 minutes

##### Logistic Regression
Accuracy: 0.778
F-1 Score: 0.691
Total training time: 41.2 minutes

##### Random Forest
Accuracy: 0.875
F-1 Score: 0.861
Total training time: 54.6 minutes

##### Gradient Boosted Trees
Accuracy: 0.857
F-1 Score: 0.84
Total training time: 133.4 minutes

##### Support Vector Machine
Accuracy: 0.773
F-1 Score: 0.674
Total training time: 40.5 minutes

Available memory: 11171M
Total training time 5.26 hours

The best model is **Random Forest**.

### Acknowledgements
Credit to [Udacity](udacity.com) for the data.
  
### Licensind
Apache License 2.0

See the LICENSE file for details
