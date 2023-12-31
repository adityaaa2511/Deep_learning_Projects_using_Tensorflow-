# Deep_learning_Projects_using_Tensorflow-
This repository contains all the deep learning models that I have implemented while learning Tensorflow.

## Transfer Learning for Computer Vision
*Using Pre-trained CNN bodies on large datasets like ImageNet and using the trained weights/bodies for classification. Some examples of popular state-of-the-art models include VGG,ResNet,Inception etc*
* Since, huge datasets like **ImageNet** contains millions of images we make use of **ImageDataGenerator** to perform Batch Gradient Descent to train the weights of the head of the VGG(body weights are pre-trained and hence, frozen to avoid re-training).<br/>
* IDG also gives an option to perform **Data Augmentation**(flipping,shifting,rotating the image), using which we can generalise the training of the weights of the body of the VGG. But, there is a flipside to this that we might have to re-train the weights of the body which may take a considerable amount of time.<br/>
* We can clearly observe that using transfer learning with data augmentation leads to a better accuracy(**97.8%**)as compared the (**97.5%**) accuracy achieved without using it, though the time taken per epoch is order of magnitudes larger(**2200s as compared to 0s**)<br/>

## Recommender Systems
*Training neural network models on User, Object, Rating dataset for recommending unseen/unused objects to users based on the type/genre that they have rated the highest* <br/>
* **Future Prospects**:- Building advanced recommender systems using Autoencoders and Restricted Boltzmann Machines 

## Generative Adversarial Networks
*Some key points I learnt while researching/reading/exploring Generative Adversarial networks popularly known as GANs.*<br/>
* A GAN is not just a single neural network, but a system of 2 neural networks: **Generator** and **Discriminator**.<br/>
* The loss function for the discriminator is simply the **BINARY CROSS ENTROPY FUNCTION** as its job is to simply classify the generated images as fake(1) or real(0).<br/>
* The Generator is not trained individually like the Discriminator, but in fact it is trained as a **Combined Model** with the discriminator while **Freezing the Weights** of the Discriminator.<br/>
* The input to the Generative network is **NOISE** sampled from the **LATENT SPACE**.<br/>
* In simple terms, the Latent Space is just like the inverse of feature transformation/embeddings which means that the Generator maps vector/features/embeddings to images.<br/>
* Since we are not doing regression/classification, the loss per iteration should not decrease, rather it should be similar to Random Noise.<br/> 
