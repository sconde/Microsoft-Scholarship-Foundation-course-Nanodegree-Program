Models vs. Algorithms
---------------------

In machine learning, the key distinction of a model and an algorithm is:

> **Models** are the **specific representations** learned from data
> 
> **Algorithms** are the processes of **learning**

We can think of the algorithm as a function—we give the algorithm data and it produces a model:

> Model\=Algorithm(Data)Model = Algorithm(Data)Model\=Algorithm(Data)

On the next page, we'll look at this distinction in the context of a concrete example: Linear regression.

More About Machine Learning Algorithms
--------------------------------------

We can think of an algorithm as a mathematical tool that can usually be represented by an equation as well as implemented in code. For example, `y = Wx + b` is an algorithm that can be used to calculate y from x if the values for `W` and `b` are known. But how do we get `W` and `b`?

This is the _learning_ part of machine learning; That is, _we can learn these values from training data_. For example, suppose the following data are collected:

| x   | y   |
| --- | --- |
| 1   | 1   |
| 2   | 2   |
| 3   | 3   |


We can plug the data into the algorithm and calculate `W = 1` and `b = 0`. We would say that that the _algorithm was run on the data and learned the values ofr `W` and `b`_. The output of the learning process is `W = 1` and `b = 0`.

Machine Learning Models
-----------------------

Machine learning models are _outputs_ or _specific representations_ of algorithms that run on data. A model represents _what is learned_ by a machine learning algorithm on the data.

In the previous example, `y = 1*x + 0` is the model we obtained from running the algorithm `y = Wx + b` on the training data. We can also say that `y = 1*x + 0` is the model that can be used to predict `y` from `x`.

A machine learning model can also be written in _a set of weights or coefficients_ instead of a full equation. Looking at the previous example, since we know the algorithm, it is redundant to keep the full equation `y = 1*x + 0`. All we need are the weights (or coefficients) `W = 1` and `b = 0`. Thus, we can also think of a model as a set of weights (or coefficients) that have been learned.

### Quiz Question

Which of these are examples of **algorithms** and which are examples of **models**?

Algorith: 
Least Squares Linear Regression

Algorith: 
Convolutional neural network

model: 
Set of coefficients

model: 
An equation learned from data

