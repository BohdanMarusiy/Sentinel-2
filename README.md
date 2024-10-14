# Image Matching with Sentinel-2 Data

## Overview

This project involves the development and evaluation of various feature matching algorithms tailored for Sentinel-2 satellite imagery. We focused on classical computer vision techniques, such as SIFT, ORB, and AKAZE, and incorporated RANSAC for geometric verification to ensure robust matching under varying conditions like season, time of day, and lighting changes.

## Challenges

Sentinel-2 imagery presents unique challenges, including substantial variations due to different seasons, times of capture, and lighting conditions. This required fine-tuning and adapting algorithms to maintain accurate feature matching across these variables.

## Achievements

Through iterative debugging and parameter adjustments, we improved the accuracy of image matching. Our solutions demonstrated robustness in handling the complex visual differences within the dataset.

## D2-Net Usage Guide

To use D2-Net for feature extraction and matching, follow these steps:

### Clone the D2-Net Repository

```bash
git clone https://github.com/mihaidusmanu/d2-net.git
```
### Pre-requisites

Ensure you have the following dependencies installed:

- Python 3.x
- OpenCV
- NumPy
- PyTorch
- h5py
- imagesize
- scipy

### Downloading Pre-trained Weights

You can download the necessary pre-trained D2-Net model weights with the following commands:

```bash
wget https://dsmn.ml/files/d2-net/d2_ots.pth -O models/d2_ots.pth
wget https://dsmn.ml/files/d2-net/d2_tf.pth -O models/d2_tf.pth
wget https://dsmn.ml/files/d2-net/d2_tf_no_phototourism.pth -O models/d2_tf_no_phototourism.pth
```
### Extracting Features

To extract features from Sentinel-2 images, run the following command:

```bash
python extract_features.py --image_list_file "<path_to_image_list.txt>" --model_file "<path_to_weights_file>"
```

This will generate `.npz` files containing the extracted features.

### Visualizing Keypoint Matching

Once the features are extracted and stored in `.npz` files, you can use them to visualize keypoint matching between Sentinel-2 images.
