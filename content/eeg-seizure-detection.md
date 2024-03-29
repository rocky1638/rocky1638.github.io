# EEG Seizure Detection

## Main talking points.

- preprocessing *(channels, windows, stride lengths, imbalanced dataset)*.
- stft *(rationale, creating spectrogram)*.
- model *(resnet transfer learning, batchnorm, fully connected layers, softmax at end)*.
- judging criteria *(heavily punishing false positives, rewarding using less channels)*.
- optimizations *(binary opening/closing)*.


## Overview

Created for [Neureka](https://neureka-challenge.com), a 2020 competition for seizure detection in scalp electrocencephalogram (EEG) readings. The dataset used in the competition was taken from the [Temple University EEG Corpus](https://www.isip.piconepress.com/projects/tuh_eeg), and submitted under the team name "RocketShoes". Our general approach was to use a pretrained ResNet18 model on overlapping windows of Short-Time Fourier Transformed (STFT) and preprocessed voltage readings to predict on the binary classification task of seizure versus background classes.

## Preprocessing

Given that the EEG data provided was of variable length and had differing sampling frequencies (commonly, but not limited to 256Hz, 400Hz and 1000Hz), we decided to cut windows of 30 seconds out from each recording. For a recording with frequency 400Hz for example, we would take 400 \* 30 = 12000 datapoints. For training and validation sets, we used variable strides between each 30s window to improve class imbalance, with an overlap of 28 seconds (2s stride) for the seizure class, and an overlap of 0s (stride of 30s) for the null class. Because the data was recorded with various configurations (tcp-ar, tcp-le, tcp-ar-a), with the final class missing channels 8 and 13 present in the other classes, these two channels were removed from *all* configurations. Finally, we apply a STFT to this data, cut out 0Hz, 60Hz and 120Hz (DC and common power-line frequency in North America), and add a small amount of gaussian noise to training data. This data is transformed to a tensor and passed directly to the model without normalization, as we use batch normalization layers in our convolutional model.

## Model

We used ResNet18 pretrained on ImageNet from [this repo](https://github.com/Cadene/pretrained-models.pytorch) with two fully connected linear layers. As the challenge allotted points for using a reduced number of input channels, we passed the number of input layers to the model as a variable. We trained individually on all 19 channels, and found the best performance channels 2, 9, and 13. In the interest of time, we assume that there is minimal cross-channel correlations, and train on these channels for our final model.

## Evaluation

Our best model was evaluated on the test set by using the same preprocessing procedure described above, with an overlap of 25s (5s stride). In overlapping regions, the average softmax prediction was taken, and we used a threshold to determine if the prediction yielded the seizure or background class. Because the competition heavily penalized false positives, we used an extremely high threshold, meaning we would only predict a seizure if it was very likely to be one. We also introduced a binary opening and closing operation, to merge and erode short segments of seizure and background guesses.

## Results

The results of the competition can be found [here](https://neureka-challenge.com/results), again, our team name was RocketShoes, and we placed fourth overall! With a team of two, and facing competition from large tech universities, we are very happy with our performance. Thanks to Novela Neurotech and NeuroTechX for organizing the challenge and providing data!
