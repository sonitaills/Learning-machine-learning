# Learning-machine-learning

This repository will be used for studying the machine learning free course from Cornell University. The idea is to create an overview of the entire content and add more discoveries and thoughts on each topic. 

In each section header, there will be a link to the code used on each specific lecture

[Youtube free videos available here](https://www.youtube.com/watch?v=vcE9WGbi4QY)

[Kuleshov repository](https://github.com/kuleshov/cornell-cs5785-applied-ml)


## Summary

Lecture 1

Lecture 2

    Supervised Learning

    ??????

    Anatomy of Supervised Learning: Learning Algorithms


### Supervised Learning
-------------------------------------------------------------------------------------------------------------------

### [Anatomy of Supervised Learning: Learning Algorithms (code)](https://github.com/sonitaills/Learning-machine-learning/blob/main/Lecture%202%20part%203%20-%20Anathomy%20of%20supervised%20learning.ipynb) 

### [Lecture link](https://www.youtube.com/watch?v=PED1OYvQUX4)
-------------------------------------------------------------------------------------------------------------------

#### Overview

This lecture uses all the information (columns) on the training dataset to provid an estimation of diabetes risk

**Used functions:**

- **linearmodel.LinearRegrression**
- **regr.fit**
- **regr.predict** 

Supervised learning consists of 3 components:

- **Dataset** --> Data to train the model and test its performance

- **Algotithm** --> Subdivided into Model Class + Objective + Optimizer

  - Model Class: Set of possible models to consider. It can have just one or several parameters that maps inputs to outputs. A linear approach is an example of a model: (**y = ax + by + cz**)

  - Objective: function, which defines how good a model is, also known as loss function. Mean squared error and absolute error are examples of objective functions

  - Optimizer: Finds the best predictive model class, according to the objective function. It will work as choosing the model that will produce, for example, the least value on mean squared error

- **Predictive Model** --> Chosen to model relationship between inputs and targets

