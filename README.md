# Quantized Deep Neural Network for Defect Detection on Jetson AGX Xavier Using GPU Coder
## How to create, train and quantize network, then integrate it into pre/post image processing and generate CUDA C++ code for targeting Jetson AGX Xavier

Deep Learning is really powerful approach to solve difficult problems(e.g. image classification, segmentation and detection). However, performing inference using deep learning is computationally intensive, consuming significant amount of memory. Even networks that are small in size require a considerable amount of memory and hardware to perform these arithmetic operations. These restrictions can inhibit deloyment of deep learning networks to devices that have low computational power and smaller momory resources.

In this case, you can use Deep Learning Toolbox in tandem with the Deep Learning Toolbox Model Quantization Library support package to reduce the memory footprint of a deep neural network by quantizing the weights, biases, and activations of convolution layers to 8-bit scaled integer data types. And then you can use GPU Coder to generate optimized CUDA code for the quantized network.

This example shows how to create, train and quantize a simple convolutional neural network for defect detection, then demonstrate how to generate code for whole algorithms that includes pre/post image processing and convolutional neural network so that you can deploy it into NVIDIA GPUs such as Jetson AGX Xavier, Nano and Drive platforms.

![title](https://user-images.githubusercontent.com/63379838/78849073-73610f80-7a4e-11ea-8feb-3f1c3ec0a0e5.png)

--------------------------------------------------------------------------------

## Requirements

- MATLAB R2020a
- Automated Driving Toolbox
- Sensor Fusion and Tracking Toolbox

--------------------------------------------------------------------------------
