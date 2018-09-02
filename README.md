# Training Deep Convolutional Generative Adversarial Networks (DCGANs)
## Experimenting with small datasets, colors and patterns

Training GANs in an adversarial setting means training two networks simultaneously and iteratively: the generator G, a generative model, that aims to replicate a data distribution (starting from random noise), which is then fed to the Discriminator D, a discriminative model, that estimates the probability of this data distribution coming from the training data rather than G, by simple classification (fake or real, 0 or 1). [1]

The layers of DCGANs change from fully connected layers in the orginial GANs to transpose convolutional for the Generator and convolutional layers for the Discriminator architecture. 

**Architecture guidelines for stable Deep Convolutional GANs:** [2]
* Replace pooling layers with strided convolutions (discriminator) and fractional-strided convolutions (generator). 
* Batchnorm in both the generator and the discriminator. 
* Remove fully connected hidden layers for deeper architectures. 
* ReLU activation in generator for all layers except for the output, > Tanh. 
* LeakyReLU activation in the discriminator for all layers.



## Experimental setup:

Objective: Generate images of oceans and mountains



![oceans_and_mountains](https://github.com/suzana-ilic/pytorch_DCGANs/blob/master/dcgans.gif)


**References**

[1] Goodfellow, I., Pouget-Abadie, J., Mirza, M., Xu, B., Warde-Farley, D., Ozair, S., ... & Bengio, Y. (2014). Generative adversarial nets. In Advances in neural information processing systems (pp. 2672-2680). https://arxiv.org/abs/1406.2661

[2] Radford, A., Metz, L., & Chintala, S. (2015). Unsupervised representation learning with deep convolutional generative adversarial networks. arXiv preprint arXiv:1511.06434. https://arxiv.org/pdf/1511.06434.pdf
