
# Architectural Basics
## Readme-Assignment-4       
The order in which I considered the 24 points in my experiments is as follows:
1.Receptive Field
2.Kernels and how do we decide the number of kernels?
3.How many layers
4.3x3 Convolutions,
5.Concept of Transition Layers,
6.1x1 Convolutions,
7.MaxPooling,
8.Position of Transition Layer,
9.Position of MaxPooling,
10.The distance of MaxPooling from Prediction,
11.Image Normalization,
12.SoftMax,
13.Learning Rate,
14.Batch Normalization,
15.DropOut
16.Batch Size, and effects of batch size
17.Adam vs SGD
18.The distance of Batch Normalization from Prediction,
19.When do we introduce DropOut, or when do we know we have some overfitting,
20.Number of Epochs and when to increase them,
21.When do we stop convolutions and go ahead with a larger kernel or some other alternative (which we have not yet covered)
22.LR schedule and concept behind it
23.How do we know our network is not going well, comparatively, very early
24.When to add validation checks

25. Hardware limitations (needs to be considered before deciding no of kernels).

##Thoughts:
The first thought that comes to the mind once we know the size of the images in our dataset
is that by the time we reach our prediction layer our model,s receptive field should be equal to the image size.
once this rule is set the next more flexible rule to put in place is that we move to transition layers (1x1 and Maxpool) at around the receptive field 
when edges and gradients are formed & we gradually increase the number of kernels upto this layer. Since Maxpooling leads to data loss we avoid using it near 
the prediction layer. Now that we have a rough outline of our network architecture we will focus on our hyperparameters- Learning rate, Batch norm, batch size, dropout
optimizer, epochs etc. we set these parameters keeping in mind its effect on various parameters of the network. Once we start training we monitor its performance and
ensure that the model isn't overfitting (ie, rise in test accuracy with epochs but drop in valid_accu. In such cases we increase the dropout proportionately).

