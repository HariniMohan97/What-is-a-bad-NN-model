# Session2
Why I think this is a bad model?
1) We can see that from the last layer, we can't see the whole image, i.e, the receptive field is less than the size of the image. This is not a good thing to have since its a loss of info and features.
2) In the model,the number of kernals used has been drastically increased after the maxpooling layer. This increases the number of parameters and hence the model takes forever to train. And we are really close to getting an OOM!
3) We can also see that the number of output channels has been drastically brought down to 10 from 2048! This is a very bad practice since theres a very large amount of information loss when we try squeezing so much into so less!
4) Applying a softmax layer at the end can sometimes screw up our results as well. Softmax returns a set of final numbers that add up to probability of 1. So this might not necessarily always work to our advantage.
Overall, we just tortured the model and made it get really confused!Because of which the learning is very slow and the decrease in loss is very less with every epoch.
