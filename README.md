# Churn Prediction with PySpark

### Motivation
Sparkify is a fake music streaming service invented by Udacity. Here users can listen to music for free (with ads between songs) or for a flat fee. Users can upgrade, downgrade, or cancel. My task is to predict the user who is going to leave in order to offer him a great discount before canceling the subscription.

I need to create a binary classifier based data thad Udacity provided. It's a large dataset of simulated Sparkify user activity logs. Due to the size of the dataset, the project  implemented using Apache Spark and Python API for Spark, PySpark.

The full Sparkify dataset is 12 GB. Due to its size, this could not be done locally, so an Elastic MapReduce (EMR) cluster was deployed to perform tasks in the AWS cloud.

#### Cluster configurations:
Release label: emr-5.30.1
Applications: Spark 2.4.5, Zeppelin 0.8.2
Instance type: m5.xlarge
Number of instances: 3 (1 master and 2 core nodes)

A post for this project is on [Medium](https://victorysharaf.medium.com/sparkify-churn-prediction-with-pyspark-on-big-data-c50157ee491c).

### Files Descriptions
* __Sparkify_small.ipynb__ includes data preparation, analysis, visualization, and machine learning models for small dataset
* __Sparkify_full.ipynb__ includes data preparation, analysis, visualization, and machine learning models for full dataset
 
### Libraries use
  * [pandas](https://github.com/pandas-dev/pandas)
  * [numpy](https://github.com/numpy/numpy)
  * [matplotlib](https://github.com/matplotlib/matplotlib)
  * [seaborn](https://github.com/mwaskom/seaborn)
  * [PySpark](https://www.payspark.com/)
  
### Results
Performance ranking by F1:

Random Forest has F1 score 0.857, Accuracy 0.872

Gradient Boosted Trees has F1 score 0.850, Accuracy 0.848

Support Vector Machine has F1 score of 0.674, Accuracy 0.773

### Acknowledgements
Credit to [Udacity](udacity.com) for the data.
  
### Licensind
Apache License 2.0

See the LICENSE file for details
