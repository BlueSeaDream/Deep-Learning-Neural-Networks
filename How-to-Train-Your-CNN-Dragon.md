# How to Train Your CNN Dragon


# How to Train Your CNN Dragon

![](D:\Books Papers Learning Materials\CNN\How to Train You CNN Dragon\How-To-Train-A-Dragon-Wallpapers-029.jpg)



Learning rate is a hyper-parameter that controls how much we are adjusting the weights of our network with respect the loss gradient. The lower the value, the slower we travel along the downward slope. While this might be a good idea (using a low learning rate) in terms of making sure that we do not miss any local minimum, it could also mean that we’ll be taking a long time to converge — especially if we get stuck on a plateau region.

The following formula shows the relationship.

```
new_weight = existing_weight — learning_rate * gradient
```



Typically learning rates are configured naively at random by the user. At best, the user would leverage on past experiences (or other types of learning material) to gain the intuition on what is the best value to use in setting learning rates.

As such, it’s often hard to get it right. The below diagram demonstrates the different scenarios one can fall into when configuring the learning rate.



#### 1. Shuffle the dataset

If your dataset hasn't been shuffled and has a particular order to it (ordered by label) this could negatively impact the learning. Shuffle your dataset to avoid this. Make sure you are shuffling input and labels together.

![learning_rate](D:\Books Papers Learning Materials\CNN\How to Train You CNN Dragon\learning_rate.png)



