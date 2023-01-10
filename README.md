# Fast training CNN network for CIFAR-10
* Reachs 80% accuracy within 4 epochs!
* Runs in 1200s with Google Colab's CPU runtime!
## Sepcification
```yaml
Title: Fast Training CIFAR-10 Model
Base model: ResNet-9
Author: Junu Kwon, Seoul National University
Contact: junukwon7@snu.ac.kr
Date: 2022-12-15
Description:
    This is a model for CIFAR-10 dataset.
    The model was trained for 4 epochs.
    The model was trained and tested on Google Colab.
Results within 10 trials:
    Best top-1 ACCURACY: 81.32%
    Average top-1 ACCURACY: 78.81%
    Min top-1 ACCURACY: 76.75%
    Train time: 1048.62s < 1200s
Hyperparameters:
    Learning rate: [0.06, 0.15, 0.2, 0.05]
    Batch size: 125
    Number of workers: 1
    Number of epochs: 4
    Batch normalization momentum: 0.4
    Label smoothing: 0.05
    Weight decay: 1e-4
    Activation: ReLU
    Optimizer: Adagrad
    Loss: CrossEntropyLoss
    See tune() for more details on tuning hyperparameters.
```

## How fast is it?
It gains about 77~81 top-1 acc within 4 epochs.
Which means < 1200s(20min) in Google Colab's CPU runtime.

![curve](https://user-images.githubusercontent.com/48399106/211515891-087e14b5-fa1b-41dd-bdaf-3d4c3382930c.png)

## Data Augmentation or Test-Time Augmentation?
Gains more accuracy, but makes the network slower. So, no.

## CELU?
No big difference within 4 epochs.

# Credit
This project was the final assessment of my school project, <br>
L0444.000300: Introduction to Artificial Intelligence, Byoung-Tak Zhang, SNU CSE (인공지능 입문, 장병탁). 

There is also a ~6pg pdf report for it, but I decided to not disclose it to prevent plagiarism.
