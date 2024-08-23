# C2A: Combination to Application Dataset

## Overview

This repository contains the code and information for the paper "UAV-Enhanced Combination to Application: Comprehensive Analysis and Benchmarking of a Human Detection Dataset for Disaster Scenarios" by Ragib Amin Nihal, Benjamin Yen, Katsutoshi Itoyama, and Kazuhiro Nakadai.

The C2A (Combination to Application) dataset is a novel synthetic dataset designed to advance human detection in disaster scenarios using UAV imagery. It combines disaster scene backgrounds from the AIDER dataset with human poses from the LSP/MPII-MPHB dataset to create a comprehensive resource for training machine learning models.

The full paper is available at: [https://arxiv.org/pdf/2408.04922](https://arxiv.org/pdf/2408.04922)

## Example Images

Here are some example images from the C2A dataset:

![Example 1](dataset_example.png)
*Caption: A synthetic disaster scene with multiple human poses*

## Dataset

The C2A dataset consists of 10,215 images containing over 360,000 annotated human instances in various disaster scenarios. It includes diverse human poses (bent, kneeling, lying, sitting, upright) and disaster contexts (traffic incidents, fire, flood, collapsed buildings).

[Download the C2A Dataset (Drive](https://drive.google.com/file/d/1Uba6CHJRCvF-rgfCXDR6NhTnOvngWsfe/view?usp=sharing)

Alternatively, you can download from [Kaggle](https://www.kaggle.com/datasets/rgbnihal/c2a-dataset)

## Dataset Structure

The C2A dataset is organized into training, validation, and test sets, with multiple annotation formats for flexibility in use. Below is the structure of the dataset:

new_dataset3/
  All labels with Pose info/
    [YOLO format labels with pose information for all images]
  test/
    images/
      [Test image files]
    labels/
      [YOLO format label files for test images]
    test_annotations.json  [COCO format annotations for test set]
  train/
    images/
      [Training image files]
    labels/
      [YOLO format label files for training images]
    train_annotations.json  [COCO format annotations for training set]
  val/
    images/
      [Validation image files]
    labels/
      [YOLO format label files for validation images]
    val_annotations.json  [COCO format annotations for validation set]

### File Descriptions

1. **Image Files**:
   - Located in the `images` subfolder of each set (train, val, test)
   - Format: [Specify image format, e.g., JPG, PNG]

2. **YOLO Format Annotations**:
   - Located in the `labels` subfolder of each set
   - Format: Text files (.txt) with one line per object
   - Each line contains: `class x_center y_center width height`
   - Coordinates are normalized to [0, 1]

3. **COCO Format Annotations**:
   - JSON files: `train_annotations.json`, `val_annotations.json`, `test_annotations.json`
   - Contains detailed information about images and annotations in COCO format

4. **Pose Information Labels**:
   - Located in `All labels with Pose info` folder
   - YOLO format with an additional value for pose
   - Format: `class x_center y_center width height pose`
   - Pose values:
     - 0: Bent
     - 1: Kneeling
     - 2: Lying
     - 3: Sitting
     - 4: Upright

### Usage Notes

- The dataset is split into training, validation, and test sets.
- Two annotation formats are provided for flexibility: YOLO and COCO.
- Pose information is available in a separate folder for all images.
- Users can choose between standard object detection (YOLO/COCO) or pose-aware detection (All labels with Pose info).

## Key Features

- Synthetic dataset combining real disaster scenes with human poses
- Over 360,000 annotated human instances
- 5 human pose categories
- 4 disaster scenario types
- Image resolutions ranging from 123x152 to 5184x3456 pixels
- Designed to improve human detection in complex disaster environments

## Usage

[Include instructions on how to use the dataset, any preprocessing steps, and example code for loading the data]

## Benchmarking Results

We evaluated several state-of-the-art object detection models on the C2A dataset. Here are some of the key results:

| Model         | mAP    | mAP@.50 |
|---------------|--------|---------|
| YOLOv9-e      | 0.6883 | 0.8927  |
| YOLOv9-c      | 0.5562 | 0.7996  |
| YOLOv5        | 0.4920 | 0.8080  |
| Cascade R-CNN | 0.4860 | 0.7350  |
| Dino          | 0.4710 | 0.7890  |

For full results and analysis, please refer to the paper.

## Citation

If you use this dataset in your research, please cite our paper:
- *Ragib Amin Nihal, Benjamin Yen, Katsutoshi Itoyama, Kazuhiro Nakadai* (2024). **UAV-Enhanced Combination to Application: Comprehensive Analysis and Benchmarking of a Human Detection Dataset for Disaster Scenarios**. [paper](https://arxiv.org/pdf/2408.04922)
