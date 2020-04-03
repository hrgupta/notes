# Intro to Machine Learning

## 1. Introduction

* This step of capturing patterns from data is called **fitting** or **training** the model. The data used to fit the model is called the **training data**.

* The details of how the model is fit (e.g. how to split up the data) is complex enough that we will save it for later. After the model has been fit, you can apply it to new data to **predict** prices of additional homes.

## 2. Building your Model

The steps to building and using a model are:

    Define: What type of model will it be? A decision tree? Some other type of model? Some other parameters of the model type are specified too.

    Fit: Capture patterns from provided data. This is the heart of modeling.
    
    Predict: Just what it sounds like
    
    Evaluate: Determine how accurate the model's predictions are.

* Many machine learning models allow some randomness in model training. Specifying a number for random_state ensures you get the same results in each run. This is considered a good practice.

* You use any number, and model quality won't depend meaningfully on exactly what value you choose.

## 3. Model Validation

* Many people make a huge mistake when measuring predictive accuracy. They make predictions with their training data and compare those predictions to the target values in the training data.

* Since models' practical value come from making predictions on new data, we measure performance on data that wasn't used to build the model.

* The most straightforward way to do this is to exclude some data from the model-building process, and then use those to test the model's accuracy on data it hasn't seen before. This data is called validation data.

## 4. Experimenting with different models

Here's the takeaway: Models can suffer from either:

    Overfitting: capturing spurious patterns that won't recur in the future, leading to less accurate predictions, or

    Underfitting: failing to capture relevant patterns, again leading to less accurate predictions.

We use validation data, which isn't used in model training, to measure a candidate model's accuracy. This lets us try many candidate models and keep the best one.

**Note:** Some or part of this document is a verbatim copy of the corresponding course at Kaggle.
