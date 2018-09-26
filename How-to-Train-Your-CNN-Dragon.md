
# How to Train Your CNN Dragon

### Guo Dong

![how to train your dragon](https://user-images.githubusercontent.com/30903837/46021445-47539700-c113-11e8-8008-434dc0b1fe5f.jpg)

## Hyperparameters

Hyperparameters are variables that define the network structure and determine the training.

Hyperparameters are the variables which determines the network structure(Eg: Number of Hidden Units) and the variables which determine how the network is trained(Eg: Learning Rate).

Hyperparameters are set before training(before optimizing the weights and bias).

Hyperparameters related to Network structure
Number of Hidden Layers and units
Hidden layers are the layers between input layer and output layer.

“Very simple. Just keep adding layers until the test error does not improve anymore.”

Many hidden units within a layer with regularization techniques can increase accuracy. Smaller number of units may cause underfitting.

Dropout

Random neurons are cancelled
Dropout is regularization technique to avoid overfitting (increase the validation accuracy) thus increasing the generalizing power.

Generally, use a small dropout value of 20%-50% of neurons with 20% providing a good starting point. A probability too low has minimal effect and a value too high results in under-learning by the network.
Use a larger network. You are likely to get better performance when dropout is used on a larger network, giving the model more of an opportunity to learn independent representations.
Network Weight Initialization
Ideally, it may be better to use different weight initialization schemes according to the activation function used on each layer.

Mostly uniform distribution is used.

Activation function

Sigmoid activation function
Activation functions are used to introduce nonlinearity to models, which allows deep learning models to learn nonlinear prediction boundaries.

Generally, the rectifier activation function is the most popular.

Sigmoid is used in the output layer while making binary predictions. Softmax is used in the output layer while making multi-class predictions.

Hyperparameters related to Training Algorithm
Learning Rate

Learning rate
The learning rate defines how quickly a network updates its parameters.

Low learning rate slows down the learning process but converges smoothly. Larger learning rate speeds up the learning but may not converge.

Usually a decaying Learning rate is preferred.

Momentum
Momentum helps to know the direction of the next step with the knowledge of the previous steps. It helps to prevent oscillations. A typical choice of momentum is between 0.5 to 0.9.

Number of epochs
Number of epochs is the number of times the whole training data is shown to the network while training.

Increase the number of epochs until the validation accuracy starts decreasing even when training accuracy is increasing(overfitting).

Batch size
Mini batch size is the number of sub samples given to the network after which parameter update happens.

A good default for batch size might be 32. Also try 32, 64, 128, 256, and so on.



## 1. Hyper Parameter Setting

### 1.1 Learning Rate

**Learning Rate** is an critical hyper-parameter parameter in CNN network trainings, it adjusts the network weight based on training loss gradients. The lower the value, the slower we travel along the downward slope. While this might be a good idea (using a low learning rate) in terms of making sure that we do not miss any local minimum, it could also mean that we’ll be taking a long time to converge — especially if we get stuck on a plateau region.

The following formula shows the relationship.

```
new_weight = existing_weight — learning_rate * gradient
```



Typically learning rates are configured naively at random by the user. At best, the user would leverage on past experiences (or other types of learning material) to gain the intuition on what is the best value to use in setting learning rates.

As such, it’s often hard to get it right. The below diagram demonstrates the different scenarios one can fall into when configuring the learning rate.



#### 1. Shuffle the dataset

If your dataset hasn't been shuffled and has a particular order to it (ordered by label) this could negatively impact the learning. Shuffle your dataset to avoid this. Make sure you are shuffling input and labels together.

![learning_rate](D:\Books Papers Learning Materials\CNN\How to Train You CNN Dragon\learning_rate.png)



![dropout](D:\Books Papers Learning Materials\CNN\How to Train You CNN Dragon\dropout.gif)




# How to Train Your CNN Dragon



![learning rate](https://user-images.githubusercontent.com/30903837/46021465-50446880-c113-11e8-85ca-5edcdd3cfb8e.png)



Learning rate is a hyper-parameter that controls how much we are adjusting the weights of our network with respect the loss gradient. The lower the value, the slower we travel along the downward slope. While this might be a good idea (using a low learning rate) in terms of making sure that we do not miss any local minimum, it could also mean that we’ll be taking a long time to converge — especially if we get stuck on a plateau region.

The following formula shows the relationship.

```
new_weight = existing_weight — learning_rate * gradient
```



Typically learning rates are configured naively at random by the user. At best, the user would leverage on past experiences (or other types of learning material) to gain the intuition on what is the best value to use in setting learning rates.

As such, it’s often hard to get it right. The below diagram demonstrates the different scenarios one can fall into when configuring the learning rate.



#### 1. Shuffle the dataset

If your dataset hasn't been shuffled and has a particular order to it (ordered by label) this could negatively impact the learning. Shuffle your dataset to avoid this. Make sure you are shuffling input and labels together.

# How to Train Your CNN Dragon

## Guo Dong

![](/home/guo/Desktop/wallpaper2you_258317.jpg)

Deep neural networks like Covnet has a huge number of parameters, often in the range of millions. Training a Covnet on a small dataset (one that is smaller than the number of parameters) greatly affects the Covnet’s ability to generalize, often result in overfitting.

Therefore, more often in practice, one would fine-tune existing networks that are trained on a large dataset like the ImageNet (1.2M labeled images) by continue training it (i.e. running back-propagation) on the smaller dataset we have. Provided that our dataset is not drastically different in context to the original dataset (e.g. ImageNet), the pre-trained model will already have learned features that are relevant to our own classification problem.

Pre-trained network on a large and diverse dataset like the ImageNet captures universal features like curves and edges in its early layers, that are relevant and useful to most of the classification problems.



# caffe中weight_filler

https://blog.csdn.net/m0_37407756/article/details/72553284



Xavier Initialization



http://philipperemy.github.io/xavier-initialization/



# Caffe Initializers

https://jihongju.github.io/2017/05/10/caffe-filler/



# Understanding Xavier Initialization In Deep Neural Networks

https://prateekvjoshi.com/2016/03/29/understanding-xavier-initialization-in-deep-neural-networks/



# Caffe常用层参数介绍

https://blog.csdn.net/Cheese_pop/article/details/52024980



# 浅谈caffe中train_val.prototxt和deploy.prototxt文件的区别

https://blog.csdn.net/fx409494616/article/details/53008971



Understanding the difficulty of training deep feedforward neural networks

http://proceedings.mlr.press/v9/glorot10a/glorot10a.pdf



Cyclical Learning Rates for Training Neural Networks



EXPLORING LOSS FUNCTION TOPOLOGY WITH CYCLICAL LEARNING RATES

https://github.com/lnsmith54/exploring-loss



# **Improving the way we work with learning rate.**

https://techburst.io/improving-the-way-we-work-with-learning-rate-5e99554f163b



# Understanding Learning Rates and How It Improves Performance in Deep Learning

https://towardsdatascience.com/understanding-learning-rates-and-how-it-improves-performance-in-deep-learning-d0d4059c1c10



# A Comprehensive guide to Fine-tuning Deep Learning Models in Keras (Part I)

https://flyyufelix.github.io/2016/10/03/fine-tuning-in-keras-part1.html



# Setting the learning rate of your neural network.

https://www.jeremyjordan.me/nn-learning-rate/


An Overview of Regularization Techniques in Deep Learning (with Python code)

https://www.analyticsvidhya.com/blog/2018/04/fundamentals-deep-learning-regularization-techniques/


# What are Hyperparameters ? and How to tune the Hyperparameters in a Deep Neural Network?

https://towardsdatascience.com/what-are-hyperparameters-and-how-to-tune-the-hyperparameters-in-a-deep-neural-network-d0604917584a



