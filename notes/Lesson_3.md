# Neural Network

## Objective

- Go through the network architecture.
- How to incorporate additional information into it.

## Architecture

- UNet
  - Input: Image
  - Output: Predicted noise with same size as image
  - First usage: Image segmentation
  - Special feature: Input and output are of same size
  - First embeds information about the input
    - Downsamples with a lot of convolutional layers, into an embedding that compresses information into a small amount of space.
  - Then it up-samples with the same number of up-sampling blocks.
  - Additional information taken by UNet in the form of embeddings
    - **Time embedding**: Related to the timestep and noise level.
      - Tells the model what the time step is, and therefore what kind of noise level we need.
    - **Context embedding**: Related to controlling the generation, e.g. text description or factor.
      - e.g. Factor: Certain color
