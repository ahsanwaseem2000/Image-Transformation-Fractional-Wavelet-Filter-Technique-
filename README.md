# Fractional Wavelet Filter for Efficient Image Compression on Raspberry Pi Zero

This repository contains a study on the use of **Fractional Wavelet Filter (FrWF)** as an image compression technique optimized for the **Raspberry Pi Zero**, a low-resource embedded platform. The research focuses on the memory-efficient properties of FrWF, which makes it suitable for devices like the Raspberry Pi Zero with limited memory and processing power.

## Table of Contents
- [Project Overview](#project-overview)
- [Tech Stack](#tech-stack)
- [Research Methodology](#research-methodology)
- [Implementation Details](#implementation-details)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Project Overview

The **Fractional Wavelet Filter (FrWF)** is a novel image compression method designed to minimize memory usage by leveraging external memory resources for storing intermediate data during the wavelet transformation process. This approach significantly reduces the memory bottlenecks commonly faced by low-resource platforms such as the Raspberry Pi Zero, which typically has limited onboard memory (256 MB to 512 MB).

In this project, we evaluate the performance of FrWF in terms of **compression efficiency**, **memory utilization**, and **image quality**. The goal is to demonstrate that FrWF can be a practical solution for **image compression** on resource-constrained devices, such as the Raspberry Pi Zero, without sacrificing image fidelity.

## Tech Stack

- **Programming Languages**:
  - **Python**: For implementing the FrWF algorithm and image processing.
  - **NumPy**: For handling arrays and mathematical operations.
  - **OpenCV**: For loading and processing images.
  - **Matplotlib**: For visualizing images and results.
  
- **Tools & Libraries**:
  - **Spyder**: An integrated development environment (IDE) used for running and testing the code on the Raspberry Pi Zero.
  
## Research Methodology

### Key Research Objectives:
1. **Compression Performance**: Compare FrWF's performance with traditional methods (e.g., JPEG, JPEG 2000) in terms of compression ratios and image quality.
2. **Memory Efficiency**: Assess how well FrWF can manage memory usage by utilizing external storage resources, a critical feature for devices with limited memory.
3. **Scalability**: Evaluate FrWF's scalability by testing its performance with different image sizes and levels of complexity.

### Contributions:
- **FrWF Algorithm**: A new approach to image compression that uses external memory for wavelet transformation data.
- **Raspberry Pi Zero**: This research focuses on using the Raspberry Pi Zero, demonstrating that FrWF can operate effectively even with the platform's memory limitations.

## Implementation Details

1. **3-Level Wavelet Decomposition**: The FrWF algorithm uses a 3-level decomposition to break down the image into approximation and detail coefficients. This process involves separating the image into different frequency bands, which can be compressed individually.

2. **External Memory Usage**: The FrWF algorithm dynamically allocates memory and stores intermediate data on external memory resources (e.g., microSD cards or external storage), alleviating the pressure on the Pi Zero's limited onboard memory.

3. **Image Compression and Reconstruction**: The image is compressed using FrWF, and the original image is reconstructed by reversing the wavelet transformation, ensuring that the integrity of important image features is maintained.

4. **Evaluation Metrics**:
   - **PSNR (Peak Signal-to-Noise Ratio)**: A common metric for evaluating image quality after compression.
   - **SSI (Structural Similarity Index)**: Measures the perceptual quality of the compressed image.
   - **Compression Ratio**: The ratio of the original image size to the compressed image size.

## Usage

### Requirements:
- **Python 3.x**
- **NumPy**: `pip install numpy`
- **OpenCV**: `pip install opencv-python`
- **Matplotlib**: `pip install matplotlib`


