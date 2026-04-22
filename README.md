# Deep-Learning-with-AlexNet-and-CIFAR-10 {-}

This notebook is adapted from a Deep Learning course assignment, with the aim of familiarizing students with training and testing the AlexNet neural network for an image classification task. The tasks include the process of loading data, preprocessing images, building the AlexNet model, evaluating its performance, and discussing some relevant questions. Below is the structure of the notebook:

1.  **Coding tasks:** 

    1.1 Load the dataset and perform image preprocessing, then split the data into training, validation, and test sets to prepare it for model training and evaluation.  

    1.2 Implement the vanilla AlexNet architecture from scratch, referred to as AlexNet version 1, by explicitly defining each layer in sequence for the image classification task. 

    1.3 Evaluate the performance of AlexNet version 1 using appropriate evaluation metrics and report the results.  
    1.4 Develop an enhanced model, AlexNet version 2, by adding or modifying architectural components with the goal of improving performance over AlexNet version 1. Clearly describe the design choices made.  

    1.5  Evaluate the performance of AlexNet version 2 and compare it with AlexNet version 1. Provide clear observations and analysis on how the architectural enhancements affected model effectiveness.  

2.  **Open discussion questions:**

    2.1 Preprocessing choices implicitly define the input distribution seen by the model. Select one preprocessing step you applied (for example normalization scheme, resizing method, or color space handling) and explain how it changes the geometry of the optimization landscape and the types of features the network can learn. Why might a different choice lead to slower convergence or worse generalization?  

    2.2 AlexNet contains multiple design elements such as large early kernels, aggressive downsampling, and deep fully connected layers. Based on your implementation and results, which of these elements do you believe are essential for AlexNet performance on your dataset, and which ones are largely incidental? Defend your answer using both intuition and experimental evidence.  

    2.3 When you modified AlexNet version 1 to obtain AlexNet version 2, how can you distinguish a genuine architectural improvement from a performance gain caused by randomness, training dynamics, or favorable initialization? Describe specific experimental controls or validation strategies that would support your conclusion.  
    2.4 Beyond reporting a higher accuracy, how would you diagnose where AlexNet version 2 improves over version 1 and where it still fails? Discuss how error analysis techniques such as confusion matrices, per class metrics, or misclassified example inspection can reveal strengths and weaknesses of the model.  

    2.5 Modern models are often built on large pretrained backbones, meaning networks that have already been trained on massive datasets such as ImageNet and are then adapted to new tasks using transfer learning. In this context, what important insights do you gain by training AlexNet entirely from random initialization, without any pretrained weights, that might be hidden or overlooked when starting from a pretrained model?  

The dataset we will be working on is CIFAR10 dataset. CIFAR10 (https://www.cs.toronto.edu/~kriz/cifar.html) consists of 60,000 32x32 colour images in 10 classes, with 6,000 images per class. There are 50,000 training images and 10,000 test images. Here follow the ten object classes:
* airplane
* automobile
* bird
* cat
* deer
* dog
* frog
* horse
* ship
* truck

Here follows some data samples in the dataset:

![alt text](https://docs.pytorch.org/tutorials/_images/cifar10.png)

### Reference {-}:
Alex Krizhevsky, Ilya Sutskever, Geoffrey E. Hinton, "Imagenet classification with deep convolutional neural networks", NIPS'12. Link to the paper: https://proceedings.neurips.cc/paper_files/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf

