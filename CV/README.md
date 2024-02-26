# Computer Vision Project - Food Tray Image Segmentation

## Overview

This project, authored by David Petrovic, Federico Luisetto, and Umberto Salviati, focuses on developing a computer vision system for estimating leftover food on a canteen consumer's tray after a meal. The system analyzes pairs of images, one taken before the meal and one after, to identify and quantify the remaining types of food.

## Project Description

The project is divided into three main parts:

1. **Food Recognition and Localization:** Identifying and localizing different types of food in the tray images based on a provided dataset.

2. **Food Segmentation:** Segmenting food items to compute the quantity of each item.

3. **Image Comparison:** Comparing images taken before and after the meal to determine which foods were consumed.

## Project Implementation

The project tackles the challenges posed by noisy images by working on different portions separately. Various techniques are employed, including color-based segmentation and texture analysis for specific items like bread. The project utilizes the CLIP (Contrastive Language-Image Pre-Training) neural network model for food item recognition.

## Circles Extraction

The project employs the Hough transform to detect circles in tray images, facilitating the extraction of plates and covering noise for bread segmentation.

## Bread Extraction

A texture-based approach is used for bread extraction, involving gamma transform, histogram equalization, Niblack thresholding, and the GrabCut algorithm. Results indicate a successful identification of bread items.

## Salad Extraction

The salad is identified by analyzing the radius of plates, showcasing a simple yet effective approach.

## CLIP

The CLIP model is utilized for food item recognition, with a training phase to select appropriate labels. The challenges of language differences and communication between Python and C++ are addressed.

## Segmentation of Plate Food

Segmentation of food items is accomplished using a hybrid approach, combining CLIP predictions and color-based segmentation.

## Bounding Box

Bounding boxes are generated around segmented food regions to evaluate and refine segmentation results.

## Performance Measurement

- **mAP (mean Average Precision):** Achieved a result of 0.566239, considering true positives and false positives.
- **mIoU (mean Intersection over Union):** Evaluated for each class, with varying results indicating segmentation performance.

## Food Leftover Estimation

Estimation of food leftovers is performed by comparing masks, and the results are saved in `data/result/results.txt`.

## How to Run the Code

To run the code, follow these commands:

```bash
cd out/build/x64-release
cmake ../../..
make
./CV-proj
```

Results will be stored in the `data/result` folder.

## Conclusion

The hybrid approach demonstrates effectiveness, with acknowledgment of areas for improvement. Refining labels for CLIP and exploring advanced techniques with a larger dataset are suggested for future enhancements. The project lays a foundation for robust and efficient food tray image segmentation with further experimentation and development.
