# Deep_learning_Projects_using_Tensorflow-
This repository contains all the deep learning models that I have implemented while learning Tensorflow.

## Transfer Learning for Computer Vision
*Using Pre-trained CNN bodies on large datasets like ImageNet and using the trained weights/bodies for classification. Some examples of popular state-of-the-art models include VGG,ResNet,Inception etc*
* Since, huge datasets like ImageNet contains millions of images we make use of **ImageDataGenerator** to perform Batch Gradient Descent to train the weights of the head of the VGG(body weights are pre-trained and hence, are freezed).<br/>

## Recommender Systems
*Training neural network models on User, Object, Rating dataset for recommending unseen/unused objects to users based on the type/genre that they have rated the highest* <br/>

## Generative Adversarial Networks
*Some key points I learnt while researching/reading/exploring Generative Adversarial networks popularly known as GANs.*<br/>
* A GAN is not just a single neural network, but a system of 2 neural networks: **Generator** and **Discriminator**.<br/>
* The loss function for the discriminator is simply the **BINARY CROSS ENTROPY FUNCTION** as its job is to simply classify the generated images as fake(1) or real(0).<br/>
* The Generator is not trained individually like the Discriminator, but in fact it is trained as a **Combined Model** with the discriminator while **Freezing the Weights** of the Discriminator.<br/>
* The input to the Generative network is **NOISE** sampled from the **LATENT SPACE**.<br/>
* In simple terms, the Latent Space is just like the inverse of feature transformation/embeddings which means that the Generator maps vector/features/embeddings to images.<br/>
* Since we are not doing regression/classification, the loss per iteration should not decrease, rather it should be similar to Random Noise.<br/> 
