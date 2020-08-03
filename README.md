# Pneumonia Diagnosis Using Deep Learning

## Introduction
The problem of proper diagnosis of disease is an essential need of today's world. One of the major issues that medical professionals face is the correct diagnosis of conditions and diseases of patients. Not being able to correctly diagnose a condition is a problem for both the patient and the doctor. Misdiagnosis could lead to malpractice lawsuits and overall hurt the doctor's business. The patient suffers by not receiving the proper treatement and risking greater harm to health by the condition that goes undetected; further the patient undergoes neccessary treatement and takes unnecessary medications, costing the patient time and money.

It happens in many cases that with bare eyes or by doctors sometimes reading the disease goes undetected. This can cause a lot. With the help of machine learning we can look at this problem and solve it more efficiently. 

Pneumonia is an infection in one or both lungs. Bacteria, viruses, and fungi cause it.

The infection causes inflammation in the air sacs in your lungs, which are called alveoli. The alveoli fill with fluid or pus, making it difficult to breathe. Also, Pneumonia is a contagious disease which can spread from person to person. I worst cases it can harm many lives if not treated on time.


In this project, we will apply machine learning and in particular Deep Learning to a dataset containing x-ray report of patients treated under an orgranization.

In this study, I will apply Convolutional Neural Network (CNN) and try to classify a patient as either having pneumonia or not having pneumonia. This problem lies in binary classification.

(Also, as we are concerned about the type of pneumonia as the patient either have Bacterial Pneumonia, Viral Pneumonia or no pneumonia. So, we will consider it as a 3 class clissification problem.)

Sample of X-ray : 

![pneumonia](https://miro.medium.com/max/1400/1*t-_EXQ3tlb8KOx6H7HN09A.jpeg)


# Data Description:
The dataset used in the project and study is used from a Kaggle Dataset : Chest X-Ray Images (Pneumonia)
The dataset can be downloaded from the :- [Kaggle](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia?)

The data is in the form of images, and a total of 5,856 X-Ray images JPG are involved.
These images are divided into 3 sections: Train , validation and test as follows : 

![data](https://github.com/Mystery01092000/Pneumonia-detection-from-x-ray/blob/master/Images/DataFolder.png)

### Data Distribution :
  Train data : 5216 images
  
  Test and val : 640 images
  
# Model and Algorithms used :
This project is entirely based on Deep Neural Networks and for image processing we use Convolutional Neural Networks.

## Convolutional Neural Networks

A Convolutional Neural Network (ConvNet/CNN) is a Deep Learning algorithm which can take in an input image, assign importance (learnable weights and biases) to various aspects/objects in the image and be able to differentiate one from the other. The pre-processing required in a ConvNet is much lower as compared to other classification algorithms. While in primitive methods filters are hand-engineered, with enough training, ConvNets have the ability to learn these filters/characteristics.

The architecture of a ConvNet is analogous to that of the connectivity pattern of Neurons in the Human Brain and was inspired by the organization of the Visual Cortex. Individual neurons respond to stimuli only in a restricted region of the visual field known as the Receptive Field. A collection of such fields overlap to cover the entire visual area.
  
  ![ConvNet](https://miro.medium.com/max/1400/1*uAeANQIOQPqWZnnuH-VEyw.jpeg)

## Convolution Layer - the Kernel
  
  A convolution is the simple application of a filter to an input that results in an activation. Repeated application of the same filter to an input results in a map of activations called a feature map, indicating the locations and strength of a detected feature in an input, such as an image.

The innovation of convolutional neural networks is the ability to automatically learn a large number of filters in parallel specific to a training dataset under the constraints of a specific predictive modeling problem, such as image classification. The result is highly specific features that can be detected anywhere on input images.

![conv layer](https://miro.medium.com/max/1400/1*ciDgQEjViWLnCbmX-EeSrA.gif)
  ## Conv2D :
   Keras Conv2D is a 2D Convolution Layer, this layer creates a convolution kernel that is wind with layers input which helps produce a tensor of outputs
## Pooling Layer 

  Similar to the Convolutional Layer, the Pooling layer is responsible for reducing the spatial size of the Convolved Feature. This is to decrease the computational power required to process the data through dimensionality reduction. Furthermore, it is useful for extracting dominant features which are rotational and positional invariant, thus maintaining the process of effectively training of the model.
  
  ![Pool](https://miro.medium.com/max/792/1*uoWYsCV5vBU8SHFPAPao-w.gif)
  
  We are going to use MaxPooling2D,
  ## MaxPooling2D :
  Max pooling operation for 2D spatial data. Downsamples the input representation by taking the maximum value over the window defined by pool_size for each dimension along the features axis. The window is shifted by strides in each dimension.
 
  ![](https://res.cloudinary.com/practicaldev/image/fetch/s--d2BTXISO--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_66%2Cw_880/https://developers.google.com/machine-learning/practica/image-classification/images/maxpool_animation.gif)
  
  
## Fully Connected Layer - Classification (FC) :

![FC](https://miro.medium.com/max/1400/1*kToStLowjokojIQ7pY2ynQ.jpeg)

