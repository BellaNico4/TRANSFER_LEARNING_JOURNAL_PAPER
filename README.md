# Deep Learning Strategies for Labeling and Accuracy Optimization in Microcontroller Performance Screening

## Introduction

This repository contains the implementation of the deep learning-based framework described in the paper "Deep Learning Strategies for Labeling and Accuracy Optimization in Microcontroller Performance Screening" by Nicolo' Bellarmino, Riccardo Cantoro, Martin Huch, Tobias Kilian, Ulf Schlichtmann, and Giovanni Squillero. Published in 2024 in the *Transactions on Computer-Aided Design*. 

Our framework leverages Semi-Supervised Learning (SSL) and Transfer Learning to optimize the performance screening of microcontrollers (MCUs). The approach reduces the prediction error and minimizes the need for labeled samples, enhancing the efficiency of the MCU characterization phase and data collection.

[![plot](media/TRANSFER_LEARNING_DIAGRAM.png)]

## Installation

To use the models and run the example provided, please follow these steps:

1. Clone this repository:
    ```sh
    git clone https://github.com/BellaNico4/DL-Strategies-in-MCU-Screening
    cd DL-Strategies-in-MCU-Screening
    ```

2. Create and activate a virtual environment with conda:
    ```sh
    conda create --name <env> --file requirements.txt
    conda activate <env>
    ```

## Usage

The notebook (*smons_transfer_learning*) provide a minimal working example on artificial data sample. Target y is a linear combination of polynomial transformation of the input features X.

### Example 1: Performance Prediction for Product A1

This example demonstrates how to train a deep feature extractor to predict the performance of MCU product A1 and save the checkpoint.

### Example 2: Transfer Learning on A2

This example shows the application of transfer learning to predict the performance of a new MCU product A2 using a pre-trained model on product A1.

### Example 3: Transfer Learning and features selection

Benchmark of several ML models on A2, with class to select random or specific columns in order to use the pretrained models.


## Model Details

The framework is designed to:
- Reduce the number of labeled samples required by up to a factor of six.
- Use deep neural networks as feature extractors.
- Leverage transfer learning to adapt models to new products and families.
- Minimize prediction error and guardband, enhancing process yield.

We both provided the architecture and the pretrained weights for two of the CNNs described in the paper (Pseudo-Labeling CNN, PL-CNN and AutoEncoder-CNN, AE-CNN). We also provided pretrained weights on artificial data with which reproduce the framework behavior.

For more details on the model architecture and training process, refer to the paper [Deep Learning Strategies for Labeling and Accuracy Optimization in Microcontroller Performance Screening](https://ieeexplore.ieee.org/document/10620213).

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Citation

If you use this code in your research, please cite the paper:

```
@ARTICLE{bellarmino2024,
  author={Bellarmino, Nicolò and Cantoro, Riccardo and Huch, Martin and Kilian, Tobias and Schlichtmann, Ulf and Squillero, Giovanni},
  journal={IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems}, 
  title={Deep Learning Strategies for Labeling and Accuracy Optimization in Microcontroller Performance Screening}, 
  year={2024},
  volume={},
  number={},
  pages={1-1},
  keywords={Transfer learning;Predictive models;Feature extraction;Data models;Testing;Microcontrollers;Accuracy;Fmax;Speed Monitors;Ring Oscillators;Speed Binning;Machine Learning;Device Testing;Manufacturing;Transfer Learning;Deep Learning},
  doi={10.1109/TCAD.2024.3436542}}
```

## Contact

For any questions or comments, please contact Nicolo' Bellarmino at [nicolo.bellarmino@polito.it].