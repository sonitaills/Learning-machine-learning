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

Lecture 3
    Optimization and Calculus

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
-------------------------------------------------------------------------------------------------------------------

### [Optimization and Calculus (code)](https://github.com/sonitaills/Learning-machine-learning/blob/main/Lecture%203%20-%20part%201%20-%20Optimization%20and%20Calculus.ipynb) 

### [Lecture link](https://www.youtube.com/watch?v=E5hU0AesA-I)
-------------------------------------------------------------------------------------------------------------------

#### Overview

Main goal is to explain how gradient descent (steepest descent) optimizer works. Recap on derivatives and some cool functions to plot derivatives graphs.
Step size in gradient descent algorithm dictates how "far down" you want to go. If the step size is too short, more iterations will be needed and optimum solution
may not be achieved. If it is too high, it might cause an overshoot and as well bot be able to achieve the optimum solution. Solution is reached when the error between the 
previous step and the new one is lower than a threshold

![image](https://user-images.githubusercontent.com/46113694/125006266-13339180-e034-11eb-8c6b-4db740c968a4.png)

**Used functions:**

### [Gradient Descent (code)](https://github.com/sonitaills/Learning-machine-learning/blob/main/Lecture%203%20part%202%20-%20Gradient%20descent.ipynb) 

### [Lecture link](https://www.youtube.com/watch?v=B3w5Zzuqi-E&t=2s)
-------------------------------------------------------------------------------------------------------------------

#### Overview
Uses UCI diabetes training data from sklearn. From this data a supervised learning model is defined

- Model family: here it will be the linear model. The relationship between the targets and all the inputs is linear

![image](https://user-images.githubusercontent.com/46113694/125005013-1c6f2f00-e031-11eb-96c0-2f96e38a1b40.png)

- Objective function: Mean squared error

- Optimizer: Gradient descent is used. To apply it, it is necessary to know how to differentiate the ojective function!

**Obs: Since linear models can also have a constant, a column consisting of only values 1 is added to data! This will generate an output paramenter that will be a constant when multiplied by the variable matrix**

![image](https://user-images.githubusercontent.com/46113694/125009453-f51d5f80-e03a-11eb-973d-8541fb6dc3bd.png)


**Used functions:**


