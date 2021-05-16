# Machine-Learning-Projects
classifying images using convolutional neural networks.

Description of the model:
            Input data is of the form 3x32x32, since each image is a coloured image in RGB framework. Convolutional Layer1 will map the input images into 6X28X28 feature map using a kernel(filter) of size 5x5. Maxpooling operation is then performed resulting in 6x14x14 feature maps. Convolutional Layer2 will map the output of Maxpooling operation to 16x10x10 feature map which after performing maxpooling operation gets converted into 16x5x5 dimensions. Now this output is converted into a row vector of size 400 which is then fed to a fully connected layer (Logistic regression operation). Activation function used in this operation is ReLU (Rectified Linear Activation Function). After using one hidden layer we get the output which tells us the probabilites of image belonging to a particular class. Class with highest probability will be considered as the predicted output of the model.

Why did we use epochs and minibatches?
Ans:  We use minibatches so that error updation process will only be done after predicted the results for each of the image in the minibatch. Both time and computational complexity of the model are reduced by using minibatches to train the data. Using minibatches also helps in reaching the minima of our loss function. Epochs are used in order to train our model on the same training dataset again and again. In cifar10 dataset the number of training images are 50000 which is insufficent to build a model with good accuracy. So, inorder to improve accuracy of the model we iterate through our training dataset again and again.
