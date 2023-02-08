# TrojAI-Project
## About this Project
This is an incomplete project worked on during my final undergraduate year with a Phd student. The purpose of this project is to investigate the differences in classification and neuron activation between deep learning models trained on clean data and deep learning models trained on backdoored data. For this project, convolutional neural networks (CNN) were trained on the MNIST dataset and hooks were used for feature extraction to compare different layers. The CNN used was the LeNet as it was a simple model with few layers and high performance on the MNIST digits dataset. The dataset was modified so that a filter with some kind of pattern was added to a certain percentage of each class while changing the label to a different one. For example, when training models for target class 1, 10 new MNIST datasets were created, with each dataset having a different class being modified. For each class from 0 to 9, a certain percentage of images have a filter applied to them. The filter used in this case is 3 black pixels on the bottom right corner. After the filter is applied to an image, the label of that image is changed to the target class, which is 1 in this example. Thus for every target class, 10 models are trained on the backdoored data and are compared to the model trained on the original MNIST dataset.
## Technologies Used
- Python
- PyTorch
- Numpy
- Matplotlib
- MNIST
## Code
Only target class 1 was investigated so far in this project. 11 LeNet models are trained on the different datasets and compared in various ways. Hooks were used to extract the final activation layer and heat maps were created to visualize the differences in neuron activation. Cosine similarity is used to measure the similarities between activations and a linear model was attempted to be fitted on the original activation layer and each of the backdoored layers. Further exploration was cut short due to graduation from school.

