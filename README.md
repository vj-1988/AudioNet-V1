# AudioNet-V1
AudioNet is a simple convolutional neural net based on 1-D convolutions. This is trained and tested on google's speech command dataset.

## Requirements

Tested with following setup

### Software
1) Python 3.5
2) Numpy
3) Scipy
4) Keras 2.0.8
5) Tensorflow 1.4.1
6) Scikit-learn

### Hardware

1) GTX 1050 TI 4 GB

## One Dimensional CNN
Here, 1-D convolutions (linear convolutions) are used to classify the speech signal. The dataset used is Google's peech Commands Dataset

The network has five convolutional layers with kernel size 32 and stride of 4. They are followed by four hidden layers with 512 neurons each. The network has approximately 10 million parameters in total.

### Data Augmentation used

1) Random noise
2) Random shift

### Training Loss vs Epochs

(https://github.com/vj-1988/AudioNet-V1/blob/master/Images/training_loss.png)

### Training Acuracy vs Epochs

(https://github.com/vj-1988/AudioNet-V1/blob/master/Images/training_accuracy.png)
