# Quantized Deep Neural Network for Defect Detection on Jetson AGX Xavier Using GPU Coder
## How to create, train and quantize network, then integrate it into pre/post image processing and generate CUDA C++ code for targeting Jetson AGX Xavier

Deep Learning is really powerful approach to solve difficult problems(e.g. image classification, segmentation and detection). However, performing inference using deep learning is computationally intensive, consuming significant amount of memory. Even networks that are small in size require a considerable amount of memory and hardware to perform these arithmetic operations. These restrictions can inhibit deloyment of deep learning networks to devices that have low computational power and smaller momory resources.

In this case, you can use Deep Learning Toolbox in tandem with the Deep Learning Toolbox Model Quantization Library support package to reduce the memory footprint of a deep neural network by quantizing the weights, biases, and activations of convolution layers to 8-bit scaled integer data types. And then you can use GPU Coder to generate optimized CUDA code for the quantized network.

This example shows how to create, train and quantize a simple convolutional neural network for defect detection, then demonstrate how to generate code for whole algorithms that includes pre/post image processing and convolutional neural network so that you can deploy it into NVIDIA GPUs such as Jetson AGX Xavier, Nano and Drive platforms.

This example demonstrates how to:
1. Load and explore image data
1. Define the network architecture and training options
1. Train the network and classify validation images
1. Quantize network to reduce memory footprint
1. Walk through whole algorithm that consist of pre-processing, CNN and post-processing
1. Generate CUDA C++ code(MEX) for whole algorithm
1. Deploy algorithms to NVIDIA hardware
1. Run the Executable on the Target

![title](https://user-images.githubusercontent.com/63379838/78849073-73610f80-7a4e-11ea-8feb-3f1c3ec0a0e5.png)

--------------------------------------------------------------------------------

## Prerequisites - MathWorks Products and Support Packages

- MATLAB (R2020a or later)
- MATLAB® Coder™
- Parallel Computing Toolbox™
- Deep Learning Toolbox™
- Image Processing Toolbox™
- Computer Vision Toolbox™

--------------------------------------------------------------------------------

## Prerequisites - Third-party Products

- NVIDIA® GPU enabled for CUDA with compute capability 3.2 or higher (6.1 or higher is required for quantization)
- CUDA toolkit and driver
- C/C++ Compiler 
- CUDA Deep Neura Network library (cuDNN)
- Open Source Computer Vision Library v3.1.0
- (Optional) NVIDIA TensorRT
- The support package GPU Coder Interface for Deep Learning
- GPU Coder Support Package for NVIDIA GPUs
- The support package Deep Learning Toolbox Model Quantization Library
- Environment variables for the compilers and libraries. For information on the supported versions of the compilers and libraries, see Third-party Products. For setting up the environment variables, see Setting Up the Prerequisite Products.
