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

[Download the C2A Dataset](INSERT_DRIVE_LINK_HERE)

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
@article{nihal2024uav,
  title={UAV-Enhanced Combination to Application: Comprehensive Analysis and Benchmarking of a Human Detection Dataset for Disaster Scenarios},
  author={Nihal, Ragib Amin and Yen, Benjamin and Itoyama, Katsutoshi and Nakadai, Kazuhiro},
  journal={arXiv preprint arXiv:2408.04922},
  year={2024}
}
