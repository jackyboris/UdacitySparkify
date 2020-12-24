## UdacitySparkify Overview
Sparkify is a digital music service similar to Spotify. Users in Sparkify either use a free tier which includes ads in between songs, or they can have the premium subscription, paid monthly, which does not have any ads. Users can upgrade, downgrade, or cancel their service at any time.

Our task in this project is to perform an analysis of the customers' data and come out with a customer churn predicting model. Here are the steps:

Clean data: fill the miss values, correct the data types, drop the outliers.
EDA: exploratory data to look at features, distributions, and correlation between columns.
Feature engineering: extract and found customer-features and customer-behavior-features; Implement standscaler on numerical features.
Train and measure models: logistic regression, linear svm classifier, decision tree and random forest classifier were used to train a baseline model and tuning a better model from best of them. It is worth mentioning that this data is unbalanced because of fewer churn customers, so we choose f1 score as a metric to measure models’ performance.
## Installation

- Python 3.6
- PySpark ML
- Jupyter

## Results

The baseline of four machine learning methods: Logistic Regression, Linear SVC, Decision Tree Classifier and Random Forest Classifier. 

| Model Name         | F1-score | Training Time(s) |
| ------------------ | -------- | ---------------- |
| Random Forest      | 0.700000	| 182.324425       |
| Logistic Regression| 0.428000	| 250.543468       |
| LinearSVC          | 0.445000	| 820.973378       |
| Decision Tree      | 0.647315	| 174.552133       |

Though the `RandomForest`, we can get the highest f1 score 0.700. Maybe I can tuning it to get a higher 
score. So I'll choose `Random Forest` to tuning, and the result is as follows:

| Model Name         | F1-score | Training Time(s) |
| ------------------ | -------- | ---------------- |
| Random Forest      | 0.6508   | 1422.96          |

Unfortunately, we get the lower f1score...... Let's just use the original one. We are happy to get 0.7.
Considering this is only a quit mini dataset and our purpose is scaling this up to the total 12G  dataset, so, the Random Forest is the best model from now on in this project.

Please check my blog post to get more details, here is the [link](https://jackyboris.blogspot.com/2020/12/sparkify-is-digital-music-service.html).

## References

Dataset provided by [Udacity](https://cn.udacity.com/).
