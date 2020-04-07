# Build a model

## Lesson 1 - Training and Evaluating a model

The following images shows the concepts that will be covered in this lesson.

![Concepts](Building&#32;a&#32;model/Concepts.png)

There are several models avaiable in ML but for this task we will be focusing on neural networks.

![Neural Networks](Building&#32;a&#32;model/Neural&#32;Networks.png)

### Overview of Modelling

#### Why Neural Networks?

Neural networks are made up of neurons, sometimes called nodes. One neuron is responsible for processing some input data and producing an output. This is modeled after the neurons in our brain, which process input signals and produce output signals. For a neural network that processes visual data, such as a set of images, these inputs will be either spatial information or color information. When these color components or shapes are combined, which happens inside a neuron in the form of an equation (ex. 0.5red and 0.5blue = 1*purple), it produces an output signal that can do something like help classify the initial input!

This explanation and the below gif, were taken from Cezanne Camacho's [blog post on neural networks](https://cezannec.github.io/Intro_Neural_Networks/)

![Neron](Building&#32;a&#32;model/neuron-in-out.gif)

A neuron in our brain, processing input signals and transforming them into an output signal.

### Activation Functions

Activation Funtions are functions we can use as decision boundaries to tell us whether or not we want to send a signal to subsequent layers of the network.

![Decision Threshold](Building&#32;a&#32;model/Decision&#32;Threshold.png)

Furthermore, activation functions allow us to send a range of values to the next function instead of a yes or no.

![Activation Functions](Building&#32;a&#32;model/Activation&#32;functions.png)

Choosing an activation function depends on the problem we are solving at hand. Step function (0/1 function) might be useful for solving binary classifcation tasks. One useful activation function which returns a range of values is **sigmoid fuction**.

![Activation Function](Building&#32;a&#32;model/Sigmoid&#32;Function.png)

Two other common functions are the ReLU and the Leaky ReLU functions. This simplify the activation function to a linear equation which allow for faster and less complex training. Teh general idea is that we don't pay much attention to the negative inputs which reduces the number of nodes that are activated therby simplying the network.

![ReLU and Leaky ReLU](Building&#32;a&#32;model/ReLU&#32;and&#32;Leaky&#32;ReLU.png)

These are the most commonly used activation functions and have been shown to generally perform best among the activation functions.

The image below shows other types of nodes or networks other than the perceptron.

![Other Nodes](Building&#32;a&#32;model/Other&#32;Nodes.png)

We might not need to know the specifics of these networks but must be aware that there are different types of nodes or networks that are specialsed for various use cases.

#### Backpropagation & Updating the Weights of a Network

As a neural network trains, it starts off randomly guessing appropriate weights and will often produce the incorrect outputs, with some error that can be measured as the difference between a model-output value and a true output label or value. For a model to improve, it needs a way to:

Identify the source of its error (which model weights are responsible for the error?)
Update those weights to a new, better value
The first step, of identifying the weights causing an output error, is referred to as **backpropagation**. Essentially, backpropagation looks at the output of a model and goes backwards through the nodes and layers of a network to find the source or error.

Then, there is a second step, **updating the weights** such that their value is either increased or decreased in response to the error they caused.

The cycle of backpropagation and updating weights continues until a model is trained or until it has sufficiently low error!

The below image shows the summary of overview of modelling.

![Overview](Building&#32;a&#32;model/Overview.png)

### Training Data

Training data is the currency of machine learning and is the basis for the learing component in ML. In Machine Learning, data is key to model performance and outcomes. If we want the model to understand a specific concept, it must be clearing represented in the data in order for the machine to learn it for the future. Furthermore bad quality data leads to bad models.

![Data in ML](Building&#32;a&#32;model/Data&#32;in&#32;ML.png)

In order to ensure a robust model, we must train it on all types of data it is likely to encounder in the future. The image below mentions key points to consider for training data.

![Training Data](Building&#32;a&#32;model/Training&#32;Data.png)

Make sure to include real world and diverse data for training.

![The Right Data](Building&#32;a&#32;model/The&#32;right&#32;data.png)

The image below mentions key points to characterize right data.

![Right data points](Building&#32;a&#32;model/Right&#32;Data&#32;points.png)

Next we will look into the common issues we face with training data.

![Common Issues](Building&#32;a&#32;model/Common&#32;Issues.png)

Next issue is when the real word data differs from the training data.

![Common Issues 2](Building&#32;a&#32;model/Common&#32;Issues&#32;2.png)

Other common issue is having mislabeled data.

![Common Issues 3](Building&#32;a&#32;model/Common&#32;Issues&#32;3.png)

Finally, we have the amount of data used to train our models.

![Common Issues 4](Building&#32;a&#32;model/Common&#32;Issues&#32;4.png)

There is no clear cut rule of how much data will we need to solve a problem as it depends on a lot of factors but we generally want to start with a few hundred examples for each target class and then scale up the amount of training data until we reached the desired accuracy.

The below images shows the summary for the training data.

![Training data summary](Building&#32;a&#32;model/Training&#32;Data&#32;summary.png)

### Model Evaluation

Some of the key points about model performance is mentioned below.

![Model Performance](Building&#32;a&#32;model/Model&#32;Performance.png)

To evaluate model performance we typically keep a separate evaluation data. This helps us simulate unseen data and check the performance of our model against it.

![Evaluation Data](Building&#32;a&#32;model/Evaluation&#32;Data.png)

#### Why are training and test data separate?

We use training data when a model is learning. In our cat/dog/gerbil example, this is the data a model can use to learn and find patterns that distinguish the different classes of images.

After training, we need a way to test how well a trained model generalizes. The idea is: we want a trained model to perform well on new inputs, that it hasn’t seen before. This is where test data becomes useful! Because a model hasn’t seen it during training, we can test it on this dataset and evaluate its performance.

We want to evaluate the performance of the model apart from total number of correct and incorrect predictions. we are also interested on how it performs across different classes.

Different model metrics are important to think about when you define ths "success" of an AI product, which is why we're reiterating the definitions of **precision**, **recall**, and **F1 score**, here.

![Evaluation Data - Metric](Building&#32;a&#32;model/Evaluation&#32;Data&#32;-&#32;Metric.png)

We will now see the definition of model precision.

![Model Precision](Building&#32;a&#32;model/Model&#32;Precision.png)

Let us calculate the model precision for one of the use cases.

![Model Precision - Calculation](Building&#32;a&#32;model/Model&#32;Precision&#32;-&#32;Calculation.png)

We will now move to see model recall.

![Model Recall](Building&#32;a&#32;model/Model&#32;Recall.png)

Now lets calcualte the model recall for the same use case.

![Model Recall - Calculation](Building&#32;a&#32;model/Model&#32;Recall&#32;-&#32;Calculation.png)

Based on the above calculations we can see that the perfomance of this model is poor.

A third measure which is also often use is F1-score. It combines precision and recall to produce and overall performance of the model.

![F1 - Score](Building&#32;a&#32;model/Model&#32;F1&#32;-&#32;Score.png)

Generally an F1 - Score anove .75 or .80 will be considered decent. However it will depend on the intended application and how the critical the perormance of the model is to the sucess of the product.

In our case, we got an F1-Score of 0.57 which indicates that our model definitely needs more training cycles to improve its performance.

Finally we can plot a confusion matrix to understand which are our problem cases and get an update on how we should update our model.

![Confusion Matrix](Building&#32;a&#32;model/Confusion&#32;Matrix.png)

The image below sums up the model evalution concepts.

![Model Evaluation Summary](Building&#32;a&#32;model/Model&#32;Evaluation&#32;Summary.png)

Now we move onto Transfer Learning and automated ML.

### Transfer Learning

**Transfer learning** is when we use the knowledge from an already trained network with a similar use case which is stores in the architecture of the network as well as the weights and adapt that to a new use case. Generally that requires different classes.

This allows us to develop models with significantly less data because the neural network can retain the knowledge it learned from previous training data, sometimes millions of data points and slightly tune parameters to fit our needs.

**Automated ML** takes this one step further by allowing us to build relatively robust and scalable models without much machine learning experience.

![Transfer Learning](Building&#32;a&#32;model/Transfer&#32;Learning.png)

#### Why does Transfer Learning Work?

In the example above, we are leveraging the weights of an existing classification network (one that classifies cats, dogs, rabbits, and horses); we're keeping the first few layers of this trained network then adding and tre-training a final classification layer to create a new classification network that identifies humans and birds.

But why are these first few layers useful?

Well, in the case of image classification, the first layers in a network are responsible for identifying general patterns in shape and color, such as simple lines and textures, that distinguish different classes of images; later layers identify more complex features such as eyes, ears, and feet. The earlier layers, because they identify simple patterns, will be relevant in any classification case (there will always be simple lines and colors that we can use to identofy different objects)! And that is why you can transfer learnings from earlier layers of one network to another.

### Automated ML

AutoML platforms work by bringing labeled data to the platform and they automatically train and tune the model to fit out use case.

![Automated ML](Building&#32;a&#32;model/Automated&#32;ML.png)

An added benefit of these services is that they will conduct neural architecture search on the back-end.

![NAS](Building&#32;a&#32;model/NAS.png)

So, now we have different options of build versus buy for building ML products.

![AML-CM](Building&#32;a&#32;model/AML&#32;vs&#32;CM.png)

The image below shows the summary points for AutoML and transfer learning.

![AML-TL Summary](Building&#32;a&#32;model/AML&#32;and&#32;TL&#32;summary.png)
