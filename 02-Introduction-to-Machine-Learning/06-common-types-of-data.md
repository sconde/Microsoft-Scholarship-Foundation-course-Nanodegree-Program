Common Types of Data
====================

It's All Numerical in the End
-----------------------------

Note that although we've described _numerical data_ as a distinct category, it is actually involved in some way with all of the data types we've described. With the example of stock performance (above) the stock prices are numerical data points. So why do we give this as an example of "time-series data" rather than "numerical data"? It is the ordering of the numerical data points _across points in time_ that leads us to call the data _time-series data_.

What is more, all data in machine learning eventually ends up being numerical, regardless of whether it is numerical in its original form, so it can be processed by machine learning algorithms.

For example, we may want to use gender information in the dataset to predict if an individual has heart disease. Before we can use this information with a machine learning algorithm, we need to transfer male vs. female into numbers, for instance, 1 means a person is male and 2 means a person is female, so it can be processed. Note here that the value 1 or 2 does not carry any meaning.

Another example would be using pictures uploaded by customers to identify if they are satisfied with the service. Pictures are not initially in numerical form but they will need to be transformed into [RGB values](https://en.wikipedia.org/wiki/RGB_color_model#Numeric_representations), a set of numerical values ranging from 0 to 255, to be processed.

### Question 1 of 2

Have a look at this graph:

![](https://video.udacity-data.com/topher/2020/April/5e936285_1000px-population-of-greece-since-1961.svg/1000px-population-of-greece-since-1961.svg.png)

[Population of Greece since 1961 (_Wikimedia Commons_)](https://commons.wikimedia.org/w/index.php?title=File:Population_of_Greece_since_1961.svg&oldid=176669906)

What type of data is this?

- [ ] Numerical
- [x] Time-Series
- [ ] Categorical
- [ ] Text
    
> The graph shows data points given across an ordered series of times—thus, it is time-series data.

### Question 2 of 2

Have a look at this chart showing the number of people who like each flavor of ice cream:

![Pie chart of favorite ice cream flavors.](https://video.udacity-data.com/topher/2020/April/5e9361b5_ice-cream-flavors-pie-chart/ice-cream-flavors-pie-chart.png)

What type of data is this?

- [ ] Numerical
- [ ] Time-Series
- [x] Categorical
- [ ] Text

> You are correct that this contains numerical data. But it is not just numerical data— it is numerical data that is divided into groups or categories.
