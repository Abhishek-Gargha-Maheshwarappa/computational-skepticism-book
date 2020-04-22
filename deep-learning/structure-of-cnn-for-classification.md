# Structure of CNN for classification



![Structure of CNN](https://lh3.googleusercontent.com/gOucczLBnWcIfpuVxTM-whsW1w7MJekPLH293Qs0UdhHyebI0JgQ_wCtjyVQlQhM46yiiOuXAr2sabXMRJDraLdarTPRrF1LUTbgyfAa2hyusZVxlWq91hBtn-bPR9bwqRDSelaN)

Image is fed to the convolution network with filters which help to learn features of the input image. Then a non linearity is introduced through activation function since the real world data is nonlinear. Then dimensional reduction is applied by pooling.This process is repeated for required number times and finally it feeds to a fully connected network.The fully connected network may contain hidden layers and based on the output we use a particular activation function.

This notebook does not deal with explanation of Deep Learning or Computer vision. There are a lot of books and tutorials which explain these techniques in detail. This notebook basically concentrates on how the CNN model does classification, how it will make its decision, what are the basis for making a decision.  
  


