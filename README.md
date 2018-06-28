# Neural Network Visualization in Javascript

This is a Javascript implementation of a vanilla neural network. I put this together to help visualize the neural net training process in a somewhat intuitive manner, all within the browser. As such, visualizaing the neural network as it learns is a somewhat intensive process for the browser and is restricted to relatively simple problems.

You can find the live visualization here: https://samgriesemer.com/projects/nn

# Usage

Everything is available in the repo, just fork or clone and open the index.html file in a browser to get things running. You can mess with the some of the core settings in the Javascript files or you can change training settings via the UI, which I'll breifly outline here:

The neural network diagram looks as follows:

<img src="https://samgriesemer.com/utils/resources/nn_explanation.png" width="90%">

Training options available through the UI:

* **Layers**: you can modify the network structure via a simple list describing how many nodes should be in each layer. By default, the network has the structure \[2,5,1\] (2 input nodes, 5 nodes in hidden layer, 1 output node). To add two hidden layers with 7 nodes each to the network, for example, you could change the layer list to be \[2,5,7,7,1\] and the network structure will update.

* **Epsilon**: this value controls the boundary for the random initialization of weights. A value of 1 would bound the weights to be randomly initialized between -1 and 1.

* **Alpha**: this value denotes the learning rate, which essentially controls the amount a gradient can update the network weights each iteration

* **Batch Size**: size of data batch when batch gradient descent is performed

* **Updates/loop**: number of training updates to be performed between each visualization update loop. Because the visualization runs at 60 fps, there is time between each frame to run backprop for multiple iterations. 

It's worth noting this project has not been extensively opmtized for user-friendliness; you can definitely break it. It's also an older project that I don't constantly update, but if you notice a bug or want to suggest an improvement I'd love to hear about it. Cheers
