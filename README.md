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
    
    Gradient Descent
    
    Ordinary Least Squares
    
    Non Linear Least Squares

Lecture 4 - Foundations of Supervised Learning

    The Data Distribution
    
     Why Does Supervised Learning Work?
     
     Overfitting and Underfitting


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

### [Ordinary Least Squares (code)](https://github.com/sonitaills/Learning-machine-learning/blob/main/Lecture%203%20part%203.pdf) 

### [Lecture link](https://www.youtube.com/watch?v=WIbgH6Nc-ac&t=2s)
-------------------------------------------------------------------------------------------------------------------

#### Overview

- Type: Supervised learning
- Model family: Linear models
- Objective function: Mean Squared Error
- Optmizer: Normal equations


To use this approach, the data must be presented in matrix form, knwon as a design matrix, where the lines represent the values of a single variable. 

The objective function used for the algorithm is the Mean Square Error (MSE). First, the function is presented in the matrix form. 

![image](https://user-images.githubusercontent.com/46113694/126000312-23f4672b-3dfe-403a-9098-130ca50865ec.png)

The theta values are the obtained from all the variables in the training data and later used to predict new answers. The MSE gradient can be found with:

![image](https://user-images.githubusercontent.com/46113694/126004014-cbeaf11e-997e-4c4a-8352-6f6d75903ba6.png)

By setting the derivatie of the MSE = 0 the optimum theta value will be achieved, and since the MSE is a quadratic function, it will have only one minimum. Note that for the below equation to work, the matrix XTX has to be invertible (determinant different than 0). Thera are though some ways of contourning this fact.

![image](https://user-images.githubusercontent.com/46113694/126004369-05bceeff-d856-40e1-96db-73f335d22626.png)

### [Non-Linear Least Squares (code)](https://github.com/sonitaills/Learning-machine-learning/blob/main/Lecture%203%20part%204.pdf) 

### [Lecture link](https://www.youtube.com/watch?v=aJzZmo9-cFk&list=PL2UML_KCiC0UlY7iCQDSiGDMovaupqc83&index=11)
-------------------------------------------------------------------------------------------------------------------

#### Overview

- Type: Supervised learning (regression)
- Model family: Linear models
- Features: Non-linear functions of the attributes
- Objective function: Mean Squared Error
- Optmizer: Normal equations

If your parameters theta are linear, it is possible to apply a non linear design matrix and use the ORDINARY LEAST SQUARE approach. These non-linear features can be of any kind. There is an endless range of functions that can be designes this way.

![image](https://user-images.githubusercontent.com/46113694/126046343-7b0d52cb-4638-428b-888d-5ba093e6ebe4.png)


**New used functions:**
- matplotlib subplot
- np.cos, np.sin

### [The data distribution (code)](https://github.com/sonitaills/Learning-machine-learning/blob/main/Lecture%203%20part%204.pdf) 

### [Lecture link](https://www.youtube.com/watch?v=eu2NKLVCJNA&list=PL2UML_KCiC0UlY7iCQDSiGDMovaupqc83&index=12)
-------------------------------------------------------------------------------------------------------------------

#### Overview

In order to apply supervised learning, we need the training dataset, the learning algotithm and then it is possible to find a predictive model. Where does the dataset come from?

Tipically the data is assumed to come from a probabilty distribution, called the data distribution. The training set is assumed to consist of **independet and identicaly distributed (IID)** samples from original distribution. When this assumption is met, it can be used to prove the algotithm will work in certain cases. If not met, it provides intuition on why some algorithms may not work.

    - Each training example iss from the same distribution
   
    -This distribution doesn't depend on previous training examples
    
**Example** --> Flipping a coin doesn't depend on previous results

**Counter-example** --> Yearly census data. The population in each year will be close to that of the previous year. This example violates the "independent" assumption

Why assume that the dateset is sampled from a distribution? 
    
    -There is inherent uncertainty in the data, which may consists of noisy measurements (reading from imperfect equipment). 
    - Uncertainty in the process being modeled. There is randomness in stock prices which can't be modeled
    - Usage of probability and statistics to analyse Supervide learning algorithms to prove they do or don't work
    
### [ Why Does Supervised Learning Work? (code)]() 

### [Lecture link](https://www.youtube.com/watch?v=eu2NKLVCJNA&list=PL2UML_KCiC0UlY7iCQDSiGDMovaupqc83&index=13)
------------------------------#### Overview-------------------------------------------------------------------------------------

#### Overview

A **good** model is one that makes accurate predictions on new data that it **has not seen at training time**. This is really important to remember! **DO NOT TEST THE MODEL ON THE TRAINING DATA**. 

For testing purposes, get some other samples from the data, unseen during the training part, and test the model versus the correct values. This new sample is called **hold-out** data.

![image](https://user-images.githubusercontent.com/46113694/126047865-56fab0ae-3a18-4ed4-893e-76a7d1c5bc97.png)

A supervised learning is **accurate** if  it predicts correctly the target on the new (hold-out) data, e.g if the probability of making an error on a random holdout sample is small

![image](https://user-images.githubusercontent.com/46113694/126047987-9300d53f-94fe-4a79-9caa-333d7185f14c.png)

**Generalization** is the property of predictive models to achiee good performance on new heldout data, distinct from the training set. In order for it to work, you must have enough data!
