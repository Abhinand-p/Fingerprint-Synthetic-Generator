# Fingerprint Generation using Generative Adversarial Networks (GANs)

![generated_images_animation.gif](generated_images_animation.gif)
---

Implementation of a Generative Adversarial Network (GAN) for generating synthetic fingerprint images. 
GANs are a class of deep learning models that consist of two neural networks, a Generator and a Discriminator, trained simultaneously in a game-like setting. 
The Generator learns to produce realistic images, while the Discriminator learns to distinguish between real and generated images.

## Model Structure

### Generator
The Generator is responsible for synthesizing realistic fingerprint images from random noise. 
It consists of a series of transposed convolutional layers followed by batch normalization and ReLU activation functions. 
The input to the Generator is a random noise vector of size 100. 
This noise vector is gradually upsampled and transformed through multiple layers to generate the final output image. 
The transposed convolutional layers learn to progressively increase the spatial dimensions of the input noise, resulting in a high-resolution image. 
The final layer uses a Tanh activation function to ensure that the pixel values of the generated image are within the range [-1, 1].

- **Input**: Random noise vector of size 100
- **Output**: Synthesized fingerprint image

### Discriminator
The Discriminator acts as a binary classifier, distinguishing between real and fake (generated) fingerprint images. 
It comprises a series of convolutional layers followed by batch normalization and leaky ReLU activation functions. 
The input to the Discriminator is an image, either real or generated. 
The convolutional layers learn to extract features from the input image, and the final layer produces a single scalar value indicating the likelihood of the input image being real. 
This scalar value is passed through a sigmoid activation function to produce a probability score between 0 and 1, where values closer to 1 indicate a real image and values closer to 0 indicate a generated image.

- **Input**: Fingerprint image (real or generated)
- **Output**: Probability score indicating the likelihood of the input image being real
