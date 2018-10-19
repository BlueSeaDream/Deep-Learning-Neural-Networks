
# How to Train Your CNN Dragon

### Guo Dong

![how to train your dragon](https://user-images.githubusercontent.com/30903837/46021445-47539700-c113-11e8-8008-434dc0b1fe5f.jpg)

The training of CNN networks are often joked as alchemy. It makes sense in the way of mistry converage 

## Hyperparameters

In CNN network training, Hyperparameters are variables related to network structure and determine the training.

Hyperparameters are the variables which determines the network structure(Eg: Number of Hidden Units) and the variables which determine how the network is trained(Eg: Learning Rate).

Hyperparameters are set before training(before optimizing the weights and bias).

Hyperparameters related to Network structure

- Number of hidden layers and units
- Dropout
- Activation function

Hyperparameters related to training

- Learning Rate
- Momentum
- Number of epochs
- Batch size

## Hyperparameters

Hyperparameters are variables that define the network structure and determine the training.

Hyperparameters are the variables which determines the network structure(Eg: Number of Hidden Units) and the variables which determine how the network is trained(Eg: Learning Rate).

Hyperparameters are set before training(before optimizing the weights and bias).

Hyperparameters related to Network structure
Number of Hidden Layers and units
Dropout
Activation function

Hyperparameters related to Training Algorithm
Learning Rate
Momentum
Number of epochs
Batch size

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

# 37 Reasons why your Neural Network is not working

https://blog.slavv.com/37-reasons-why-your-neural-network-is-not-working-4020854bd607


# 38 caffe中怎么固定前面的网络参数，训练后面层的参数
1、会更新，finetune的过程相当于继续训练，跟直接训练的区别是初始化的时候：
a. 直接训练是按照网络定义指定的方式初始化（如高斯随机初始化）
b. finetune是用你已经有的参数文件来初始化（就是之前训练好的caffemodel）
2、嗯，这个问题有两种情况：比如有4个全连接层A->B->C->D
a. 你希望C层的参数不会改变，C前面的AB层的参数也不会改变，这种情况也就是D层的梯度不往前反向传播到D层的输入blob（也就是C层的输出blob 没有得到梯度），你可以通过设置D层的propagate_down为false来做到。
propagate_down的数量与输入blob的数量相同，假如你某个层有2个输入blob，那么你应该在该layer的Param里面写上两行：
propagate_down : 0 # 第1个输入blob不会得到反向传播的梯度
propagate_down : 0 # 第2个输入blob不会得到反向传播的梯度
这样的话，你这个layer的梯度就不会反向传播啦，前面的所有layer的参数也就不会改变了
b. 你希望C层的参数不会改变，但是C前面的AB层的参数会改变，这种情况，只是固定了C层的参数，C层得到的梯度依然会反向传播给前面的B层。只需要将对应的参数blob的学习率调整为0：
你在layer里面加上param { lr_mult: 0 }就可以了，比如全连接层里面：
layer {
type: "InnerProduct"
param { # 对应第1个参数blob的配置，也就是全连接层的参数矩阵的配置
lr_mult: 0 # 学习率为0，其他参数可以看caffe.proto里面的ParamSpec这个类型
}
param { # 对应第2个参数blob的配置，也就是全连接层的偏置项的配置
lr_mult: 0 # 学习率为0
}
}

Caffe学习笔记--如何创建自定义Layer

https://zhuanlan.zhihu.com/p/25484850

/aiml/g00391176/EV200/one_stg_obj_det/caffe/src/caffe/proto/

Note: must erase the original built and rebuild everything from the scratch.


# Caffe中Layer参数的初始化方式

https://blog.csdn.net/wenlin33/article/details/53378613

在Caffe的学习或者使用过程中，我们常会使用到prototxt文件。我们经常用prototxt来写整个深度学习模型的架构还有一些训练是需要用到的超参数。而在prototxt关于模型的某些Layer的描述中，我们经常会见到关于weight_filler和bias_filler的相关描述。 
如caffe中mnist的prototxt文件中关于conv_layer描述：

  layer {
  name: "conv1"
  type: "Convolution"
  bottom: "data"
  top: "conv1"
  param {
    lr_mult: 1
  }
  param {
    lr_mult: 2
  }
  convolution_param {
    num_output: 20
    kernel_size: 5
    stride: 1
    weight_filler {
      type: "xavier"
    }
    bias_filler {
      type: "constant"
    }
  }

还有innerproduct_layer的描述：

layer {
  name: "ip2"
  type: "InnerProduct"
  bottom: "ip1"
  top: "ip2"
  param {
    lr_mult: 1
  }
  param {
    lr_mult: 2
  }
  inner_product_param {
    num_output: 10
    weight_filler {
      type: "xavier"
    }
    bias_filler {
      type: "constant"
    }
  }
}

大家可以看到，这些层都涉及到了层参数初始化的有关设置。而这些都与Caffe中的Filler有关。Fillers是caffe用特定算法随机生成的值来填充网络参数在blob里面的初始值。它只作用在参数的初始化阶段，与gpu无关的操作。下面我们将一一介绍caffe中layer参数初始化的类型及其初始化的方式。 
这里我们先上proto上关于FillerParameter的数据结构描述，对应的Caffe源码的头文件为filler.hpp。

message FillerParameter {
  // The filler type.
  optional string type = 1 [default = 'constant'];
  optional float value = 2 [default = 0]; // the value in constant filler
  optional float min = 3 [default = 0]; // the min value in uniform filler
  optional float max = 4 [default = 1]; // the max value in uniform filler
  optional float mean = 5 [default = 0]; // the mean value in Gaussian filler
  optional float std = 6 [default = 1]; // the std value in Gaussian filler
  // The expected number of non-zero output weights for a given input in
  // Gaussian filler -- the default -1 means don't perform sparsification.
  optional int32 sparse = 7 [default = -1];
  // Normalize the filler variance by fan_in, fan_out, or their average.
  // Applies to 'xavier' and 'msra' fillers.
  enum VarianceNorm {
    FAN_IN = 0;
    FAN_OUT = 1;
    AVERAGE = 2;
  }
  optional VarianceNorm variance_norm = 8 [default = FAN_IN];
}

从上面我们可以看到有关的filler参数及其默认值。如默认filler填充类型为constant，value默认值为0，xavier和msra的VarianceNorm类型默认为FAN_IN等等。重点注意下sparse这个参数，它标志着初始化的数据有没有稀疏性。

Constant 
作用：默认将Blob系数x初始化为0。如果定义了value的值value = a，则x = a。（不支持sparse）

Gaussian 
作用：默认将Blob系数x初始化为满足mean=0，std=1的高斯分布x∼N(mean,std2)x∼N(mean,std2)。mean和std的值可自定义，支持sparse。

Positive_unitball 
作用：默认将Blob系数x初始化为满足x∈[0,1]x∈[0,1]，∀i∑jxij=1∀i∑jxij=1.（不支持sparse）

Uniform 
作用：默认将Blob系数x初始化为满足min=0,max=1的均匀分布。x∼U(min,max)x∼U(min,max)（不支持sparse）

Xavier（不适用于inner product layers.） 
作用：默认将Blob系数x初始化为满足x∼U(−a,+a)x∼U(−a,+a)的均匀分布， 其中 aa = sqrt(3 / n)。（不支持sparse） 
假设输入blob的shape为（num, a, b, c）。对于n的取值，下面分三种情况：
FAN_IN: 默认为这种类型。该类型下，n = a * b * c
FAN_OUT: n = num * b * c
AVERAGE: n = ( FAN_IN + FAN_OUT )/2 
参考paper [Bengio and Glorot 2010]: Understanding the difficulty of training deep feedforward neural networks.

Msra（不适用于inner product layers.） 
作用：默认将Blob系数x初始化为满足x∼N(0,σ2)x∼N(0,σ2)的高斯分布，其中σσ =sqrt(2 / n)。和Xavier一样，对于n的取值分为三种类型：
FAN_IN: 默认为这种类型。该类型下，n = a * b * c
FAN_OUT: n = num * b * c
AVERAGE: n = ( FAN_IN + FAN_OUT )/2 
参考paper [He, Zhang, Ren and Sun 2015]: Specifically accounts for ReLU nonlinearities.

Bilinear 
作用：一般用在deconvolution 层做upsampling，例子如下：

layer {
  name: "upsample", type: "Deconvolution"
  bottom: "{{bottom_name}}" top: "{{top_name}}"
  convolution_param {
    kernel_size: {{2 * factor - factor % 2}} stride: {{factor}}
    num_output: {{C}} group: {{C}}
    pad: {{ceil((factor - 1) / 2.)}}
    weight_filler: { type: "bilinear" } bias_term: false
  }
  param { lr_mult: 0 decay_mult: 0 }
}

轻量化神经网络综述
https://cloud.tencent.com/developer/article/1348098


