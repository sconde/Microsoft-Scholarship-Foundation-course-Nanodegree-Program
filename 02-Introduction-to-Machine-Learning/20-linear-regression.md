Linear Regression
=================

In our first lab, we're going to use Azure Machine Learning Studio to train a model using one of the fundamental machine learning algorithms: _Linear regression_. Before we dive into the lab, let's review what linear regression is and how it can be used to train a model.

The video below gives a brief review of the main concepts. If you've never seen linear regression before, or need a more thorough review, you can continue on for a detailed explanation below.

If you feel confident in your understanding of linear regression, feel free to move ahead to the next page and get started on the lab. Otherwise, we'll go over the concepts in further detail below.

Understanding Linear Regression
-------------------------------

> As the term suggests, **linear regression** is an _algorithm_ that uses a straight line (or plane) to describe relationships between variables.

Let's consider a very simple example of a linear relationship. Suppose that we want to know if the _number of hours a student spends studying for a test_ is related to the _number of questions answered correctly on the test_.

Such a relationship might look something like this:

![Graph showing a linear relationship.](https://video.udacity-data.com/topher/2020/May/5ebe8c0b_linear-relationship/linear-relationship.png)

We can see that there is a clear relationship: Students who spent more time studying also scored higher on the test.

What is more, we can see that the data points cluster around a straight line. Linear regression is all about finding the _line that best fits the data_. And this model (or line) can then be used to make predictions. In this case, if we know the number of hours a student has studied for the test, we can predict how many questions he or she can answer correctly. To make this prediction, we need the equation for the line of best fit. What would that look like?

Simple Linear Regression
------------------------

You may recall from fundamental algebra that the general equation for a line looks like this:

y\=mx+b y = m x + b y\=mx+b

Where mmm is called the _slope_ of the line, and _b_ is the y-intercept. Again, this is the _general_ equation. For a specific line, we need to know the values for the slope and y-intercept. For example, the following equations represent three different lines.

y\=10x+50 y = 10 x + 50 y\=10x+50

y\=2x+3 y = 2 x + 3 y\=2x+3

y\=−10x+40 y = -10 x + 40 y\=−10x+40

Equations like these can be used to make _predictions_. Once we know mmm and bbb , we can feed in a value for xxx and the equation will give us the value of yyy.

### Question 1 of 2

For the earlier example of students studying for a test, suppose that we find that the line of best fit is:

y\=15x+3 y = 15 x + 3 y\=15x+3

Where xxx is the number of hours studied and yyy is the number of questions correctly answered.

If a student studied 10 hours for the test, what is their predicted score?

- [ ] 48
- [ ] 148
- [x] 153
- [ ] 183

> If we plug the value 10 into the equation, we get:

> y = 15 *10 + 3 = 153y=15∗10+3=153

Submit

### Question 2 of 2

Thinking back to the _models vs. algorithms_ distinction, is our equation…

y\=15x+3 y = 15 x + 3 y\=15x+3

…best described as a **model** or an **algorithm**?

- [x] y\=15x+3 y = 15 x + 3 y\=15x+3 is a model
- [ ] y\=15x+3 y = 15 x + 3 y\=15x+3 is an algorithm

> This specific line (with mm = 15 and b = 3) is a model that we got from combining the general equation y = m x + by=mx+b with the training data.

Linear Regression in Machine Learning
-------------------------------------

The equation we used above was:

y\=mx+b y = mx + by\=mx+b

In algebraic terms, we may refer to mmm as the **coefficient** of x or simply the **slope** of the line, and we may call bbb the **y-intercept**. In machine learning, you will typically see the y-intercept referred to as the **bias**. In machine learning, you will also often see the equation represented using different variables, as in:

y\=B0+B1∗x y = B\_0 + B\_1\*xy\=B0​+B1​∗x

The letters are different and the order has been changed, but it is exactly the same equation. Thus, we can see that what we know from algebra as the basic equation for a line is also, in machine learning, the equation used for **simple linear regression**.

Multiple Linear Regression
--------------------------

In more complex cases where there is _more than one_ input variable, we might see something like this:

y\=B0+B1∗x1+B2∗x2+B3∗x3...+Bn∗xn y = B\_0 + B\_1\*x\_1 + B\_2\*x\_2 + B\_3\*x\_3 ... + B\_n \*x\_ny\=B0​+B1​∗x1​+B2​∗x2​+B3​∗x3​...+Bn​∗xn​

In this case, we are using multiple input variables to predict the output. When we have _multiple_ input variables like this, we call it **multiple linear regression**. The visualization of multiple linear regression is no longer a simple line, but instead a _plane_ in multiple dimensions:

![Graph of multiple linear regression.](https://video.udacity-data.com/topher/2020/May/5eb4a3c3_screen-shot-2020-05-07-at-5.11.11-pm/screen-shot-2020-05-07-at-5.11.11-pm.png)

But don't let any of this intimidate you: The core idea is still that we are modeling a relationship (using a line or plane) in order to help us predict the value of some variable that we are interested in.

Training a Linear Regression Model
----------------------------------

To "train a linear regression model" simply means to learn the _coefficients_ and _bias_ that _best fit the data_. This is the purpose of the linear regression algorithm. Here we will give you a high-level introduction so that you understand conceptually how it works, but we will not go into the mathematical details.

### The Cost Function

Notice from our example of test scores earlier that the line we came up with did not _perfectly_ fit the data. In fact, _most_ of the data points were not on the line! When we predict that a student who studies for 10 hours will get a score of 153, we do not expect their score to be exactly 153. Put another way, when we make a prediction using the line, we expect the prediction to have some **error**.

The process of finding the best model is essentially a process of finding the coefficients and bias that _minimize_ this error. To calculate this error, we use a **cost function**. There are many cost functions you can choose from to train a model and the resulting error will be different depending one which cost function you choose. The most commonly used cost function for linear regression is the [**root mean squared error (RMSE)**](https://en.wikipedia.org/wiki/Root-mean-square_deviation)

### Preparing the Data

There are several [**assumptions**](https://www.jmp.com/en_us/statistics-knowledge-portal/what-is-regression/simple-linear-regression-assumptions.html) or conditions you need to keep in mind when you use the linear regression algorithm. If the raw data does not meet these assumptions, then it needs to be prepared and transformed prior to use.

*   **Linear assumption:** As we've said earlier, linear regression describes variables using a _line_. So the relationship between the input variables and the output variable needs to be a linear relationship. If the raw data does not follow a linear relationship, you may be able to [transform](https://en.wikipedia.org/wiki/Data_transformation_(statistics)) your data prior to using it with the linear regression algorithm. For example, if your data has an exponential relationship, you can use _log transformation_.
*   **Remove collinearity**: When two variables are **collinear**, this means they can be modeled by the same line or are at least highly _correlated_; in other words, one input variable can be accurately predicted by the other. For example, suppose we want to predict education level using the input variables `number of years studying at school`, `if an individual is male`, and `if an individual is female`. In this case, we will see collinearity—the input variable `if an individual is female` can be perfectly predicted by `if an individual is male`, thus, we can say they are highly correlated. Having highly correlated input variables will make the model less consistent, so it's important to perform a _correlation check_ among input variables and remove highly correlated input variables.
*   **Gaussian (normal) distribution:** Linear regression assumes that the distance between output variables and real data (called _residual_) is _normally distributed_. If this is not the case in the raw data, you will need to first transform the data so that the residual has a normal distribution.
*   **Rescale data:** Linear regression is very sensitive to the distance among data points, so it's always a good idea to _normalize_ or _standardize_ the data.
*   **Remove noise**: Linear regression is very sensitive to noise and _outliers_ in the data. Outliers will significantly change the line learned, as shown in the picture below. Thus, cleaning the data is a critical step prior to applying linear regression.

![Graph showing the sensitivity of linear regression to outliers.](https://video.udacity-data.com/topher/2020/May/5eb4b45d_screen-shot-2020-05-07-at-6.21.26-pm/screen-shot-2020-05-07-at-6.21.26-pm.png)

### Calculating the Coefficients

We've discussed here the overall concept of training a linear regression model: We take the _general_ equation for a line and use some data to learn the coefficients for a _specific line_ that will best fit the data. Just so that you have an idea of what this looks like in concrete terms, let's look at the formulas used to calculate the coefficients. We're showing these in order to give you a general idea of what the calculations actually involve on a concrete level. For this course, you do _not_ need to worry about how the formulas are derived and how to use them to calculate the coefficients.

The formula for getting the slope of the line looks something like this:

![Formula for calculating slope.](https://video.udacity-data.com/topher/2020/May/5ebea0c7_slope/slope.png)

To get the intercept, we calculate:

![Formula for calculating the intercept.](https://video.udacity-data.com/topher/2020/May/5ebea0f1_intercept/intercept.png)

And to get the _root mean squared error (RMSE)_, we have:

![Formula for calculating RMSE.](https://video.udacity-data.com/topher/2020/May/5ebea119_rmse/rmse.png)

In most machine learning libraries (such as Sklearn or Pythorch) the inner workings of the linear regression algorithm are implemented for you. The error and the best coefficients will be automatically calculated when you input the data. Here, the important thing is to understand what is happening conceptually—namely, that we choose a cost function (like RMSE) to calculate the _error_ and then _minimize_ that error in order to arrive at a _line of best fit_ that models the training data and can be used to make predictions.

Now that we've review the concept, let's get some hands-on practice implementing the linear regression algorithm in Azure Machine Learning Studio!
