# Vector Quantized Variational Autoencoder (VQ-VAE)

This repository contains an implementation of a Vector Quantized Variational Autoencoder (VQ-VAE) in PyTorch. The VQ-VAE is a powerful generative model that combines ideas from vector quantization and variational autoencoders to learn discrete latent representations of data.

## Overview

The VQ-VAE architecture consists of:
- An encoder that compresses input data into a discrete latent space
- A vector quantization layer that maps continuous encodings to discrete codes
- A decoder that reconstructs the input from the quantized representations

## Training Details

The model is trained on image data with the following specifications:
- Number of epochs: 50
- Batch size: Variable (146 batches per epoch)
- Loss function: Combination of reconstruction loss and commitment loss
- Training progress is monitored through:
  - Per-batch loss values
  - Reconstructed image samples saved each epoch

## Training Progress

The training shows clear convergence:
- Initial loss values around 50-60 in epoch 1
- Steady decrease to ~0.8-1.0 by epoch 4  
- Further improvement to ~0.4-0.5 by epoch 16
- Final convergence to ~0.35-0.40 by epoch 33

## Results

The model saves reconstructed images throughout training to visualize the quality of learned representations. These can be found in the `reconstructed_images` directory.

## Usage

To train the model:
1. Ensure PyTorch is installed
2. Run the Jupyter notebook `Vector-Quantized-Variational-Autoencoder.ipynb`
3. Monitor training progress through loss values and reconstructed images

## References

This implementation is based on the original VQ-VAE paper:
van den Oord, A., Vinyals, O., & Kavukcuoglu, K. (2017). Neural Discrete Representation Learning. arXiv preprint arXiv:1711.00937.
