# mlfs-book
O'Reilly book - Building Machine Learning Systems with a feature store: batch, real-time, and LLMs


## ML System Examples


[Dashboards for Example ML Systems](https://ivwhy.github.io/mlfs-book/air-quality/)

## Course Comparison

| Course                         | MLOps | LLLMs             | Feature/Training/Inference | Working AI Systems | Focus |
|--------------------------------|-------|----------------------------|--------------------|------------------|
| Building AI Systems (O'Reilly) | Yes   | Fine-Tuning & RAG | Yes                        | High               | Project-based, Software Engineering, Fundamentals    |
| [Made With ML](https://madewithml.com/)                   | No          | Yes   | No                         | No                 | Software Engineering, Model Training   |
| [7 Steps MLOps](https://www.pauliusztin.me/courses/the-full-stack-7-steps-mlops-framework)            | Yes   | Separate Course    | Yes                        | Low                | Learning Tools and Project    |

## Lab Description

1. Write a backfill feature pipeline that downloads historical weather data (ideally >1
year of data), loads a csv file with historical air quality data (downloaded from
https://aqicn.org) and registers them as 2 Feature Groups with Hopsworks.
2. Schedule a daily feature pipeline notebook that downloads yesterday’s weather
data and air quality data, and also the weather prediction for the next 7-10 days
and update the Feature Groups in Hopsworks. Use GH Actions or Modal.
3. Write a training pipeline that (1) selects the features for use in a feature view, (2)
reads training data with the Feature View, trains a regression or classifier model to
predict air quality (pm25). Register the model with Hopsworks.
4. Write a batch inference pipeline that creates a dashboard. The program should
download your model from Hopsworks and plot a dashboard that predicts the air
quality for the next 7-10 days for your chosen air quality sensor.
5. Monitor the accuracy of your predictions by plotting a hindcast graph showing
your predictions vs outcomes (measured air quality).
6. Update your Model by adding a new feature, lagged air quality for the previous 1-3
days.
