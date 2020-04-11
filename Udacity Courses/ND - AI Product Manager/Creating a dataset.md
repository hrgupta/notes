# Creating a dataset

## Lesson 1 - Data Fit and Annotation

As mentioned in the previous lessons it is really important to have good quality data in order to solve business questions.

![Data Use](Creating&#32;a&#32;Dataset/Data&#32;Use.png)

The following questions need to be addressed in order to create quality dataset.

![Dataset](Creating&#32;a&#32;Dataset/Dataset.png)

How a model performs heavily depends on the training data we give it. One factor to look for is whether we have good enough data.

![Data Size](Creating&#32;a&#32;Dataset/Data&#32;Size.png)

### Garbage in, Garbage out

    "In computer science, garbage in, garbage out (GIGO) describes the concept that flawed, or nonsense input data produces nonsense output or 'garbage'."

### Data Size

Deep learning (neural networks) often need to see many examples of every possible category before they can learn to distinguish between different classes of data and find general patterns in some data. If you have too few data points or your data is not evenly distributed between different categories that you want to distinguish, you could get some significant sampling bias in your end predictions; predictions that are biased towards classifying all data into one class, for example, or predictions that have learned to find patterns that are irrelevant to the task at hand.

### Data Distribution and Pattern Detection

* Credit card fraud detection: most credit card transactions are valid, and so these datasets often have thousands of valid examples and very few examples of fraudulent transaction data, so you'd need to take steps to account for this imbalance otherwise a model will likely learn to classify all new data as valid since that is the most likely choice.
* You might think of building a classifier to distinguish wolves from dogs. If all wolves are images with a snowy background, a machine learning model might mistakenly conflate snow with wolves, and you'll need more, varied data to create an accurate model.

![Wolf-Dog classify](Creating&#32;a&#32;Dataset/Wolf-dog&#32;classify.png)

### Data Fit

In order to solve real world problems we need to make sure that our data represents real world which ensures that we have a good data fit for our business problem.

![Data Fit](Creating&#32;a&#32;Dataset/Data&#32;Fit.png)

Confusion Matrix is one of ensuring a good data fit. A confusion matrix displays the number of true positives, true negatives, false positives, and false negatives given some number of input data points n.

The accuracy, for example, will be the number of true positives + true negatives divided by the total number of data points.

![Confusion Matrix](Creating&#32;a&#32;Dataset/Confusion&#32;Matrix.png)

#### Precision & Recall

Precision and recall are just different metrics for measuring the "success" or performance of a trained model.

* precision is defined as the number of true positives (truly fraudulent transaction data, in this case) over all positives, and will be the higher when the amount of false positives is low.

* recall is defined as the number of true positives over true positives plus false negatives and will be higher when the number of false negatives is low.

Both take into account true positives and will be higher for high, positive accuracy, too.

It is helpful to visualize them as below:

![Precision and Recall](Creating&#32;a&#32;Dataset/Precision&#32;and&#32;Recall.png)

In many cases, it may be worthwhile to optimize for a higher recall or precision, which gives you a more granular look at false positives and negatives.

### Data Collection and Relevance

During Data collection, it is necessary to look whether the data we are collecting is relevant to the problem being solved. Also looking at data collection techniques used for similar problems might be useful.

### Data Completeness

In order to solve an ML problem, in addition to data relevancy, we also need to make sure that the data we have is complete.

![Data Completeness](Creating&#32;a&#32;Dataset/Data&#32;Completeness.png)

### Data Annotation

The goal of data annotation is to bring about you from unstructured, to a desired, labeled output.

### Annotation Instructions

Annotation instructions and examples are meant to set human annotators up for success. As such, it is important to be clear about the goal of the data annotation and all of the cases that annotators might see.

Which two kinds of examples should you include in your instructions for any data annotation?

* At least one example for each possible data annotation
* Ambiguous or "tricky" annotation cases

### Summary

![Summary](Creating&#32;a&#32;Dataset/Summary.png)
