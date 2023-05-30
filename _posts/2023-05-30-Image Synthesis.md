---
layout: post

title: Generative Models and Image Synthesis
thumbnail-img: /assets/img/2023-05-30-génération_des_images.png
cover-img: /assets/img/2023-05-30-génération_des_images.png

tags: [Variational Autoencoders, Generative Adversarial Networks, Probabilistic Diffusion Models]

comments: true

pinned: true
---

**In recent years, generative models have been used extensively in image synthesis, where they can create new and realistic images that are indistinguishable from the real ones. In this article we will explore the different types of generative models used in image synthesis, including Variational Autoencoders (VAEs), Generative Adversarial Networks (GANs), and Probabilistic Diffusion Models**

## 1.	Variational Autoencoders (VAEs):

VAEs are unsupervised learning models designed to learn a compressed representation of input data in a lower-dimensional latent space. They consist of an encoder and a decoder. The encoder maps input data to a probability distribution in the latent space. The decoder takes samples from this distribution and reconstructs the original input. The VAE's objective is to minimize the reconstruction error while maintaining a well-structured latent space through a regularization term. The regularization term encourages the encoder to generate latent representations that follow a standard normal distribution, enabling smooth interpolations between data points in the latent space.

## 2.	Generative Adversarial Networks (GANs):

GANs consist of two competing neural networks: a generator and a discriminator. The generator learns to create realistic images by mimicking the real data distribution, while the discriminator learns to differentiate between real and generated images. Both networks are trained simultaneously in a competitive manner, with the generator improving its image generation capabilities as the discriminator becomes better at identifying fake images. GAN variations include:
  - Deep Convolutional GANs (DCGANs): These GANs use Convolutional Neural Networks (CNNs) for both the generator and discriminator, enabling better feature learning from images.
  - Wasserstein GANs (WGANs) and WGAN-GP: These GANs improve training stability by using the Wasserstein distance to measure the divergence between real and generated data distributions. WGAN-GP adds a gradient penalty term to further stabilize training and prevent gradient explosion issues.

## 3.	Probabilistic Diffusion Models:

Probabilistic Diffusion Models and Latent Diffusion Models are generative models that involve learning to reverse a well-defined stochastic process that progressively destroys images by adding Gaussian noise. Both models have similarities in their approaches to generating images; however, Latent Diffusion Models incorporate concepts from Variational Autoencoders (VAEs) to perform diffusion in a latent space instead of the original image space.

In Probabilistic Diffusion Models, the training process involves learning to denoise images iteratively. During inference, the model starts with Gaussian noise and iteratively denoises it to generate a high-quality image.

Latent Diffusion Models, on the other hand, first use a VAE to encode the input image into a lower-dimensional latent space. The diffusion process is then applied in this latent space, making the training process more stable and faster. During the reverse diffusion process, the denoised latent representation is decoded back into the image space to generate the final output. This approach allows for improved training stability and faster inference times compared to classical diffusion models.

