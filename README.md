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
Here, 1-D convolutions (linear convolutions) are used to classify the speech signal. The dataset used is Google's speech Commands Dataset

The network has five convolutional layers with kernel size 32 and stride of 4. They are followed by four hidden layers with 512 neurons each. The network has approximately 10 million parameters in total.

### Data Augmentation used

1) Random noise
2) Random shift

### Training Loss vs Epochs

![](https://github.com/vj-1988/AudioNet-V1/blob/master/Images/training_loss.png)

### Training Acuracy vs Epochs

![](https://github.com/vj-1988/AudioNet-V1/blob/master/Images/training_accuracy.png)


## Training 

The dataset has to be in appropriate subfolders with each folder name being the class label. The script AudioNet32.py needs the following inputs to train

1) data_path : root folder of dataset
2) train_ratio : ratio of files to be used for training and remaining is for validation
3) batch_size : minibatch size for training.
4) num_epochs : total no. of epochs
5) dst : destination folder to save weights, logs

The script will generate a pickle file that contains synset for validation, training and validation files path and labels. This can be used to resume training using resume_training() function.

The script will save weights once in every 2 epochs.

## Validation

The synset used for training is available in train_data_dic.pkl file. The pretrained weights are available in the following link

[Download pretrained weights (Epoch 10)](https://drive.google.com/file/d/1vrfeXhtb8mRiLI1ja3Ep80M-zv9a-IVw/view?usp=sharing)

