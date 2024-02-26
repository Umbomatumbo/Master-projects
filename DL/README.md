# Abstract

This paper presents an in-depth study of a research framework focused on encoding information from *n* grayscale images to a single 'RGB' image for training a Convolutional Neural Network (CNN). The study explores alternate approaches for converting grayscale images to RGB, enriching the CNN training process. The investigation includes the implementation of diverse transformation techniques and a comparative analysis of the network's performance on MATLAB and PyTorch platforms. The results indicate improved accuracy, ranging from 2% to more than 5%, compared to the original project.

# Research Objectives

The research aims to enhance the existing framework for encoding grayscale images into RGB for CNN training. The focus is on exploring different conversion techniques, evaluating performance on both MATLAB and PyTorch, and assessing the impact on CNN's ability to extract meaningful features.

## Methodology

### Grayscale to RGB Conversion Techniques

- **Median Algorithm (MATLAB):** Divides grayscale images into three subsets, computes the median for each, and creates an RGB output image.

- **Alpha-Trimmed Mean Algorithm (PyTorch):** Applies alpha-trimmed mean to reduce noise and uses a pre-trained CNN for image colorization.

- **Percentile Algorithm (Original):** Computes percentiles for pixel sets to create RGB images.

### Experimental Setup

- Utilizes a diverse dataset of foraminifera specimens captured under varying lighting conditions.
  
- Pre-trained CNN models (AlexNet) are adapted for the task.

# Results and Discussion

## MATLAB Model

- Best dataset: Median algorithm with an accuracy of 78.32%.

- Comparative analysis with alpha-trimmed mean (77.35%) and percentile algorithm (76.06%).

- Heatmaps and accuracy comparisons demonstrate the effectiveness of the median algorithm.

## PyTorch Model

- Best dataset: Alpha-trimmed mean (alpha=8) with an accuracy of 75.69%.

- Comparative analysis with median algorithm (73.17%) and percentile algorithm (69.47%).

- Larger variance in accuracy compared to MATLAB, emphasizing differences in training processes.

# Conclusion

The study successfully enhances the original framework's performance through different grayscale to RGB conversion techniques. The challenges of cross-environment comparisons are highlighted, emphasizing the need for a comprehensive understanding of platform-specific nuances. The results contribute to the broader discourse on tailoring machine learning solutions to specific programming environments.

# Project contrributors
David P. and Federico L.
